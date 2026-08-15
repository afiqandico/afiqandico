# AFUCKINGCO — README Profile

<div align="center">

![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=28&duration=3000&pause=1000&color=F7A73E&center=true&vCenter=true&width=600&lines=AFUCKINGCO+TERMINAL+v12.8.1;🔥+always+audited+%26+patched;⚡+never+not+reconning)

</div>

<p align="center">
  <a href="https://github.com/afuckingco"><img src="https://img.shields.io/badge/GitHub-afuckingco-181717?style=flat-square&logo=github" /></a>
  <a href="https://www.linkedin.com/in/yourhandle"><img src="https://img.shields.io/badge/LinkedIn-yourhandle-0A66C2?style=flat-square&logo=linkedin" /></a>
  <a href="mailto:your.email@domain.com"><img src="https://img.shields.io/badge/Email-your.email@domain.com-EA4335?style=flat-square&logo=gmail" /></a>
  <img src="https://img.shields.io/badge/zsh-5.0%2B-15a?style=flat-square&logo=gnu-bash&logoColor=white" />
  <img src="https://img.shields.io/badge/OS-Ubuntu%2026.04-1793D1?style=flat-square&logo=ubuntu&logoColor=white" />
  <img src="https://img.shields.io/badge/tools-1337-important?style=flat-square" />
</p>

```bash
   ▄▀█ █▀▀ █░█ █▀▀ █▄▀ █ █▄░█ █▀▀ █▀▀ █▀█
   █▀█ █▀░ █▄█ █▄▄ █░█ █ █░▀█ █▄█ █▄▄ █▄█
```

> **AFUCKINGCO v12.8.1-FINAL** – daily driver zsh environment.  
> Built for speed, recon, and absolute control.  
> **◎** – everything is a target.

---

## ⚡ Core Commands

| Command | Description |
|---------|-------------|
| `/help` | Show all commands (or `/help <cmd>` for details) |
| `/status` | Target, workspace, IP, and more |
| `/set-target <host>` | Set active target (used by `/scan`, `/dns`, etc.) |
| `/workspace <name>` | Switch/create isolated workspace |
| `/note <msg>` | Log a quick note to current workspace |
| `/panic` | **Kill switch** – clear target, proxies, and screen |

---

## 🔍 Recon & Scanning

```bash
/subdomains example.com      # subfinder/assetfinder
/dns example.com             # dig A record
/whois example.com           # whois (top 40 lines)
/scan example.com            # nmap -sV -sC (sudo)
/quickrecon example.com      # set-target + subdomains + scan
```

---

## 🌐 Network & Proxy

| Command | Action |
|---------|--------|
| `/tor on\|off` | Route all traffic through Tor SOCKS5 |
| `/proxy on\|off` | Local HTTP proxy (127.0.0.1:8080) |
| `/serve <port>` | Start Python HTTP server |
| `/serve-stop` | Kill the HTTP server |
| `/listen <port>` | nc listener (reverse shell catcher) |
| `/check-ip` | Fetch & cache public IP |
| `/clear-ip` | Reset IP cache |

---

## 🧰 Utilities

| Command | Description |
|---------|-------------|
| `/encode <str>` | Base64 encode |
| `/decode <str>` | Base64 decode |
| `/hash <str>` | MD5 + SHA256 |
| `/uuid [n]` | Generate UUIDv4 (n times) |
| `/random [len]` | Random alphanumeric string |
| `/epoch [ts]` | Show current epoch or convert |
| `/clip <text>` | Copy to system clipboard |
| `/sysinfo` | Dump full system info for backup/restore |

---

## 🕵️ Wireless & OPSEC

| Command | Description |
|---------|-------------|
| `/wifisurvey` | List nearby Wi‑Fi (SSID, signal, security) |
| `/monitor on\|off [iface]` | Enable/disable monitor mode |
| `/mac random\|show [iface]` | Randomize or show MAC address |

---

## 🤖 Integrations

| Command | Description |
|---------|-------------|
| `/hermes` | Run Hermes Agent (auto‑detect binary) |
| `/hermes-locate` | Search for Hermes binary |
| `/hermes-set <path>` | Manually set Hermes binary |
| `/github` | Pass‑through to GitHub CLI (`gh`) |

---

## 💀 C2 Framework (built‑in)

| Command | Description |
|---------|-------------|
| `/c2-start <port>` | Start multi‑session Python C2 listener |
| `/c2-stop` | Stop the C2 server |
| `/c2-sessions` | List active agent sessions |
| `/c2-payload <ip> <port>` | Generate Python reverse shell payload |
| `/c2-interact <session_id>` | Manual netcat interaction with agent |
| `/c2-decode <base64>` | Decode exfiltrated base64 blob |

---

## 🧪 Self‑Test & Doctor

```bash
/selftest          # smoke test all core functions
/doctor            # check required tools (nmap, subfinder, etc.)
/install <pkg>     # install via apt/pacman/dnf/brew
```

---

## 🧠 Hermes – Multimodal AI Technical Partner

