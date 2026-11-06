# Afiq Andico Pangimpian

**Security engineering & adversarial machine learning.** I build small, verifiable tools
for detection work, and I try to be precise about what my numbers actually prove.

---

## About

- **B.Comp.Sc. (S1), Computer Science** — ITB STIKOM Bali. GPA **3.34**, **144 credits**.
- **M.Comp.Sc. (S2) in Cyber Security** — starting **February 2027**.
- Based in Bali, Indonesia. Working in Indonesian and English.

My interest sits where detection engineering meets machine learning: what a model
reports, and whether that report survives an adversary who knows the model exists.

## Research

**Robustness of ML-based network intrusion detection (ML-NIDS) under problem-space
evasion.** Most adversarial-ML work on NIDS perturbs feature vectors; that is not what
an attacker can actually do on a wire. My work evaluates detectors against evasions
that remain valid at the protocol and traffic level, and reports the gap between
feature-space and problem-space results.

> Manuscript **in preparation** — not submitted, not under review, not accepted. When any
> of that changes I will state it with the submission ID. I would rather write
> "in preparation" than imply a status the record cannot back up.

Related threads: detection engineering (Suricata/Zeek rules, lab traffic capture) and
reproducibility of ML experiments (fixed seeds, versioned data, one command to
regenerate every table).

## Selected work

**[anf-cyber-shell](https://github.com/afiqandico/anf-cyber-shell)** — zsh framework
for authorised security research. One dispatcher over 16 external security CLIs
(nmap, httpx, nuclei, ffuf, subfinder, amass, nikto, whatweb, gobuster, sqlmap-free
recon, whois, dig, yara, suricata, jq, curl), workspace-scoped artefacts, a JSONL
audit log, and *GuardFall v2* — a command canonicaliser that rejects shell-injection
and destructive patterns before passthrough execution. 3,111 lines in a single zsh module, 116 subcommand functions; `make verify`
runs 15 checks (`PASS=15 FAIL=0` locally; 14 pass + 1 skipped in CI, where one check
needs a tool the runner does not have). MIT.

**[security-lab](https://github.com/afiqandico/security-lab)** — the CLI tooling I
actually use, consolidated: `sift` (zero-dependency Go secret scanner with git-history
walking), `dockguard` (Dockerfile linter), `log-anonymizer`, `sec-scan-cli` (npm audit /
pip-audit / gitleaks / Suricata in one pipeline), and `pilgrims` (modules for authorised
engagements) behind one `seclab` entry point. Secret-scan clean (`gitleaks detect`:
no leaks); the only credential-shaped strings in the repo are deliberately fake test
fixtures, allowlisted in `.gitleaks.toml` with the reason written next to them.

**[b-comp-sc-research](https://github.com/afiqandico/b-comp-sc-research)** —
undergraduate research on campus-management optimisation treated as a classification
problem across three domains (marketing → Random Forest, HR → Decision Tree,
operations → SVM/kNN). The README separates two kinds of numbers on purpose: the demo
pipeline is reproducible here and asserted by `verify.py` on the committed fixtures
(9–12 rows each, so a "100%" there means nothing about model quality), while the thesis
figures were computed on the full institutional dataset, which is **not** in the
repository and therefore cannot be regenerated from it.

**LaTeX book project** *(in progress)* — long-form technical writing authored as LaTeX
source rather than a word processor, so the manuscript stays diffable, version-controlled,
and buildable from a clean checkout. No link yet; it is not finished.

## How I work

Three rules I apply to my own output, including the repos above:

- **Reproducibility over polish.** If a number appears in a README or a paper, a script
  in the repo regenerates it from versioned inputs. A result I cannot re-run is a result
  I do not report. Every repo of mine ships a verification command, and I run it before
  I publish.
- **No fabricated numbers.** No placeholder metrics, no "approximately" F1 scores, no
  benchmark tables assembled from memory. When a claim stops being true, it is corrected
  in the README and the limitation is written down rather than quietly deleted.
- **Backup before mutation.** Full archive before any destructive or restructuring
  operation on a repo, and branch-scoped changes thereafter. An experiment is never the
  only copy of its result.

Practically: Python (scikit-learn, NumPy/pandas, matplotlib), detection tooling
(Suricata, Zeek, YARA), Go and zsh for CLI work, Docker for lab isolation, Lean 4 and
LaTeX when the problem is formal or the output is a document.

## Contact

- Email — **afiqandico13@gmail.com**
- GitHub — [@afiqandico](https://github.com/afiqandico)
- ORCID — [0009-0002-1750-9551](https://orcid.org/0009-0002-1750-9551)

Open to research collaboration on adversarial ML for network detection,
detection-engineering work, and reproducibility tooling. For anything involving testing
systems, I will ask for the scope in writing first.
