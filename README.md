<div align="center">

```bash
   ▄▀█ █▀▀ █░█ █▀▀ █▄▀ █ █▄░█ █▀▀ █▀▀ █▀█
   █▀█ █▀░ █▄█ █▄▄ █░█ █ █░▀█ █▄█ █▄▄ █▄█
```

**Thesis:** *Adversarial ML for IDS Validation via Red‑Team Techniques*

$$
\Delta = \mathbb{E}[f(x) \mid x \sim D_{train}] - \mathbb{E}[f(x) \mid x \sim D_{adv}]
$$

</div>

---

## 🔬 Research Artifacts

| Project | Core Contribution | Performance |
|---------|-------------------|-------------|
| **VeriML** | Certified compilation via Gödel numbering: $\\#P = \prod_{i=1}^{n} p_i^{a_i}$ | 5 peer‑reviewed components (ICONIP '25 → USENIX '25) |
| **TLS Adversarial Detector** | JA4 + HTTP/2 SETTINGS + timing jitter ($\sigma_t < 2$ ms, $H \approx 3.2$ bits) | AUC **0.94** · FPR **0.03** |
| **Paper Replication (NIDS)** | FGSM attack: $x' = x + \epsilon \cdot \mathrm{sign}(\nabla_x J)$ on UNSW‑NB15 | Benign ACC **0.85** · Evasion **0.62** |

---

## 📐 Mathematical Canon

| Domain | Formula |
|:-------|:--------|
| **Evasion Gap** | $\Delta = \mathbb{E}[f(x) \mid x \sim D_{train}] - \mathbb{E}[f(x) \mid x \sim D_{adv}]$ |
| **Shannon Entropy** | $H(X) = -\sum_{x \in \mathcal{X}} p(x) \log_2 p(x)$ |
| **KL Divergence** | $D_{\text{KL}}(P \parallel Q) = \sum_{x \in \mathcal{X}} P(x) \log \frac{P(x)}{Q(x)}$ |
| **FGSM Attack** | $x' = x + \epsilon \cdot \mathrm{sign}(\nabla_x J(\theta, x, y))$ |
| **Cross‑Entropy Loss** | $\mathcal{L} = -\sum_{i=1}^{N} y_i \log \hat{y}_i$ |
| **Gödel Numbering** | $\\#P = \prod_{i=1}^{n} p_i^{a_i}$ |
| **Batch Normalisation** | $\hat{x}^{(k)} = \frac{x^{(k)} - \mu_{\mathcal{B}}}{\sqrt{\sigma_{\mathcal{B}}^2 + \epsilon}}, \quad y^{(k)} = \gamma^{(k)} \hat{x}^{(k)} + \beta^{(k)}$ |
| **Friis Transmission** | $P_r = P_t G_t G_r \left( \frac{\lambda}{4\pi r} \right)^2$ |
| **Shannon‑Hartley** | $C = B \log_2 \left( 1 + \frac{S}{N} \right)$ |
| **TCP Reno (AIMD)** | $\mathrm{cwnd} \leftarrow \mathrm{cwnd} + \frac{1}{\mathrm{cwnd}}, \quad \mathrm{cwnd} \leftarrow \frac{\mathrm{cwnd}}{2}$ |
| **RSA Cryptography** | $C = M^e \bmod n, \quad M = C^d \bmod n$ |
| **ECDH** (on $E(\mathbb{F}_p)$) | $Q = d \cdot G$ |

---

## 🎓 S2 Blueprint — 9 Priorities

1. `adversarial-traffic-generator`       ← core red‑team engine
2. `paper-replication-ids-adversarial`   ← methodology
3. `network-traffic-analytics-pipeline`  ← PySpark / Dask
4. `ids-architecture-comparison`         ← XGBoost / CatBoost / MLP
5. `thesis-research-design`              ← hypothesis: $\Delta > 0.3$
6. `dl-anomaly-detection-fundamentals`   ← CNN / LSTM / Transformer
7. `mini-soc-enterprise-arch`            ← Docker + alerting
8. `threat-intel-aggregator`             ← OSINT (CVSS > 7.0)
9. `thesis-paper-draft`                  ← IEEEtran LaTeX

---

> *"Build systems. Break systems. Learn from both."*
> *"Security is an invariant, not a feature."*

**◎** — target · **⟡** — theorem

## 📂 Portfolio

The complete implementation and experiments are available in the thesis portfolio repository:
https://github.com/afuckingco/Adversarial-ML-for-IDS-Validation-via-Red-Team-Techniques