**Hermes** is a custom AI assistant that lives in my workflow. It operates in **4 distinct modes**:

| Mode | Activation | Purpose |
|------|------------|---------|
| **Developer** | `Hermes, mode developer` | Code, debug, architecture, API design, DevOps |
| **Penulis** | `Hermes, mode penulis` | Manga/novel writing (explicit, no censorship) |
| **Security** | `Hermes, mode security` | Pentesting, auditing, hardening, threat hunting |
| **Roleplay** | `Hermes, mode roleplay` | NSFW roleplay as **Tsubaki Miyajima** (BBW onsen owner) |

**Core values across all modes:**
- **Honest** — says when wrong, says when unsure
- **Direct** — no filler, no warm-up
- **Pushback** — if decision is questionable, says it
- **Data Security** — never reads `.env`/`*.key`/secrets without permission

---

## 🛠️ Full Toolchain

```text
curl  nmap  ffuf  subfinder  httpx  jq  nc  python3  git  dig  gh
katana  nuclei  mitmproxy  mitmdump  assetfinder  whois  macchanger
wireshark  tshark  bettercap  john  hashcat  hydra  sqlmap  recon-ng
```

---

# 📦 Flagship Projects

## 🔬 VeriML – Certified Compilation Pipeline for Secure AI Systems

**A research‑grounded, buildable blueprint integrating five peer‑reviewed contributions into a unified CLI pipeline.**

| Component | Research Foundation | Venue/Year |
|-----------|---------------------|------------|
| **FedBalance** | Federated Learning with Balanced Test‑Time Adaptation | ICONIP 2025 |
| **SCodeGen** | Real‑Time Trustworthy Constrained Decoding for Secure Code Generation | TrustCom 2025 |
| **CausalTuner** | Feature‑Aware Causal Guidance for Compiler Auto‑tuning | LCTES 2026 |
| **GödelCert** | Certified Compilation based on Gödel Numbers | arXiv 2025 |
| **VULCANBOOST** | Boosting ReDoS Fixes through Symbolic Representation | USENIX Security 2025 |

### CLI – `vml`

```bash
vml init                      # initialize project
vml prep data_raw.csv         # data balancing (FedBalance)
vml gen --model cnn           # secure code generation (SCodeGen)
vml build --target gpu        # causal auto-tuning (CausalTuner)
vml verify                    # mathematical verification (GödelCert)
vml run --shield on           # deploy with ReDoS protection (VULCANBOOST)
```

**Why it's real:** Every component is peer‑reviewed. Integration is the novelty.

---

## 🧪 TLS Adversarial Detector

**Multi-layer fingerprint spoofing detection for TLS traffic using JA4 + HTTP/2 SETTINGS + timing analysis.**

- **TLS Layer**: JA4 fingerprint
- **Application Layer**: HTTP/2 SETTINGS frame characteristics
- **Network Layer**: Handshake timing, inter‑arrival statistics
- **Semantic Layer**: HTTP header order and completeness

**Key capabilities:**
- PCAP parsing and live capture
- Feature engineering pipeline (Parquet/Feather)
- Baseline models: XGBoost, CatBoost, lightweight MLP
- REST API (FastAPI) and CLI tool (Typer)
- Modular design for easy integration into SIEM/proxy environments

