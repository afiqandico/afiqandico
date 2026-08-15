<div align="center">

![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=26&duration=3000&pause=1000&color=F7A73E&center=true&vCenter=true&width=600&lines=Adversarial+ML+for+IDS+Validation;Red-Team+%26+Secure+Compilation;TLS+Fingerprint+Spoofing+Detection)

</div>

<p align="center">
  <a href="https://github.com/afuckingco"><img src="https://img.shields.io/badge/GitHub-afuckingco-181717?style=flat-square&logo=github" /></a>
  <img src="https://img.shields.io/badge/zsh-5.0%2B-15a?style=flat-square&logo=gnu-bash&logoColor=white" />
  <img src="https://img.shields.io/badge/OS-Ubuntu%2026.04-1793D1?style=flat-square&logo=ubuntu&logoColor=white" />
</p>

> **Thesis:** *Adversarial Machine Learning for Intrusion Detection Systems Validation via Red-Team Techniques*  
> Building interconnected research artifacts spanning big data pipelines, ML architectures, and offensive security.

---

## 🔬 Flagship Projects

### 1. VeriML – Certified Compilation Pipeline

Unified CLI integrating **5 peer-reviewed contributions** (ICONIP 2025, TrustCom 2025, LCTES 2026, USENIX Security 2025).

```bash
vml init → vml prep → vml gen → vml build → vml verify → vml run
```

[`veriml`](https://github.com/afuckingco/veriml) *(WIP)*

---

### 2. TLS Adversarial Detector

Multi-layer fingerprint spoofing detection using **JA4 + HTTP/2 SETTINGS + timing analysis**.

- PCAP parsing + live capture
- Feature engineering → Parquet/Feather
- XGBoost, CatBoost, MLP baselines
- REST API (FastAPI) + CLI (Typer)

[`tls-adversarial-detector`](https://github.com/afuckingco/tls-adversarial-detector) · MIT

---

### 3. Paper Replication – Adversarial NIDS

Replicates *"Adversarial Challenges in Network Intrusion Detection Systems"* (arXiv:2409.18736v3).

- **Dataset:** UNSW-NB15 · **Model:** Random Forest · **Attack:** FGSM
- **Output:** Benign accuracy 0.85 · Evasion rate 0.62

[`paper-replication-ids-adversarial`](https://github.com/afuckingco/paper-replication-ids-adversarial)

---

## 🎓 Academic Blueprint – S2 Research Portfolio

**Core Artifact:** `adversarial-traffic-generator` — red-team engine (JA3 randomization, timing jitter, header manipulation)

### Semester 1

| # | Course | Repo | Purpose |
|---|--------|------|---------|
| 1 | Big Data Analytic | [`network-traffic-analytics-pipeline`](https://github.com/afuckingco/network-traffic-analytics-pipeline) | PySpark/Dask PCAP ingestion & feature aggregation |
| 2 | Digital Entrepreneur | [`ids-validation-saas-mvp`](https://github.com/afuckingco/ids-validation-saas-mvp) | Business model canvas + landing page |
| 3 | Advanced ML | [`ids-architecture-comparison`](https://github.com/afuckingco/ids-architecture-comparison) | XGBoost, CatBoost, MLP, PyTorch comparison |
| 4 | Scientific Methodology | [`paper-replication-ids-adversarial`](https://github.com/afuckingco/paper-replication-ids-adversarial) | **Methodological foundation** |
| 5 | Advanced Security System | [`adversarial-traffic-generator`](https://github.com/afuckingco/adversarial-traffic-generator) | ⭐ **Core Artifact** |
| 6 | Technology & Digital Culture | [`aksara-bali-ocr`](https://github.com/afuckingco/aksara-bali-ocr) | CNN for Balinese script OCR |

### Semester 2

| # | Course | Repo | Purpose |
|---|--------|------|---------|
| 7 | IS Transformation | [`is-transformation-case-study`](https://github.com/afuckingco/is-transformation-case-study) | System analysis case study |
| 8 | Research Design | [`thesis-research-design`](https://github.com/afuckingco/thesis-research-design) | **Methodology chapter** – hypotheses, variables, metrics |
| 9 | Enterprise Systems | [`mini-soc-enterprise-arch`](https://github.com/afuckingco/mini-soc-enterprise-arch) | Docker‑based mini‑SOC architecture |
| 10 | Intelligence & Infosphere | [`threat-intel-aggregator`](https://github.com/afuckingco/threat-intel-aggregator) | OSINT threat intelligence aggregator |
| 11 | Deep Learning | [`dl-anomaly-detection-fundamentals`](https://github.com/afuckingco/dl-anomaly-detection-fundamentals) | Custom CNN, RNN/LSTM, Transformer, Autoencoder |
| 12 | Scientific Publication | [`thesis-paper-draft`](https://github.com/afuckingco/thesis-paper-draft) | LaTeX draft (IEEE/ACM) for journal submission |

### Priority Order

```
1. adversarial-traffic-generator      ← core artifact
2. paper-replication-ids-adversarial  ← methodology
3. network-traffic-analytics-pipeline ← dataset
4. ids-architecture-comparison        ← baselines
5. thesis-research-design             ← methodology chapter
6. dl-anomaly-detection-fundamentals  ← deep dive
7. mini-soc-enterprise-arch           ← deployment
8. threat-intel-aggregator            ← threat model
9. thesis-paper-draft                 ← publication
```

> **Thesis Flow:** Proposal Defense → Results Seminar → Journal Publication → Thesis Defense

---

## ⚙️ Environment & Toolchain

**Shell:** AFUCKINGCO v12.8.1-FINAL (Zsh) with slash-command autocomplete

```text
nmap  subfinder  ffuf  httpx  nuclei  katana  mitmproxy  assetfinder
whois  macchanger  bettercap  wireshark  john  hashcat  hydra
sqlmap  recon-ng  nikto  gobuster  curl  jq  nc  python3  git  gh
```

**Hermes AI** – 4 modes: Developer · Penulis · Security · Roleplay

---

## 📐 Mathematical Foundations

| Concept | Formula |
|---------|---------|
| Shannon Entropy | $H(X) = -\sum p(x)\log_2 p(x)$ |
| FGSM Attack | $x' = x + \epsilon \cdot \text{sign}(\nabla_x J(\theta, x, y))$ |
| Gödel Numbering | $\P = \prod p_i^{a_i}$ |
| Batch Norm | $\hat{x} = \frac{x - \mu}{\sqrt{\sigma^2 + \epsilon}}, \quad y = \gamma\hat{x} + \beta$ |

---

## 📊 GitHub Stats

![GitHub Stats](https://github-readme-stats.vercel.app/api?username=afuckingco&show_icons=true&theme=dark&hide_border=true)
![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=afuckingco&layout=compact&theme=dark&hide_border=true)

---

<p align="center">
  <img src="https://komarev.com/ghpvc/?username=afuckingco&label=Profile%20Views&color=orange&style=flat-square" />
</p>

---

*"Build systems. Break systems. Learn from both."*

**◎** – everything is a target.
