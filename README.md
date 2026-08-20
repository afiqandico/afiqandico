<div align="center">

```bash
   ▄▀█ █▀▀ █░█ █▀▀ █▄▀ █ █▄░█ █▀▀ █▀▀ █▀█
   █▀█ █▀░ █▄█ █▄▄ █░█ █ █░▀█ █▄█ █▄▄ █▄█
```

# Adaptive Evasion Traffic Generator (AETG)
### *Lecture Notes on Adaptive IDS Validation via Red‑Team Techniques*

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python 3.11+](https://img.shields.io/badge/python-3.11+-blue.svg)](https://www.python.org/downloads/)
[![Docker](https://img.shields.io/badge/docker-✓-2496ED?logo=docker)](https://www.docker.com/)
[![Paper](https://img.shields.io/badge/paper-AETG_2026-blue)](AETG_paper/output/AETG_paper.pdf)

*"Chalk in hand, we derive it from first principles."*

</div>

---

## §0 — Preliminaries

> **Remark.** What follows is written the way it would be boarded in a
> Monday‑morning seminar: definitions first, mechanism second, results
> last. Erase and rewrite as needed — that is what chalk is for.

---

## §1 — Feature Extraction

**Definition 1.1.** Every network flow is mapped to a feature vector

$$
f_{\text{flow}} = \big[\,p,\; \bar{s},\; \sigma_s,\; u_{\text{src}},\; u_{\text{dst}},\; c_{\text{ja3}}\,\big]
$$

where $p$ is the protocol, $\bar{s}$ and $\sigma_s$ the mean and
standard deviation of packet size, $u_{\text{src}}, u_{\text{dst}}$
source/destination uniformity, and $c_{\text{ja3}}$ the TLS
fingerprint class.

---

## §2 — The Evasion Stealth Metric (ESM)

**Definition 2.1 (per‑feature distribution).** For feature $i$ and bin
$k$,

$$
P_i(k) = \frac{n_{\text{benign}}^{(i)}(k)}{N_{\text{benign}}}, \qquad
Q_i(k) = \frac{n_{\text{adv}}^{(i)}(k)}{N_{\text{adv}}}
$$

**Definition 2.2 (Jensen–Shannon divergence).**

$$
\mathrm{JSD}_i = \frac{1}{2} \sum_{k=1}^{K} \left[
P_i(k) \log \frac{2P_i(k)}{P_i(k) + Q_i(k)} +
Q_i(k) \log \frac{2Q_i(k)}{P_i(k) + Q_i(k)}
\right]
$$

**Definition 2.3 (aggregate ESM).**

$$
\mathrm{ESM} = \frac{\sum_{i=1}^{m} w_i \cdot \mathrm{JSD}_i}{\sum_{i=1}^{m} w_i}, \quad w_i = 1,\; m = 6
$$

$$
\mathrm{ESM}_{\text{norm}} = \frac{\mathrm{ESM}}{\ln 2}
$$

> **Remark.** Small $\mathrm{ESM}$ means the adversarial traffic sits
> close to the benign distribution in feature space — "quiet," in the
> jargon of the trade.

---

## §3 — Arm Selection via LinUCB

**Setup.** At round $t$, the context is $x_t \in \mathbb{R}^{16}$.

**Definition 3.1 (ridge estimator per arm $a$).**

$$
A_a = I_d + \sum_{s} x_s x_s^\top, \qquad
b_a = \sum_{s} r_s x_s, \qquad
\hat{\theta}_a = A_a^{-1} b_a
$$

**Rule 3.2 (UCB selection).**

$$
a_t = \arg\max_a \left( x_t^\top \hat{\theta}_a + \alpha \sqrt{x_t^\top A_a^{-1} x_t} \right)
$$

**Update.**

$$
A_a \leftarrow A_a + x_t x_t^\top, \qquad
b_a \leftarrow b_a + r_t x_t
$$

---

## §4 — Reward Shaping

**Definition 4.1.** Let $\rho_t \in [0,1]$ denote the *alert rate*
observed at round $t$ (fraction of adversarial samples that tripped
an IDS alert). The reward is

$$
r_t = (1 - \rho_t) \cdot (1 - \mathrm{ESM}_t)
$$

> **Remark.** The reward rewards two things simultaneously: getting
> past the sensor, *and* not standing out statistically once past it.

---

## §5 — The Detector (XGBoost Inference)

$$
x_{\text{norm}} = \frac{x - \mu}{\sigma}
$$

$$
P(y=1 \mid x) = \frac{1}{1 + e^{-F(x)}}, \qquad
F(x) = \sum_{m=1}^{M} f_m(x)
$$

$$
\hat{y} = \begin{cases}
1 & \text{if } P(y=1 \mid x) \geq 0.5 \\
0 & \text{otherwise}
\end{cases}
$$

---

## §6 — Evaluation Metrics

$$
\text{Precision} = \frac{TP}{TP + FP}, \qquad
\text{Recall} = \frac{TP}{TP + FN}
$$

$$
F_1 = 2 \cdot \frac{\text{Precision} \cdot \text{Recall}}{\text{Precision} + \text{Recall}}
$$

$$
\text{AUC} = \int_{0}^{1} \mathrm{TPR}(t) \cdot d(\mathrm{FPR}(t))
$$

$$
\text{Evasion Rate} = \frac{\big|\{\text{adversarial} \to \text{benign}\}\big|}{\big|\{\text{total adversarial}\}\big|}
$$

---

## §7 — The Alert Pipeline

The alert flow is a straight line — Suricata writes events, a
collector pushes them into Redis, and the evaluator counts them:

```
Suricata  --(eve.json)-->  push_alerts.py  --(Redis)-->  eval_ids.py
```

**Definition 7.1.** Let $K$ be the set of keys currently in Redis.
The number of active alerts is

$$
N_{\text{alert}} = \bigl|\{\, k \in K \;:\; k \text{ has prefix } \text{"alert:"} \,\}\bigr|
$$

---

## §8 — Final Aggregation

$$
\mathcal{R} = \{
F_1,\; \text{Precision},\; \text{Recall},\; \text{AUC},\; \text{Evasion Rate},\; N_{\text{alert}}
\}
$$

---

## 📊 Worked Examples

### Calibration run

$$
\text{Evasion Rate} = 0.968, \qquad
\overline{\mathrm{ESM}} = 0.14, \qquad
\text{Adaptation Speed} = 38 \text{ rounds}
$$

### Mini‑SOC + ML detector

$$
\text{Recall} = 1.0, \quad \text{Precision} = 0.5, \quad F_1 = 0.667, \quad \text{AUC} = 0.505
$$

$$
\text{Evasion Rate (vs ML)} = 0.0, \qquad
N_{\text{alert}} = 5
$$

### Adversarial training — before and after

| Model                   | $F_1$ | Evasion Rate |
|--------------------------|:-----:|:------------:|
| Baseline                 | 0.0   | 1.0          |
| Adversarially Trained    | 0.953 | 0.089        |

> **Remark, chalk underlined twice.** This is the whole point of the
> exercise: a detector trained only on clean traffic looks strong on
> paper and collapses the moment someone adapts against it. Train
> against the adversary, or don't call it validated.

---

<div align="center">

> *"Build systems. Break systems. Learn from both."*
> *"Security is an invariant, not a feature."*

**◎** — target · **⡇** — theorem

*Last updated: August 20, 2026*

</div>