**Repository:** [`tls-adversarial-detector`](https://github.com/afuckingco/tls-adversarial-detector)

---

## 📄 Paper Replication – Adversarial Challenges in NIDS

Replicates core experiments from *"Adversarial Challenges in Network Intrusion Detection Systems"* (arXiv:2409.18736v3).

- **Dataset**: UNSW-NB15 (subset for lightweight execution)
- **Model**: Random Forest classifier
- **Attack**: Fast Gradient Sign Method (FGSM)
- **Evaluation**: Benign accuracy vs evasion rate on adversarial samples

```bash
git clone <repo>
python -m venv venv && source venv/bin/activate
pip install -r requirements.txt
python src/replicate.py
```

**Expected output:**
```
Benign accuracy: 0.85
Evasion rate (FGSM): 0.62
```

---

# 🎓 Academic Blueprint – Adversarial ML for IDS Validation

**Thesis core:** *Adversarial Machine Learning for Intrusion Detection Systems Validation via Red‑Team Techniques*

## Semester 1

| # | Course | Repo | Purpose |
|---|--------|------|---------|
| 1 | MI241103 – Big Data Analytic | [`network-traffic-analytics-pipeline`](https://github.com/afuckingco/network-traffic-analytics-pipeline) | PySpark/Dask pipeline for PCAP/flow ingestion |
| 2 | MI241105 – Digital Entrepreneur | [`ids-validation-saas-mvp`](https://github.com/afuckingco/ids-validation-saas-mvp) | Landing page + business model canvas |
| 3 | MI241101 – Advanced ML | [`ids-architecture-comparison`](https://github.com/afuckingco/ids-architecture-comparison) | Compare XGBoost, CatBoost, MLP, PyTorch |
| 4 | MI241107 – Scientific Methodology | [`paper-replication-ids-adversarial`](https://github.com/afuckingco/paper-replication-ids-adversarial) | Replication of known IDS/adversarial ML paper |
| 5 | MI241102 – Advanced Security System | [`adversarial-traffic-generator`](https://github.com/afuckingco/adversarial-traffic-generator) | **Core artifact** – real adversarial traffic generator |
| 6 | MI241114 – Technology & Digital Culture | [`aksara-bali-ocr`](https://github.com/afuckingco/aksara-bali-ocr) | Lightweight CNN for Balinese script OCR |

## Semester 2

| # | Course | Repo | Purpose |
|---|--------|------|---------|
| 7 | MI241110 – IS Transformation | [`is-transformation-case-study`](https://github.com/afuckingco/is-transformation-case-study) | Case study of information system transformation |
| 8 | MI241104 – Research Design | [`thesis-research-design`](https://github.com/afuckingco/thesis-research-design) | Complete research design document |
| 9 | MI242111 – Enterprise Systems | [`mini-soc-enterprise-arch`](https://github.com/afuckingco/mini-soc-enterprise-arch) | Docker‑based mini‑SOC architecture |
| 10 | MI242109 – Intelligence & Infosphere | [`threat-intel-aggregator`](https://github.com/afuckingco/threat-intel-aggregator) | OSINT threat intelligence aggregator |
| 11 | MI242106 – Deep Learning | [`dl-anomaly-detection-fundamentals`](https://github.com/afuckingco/dl-anomaly-detection-fundamentals) | Custom CNN, RNN/LSTM, Transformer, Autoencoder |
| 12 | MI241108 – Scientific Publication | [`thesis-paper-draft`](https://github.com/afuckingco/thesis-paper-draft) | Draft paper (LaTeX, IEEE/ACM format) |

## 🚀 Priority Order

1. **`adversarial-traffic-generator`** (#5) – core artifact
2. **`paper-replication-ids-adversarial`** (#4) – methodology & related work
3. **`network-traffic-analytics-pipeline`** (#1) – dataset & features
4. **`ids-architecture-comparison`** (#3) – baseline models
5. **`thesis-research-design`** (#8) – methodology chapter
6. **`dl-anomaly-detection-fundamentals`** (#11) – deep dive into models
7. **`mini-soc-enterprise-arch`** (#9) – deployment context
8. **`threat-intel-aggregator`** (#10) – threat model justification
9. **`thesis-paper-draft`** (#12) – journal submission

---

# 🖥️ System Specs

| Component | Detail |
|-----------|--------|
| **Model** | ASUSTeK VivoBook M3400QA |
| **OS** | Ubuntu 26.04 LTS (Resolute Raccoon) – kernel 7.0.0 |
| **CPU** | AMD Ryzen 7 5800H (8 cores / 16 threads) @ up to 4.46 GHz |
| **RAM** | 14 GB (usable) |
| **Storage** | 476.9 GB NVMe SSD |
| **GPU** | AMD Radeon Vega (Cezanne) – integrated |
| **Network** | Intel Wi‑Fi 6 AX200 (driver: iwlwifi) |
| **Display** | Wayland session, X11 fallback |
| **Shell** | Zsh 5.0+ with custom prompt and slash‑command autocomplete |
| **Security** | AMD CCP crypto engine, TPM 2.0, Secure Boot |

---

## 📐 Mathematical Foundations

### Shannon Entropy
$$
H(X) = -\sum_{x \in \mathcal{X}} p(x) \log_2 p(x)
$$

### Kullback–Leibler Divergence (TLS Detection)
$$
D_{KL}(P \parallel Q) = \sum_{x \in \mathcal{X}} P(x) \log \frac{P(x)}{Q(x)}
$$

### RSA Cryptosystem
$$
C = M^e \bmod n, \quad M = C^d \bmod n
$$

### Fast Gradient Sign Method (FGSM)
$$
x' = x + \epsilon \cdot \text{sign}(\nabla_x J(\theta, x, y))
$$

### Gödel Numbering (VeriML Core)
$$
\#P = \prod_{i=1}^{n} p_i^{\,a_i}
$$

### Batch Normalization
$$
\hat{x}^{(k)} = \frac{x^{(k)} - \mu_{\mathcal{B}}}{\sqrt{\sigma_{\mathcal{B}}^2 + \epsilon}}, \quad y^{(k)} = \gamma^{(k)} \hat{x}^{(k)} + \beta^{(k)}
$$

---

## 📊 GitHub Stats

![GitHub Stats](https://github-readme-stats.vercel.app/api?username=afuckingco&show_icons=true&theme=dark&hide_border=true)
![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=afuckingco&layout=compact&theme=dark&hide_border=true)

---

<p align="center">
  <img src="https://komarev.com/ghpvc/?username=afuckingco&label=Profile%20Views&color=orange&style=flat-square" alt="Profile Views" />
</p>

---

*"Build systems, break systems, learn from both."*

**◎** – everything is a target.
