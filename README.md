# Trust Signal Health Framework
**Governance signals for KPI-driven, AI-accelerated operations (Goodhart-aware monitoring).**

> **NovaWireless is a fictional case-study brand used for demonstrations.**  
> This repository contains methodology, code, and artifacts intended to be **industry-agnostic**.

📄 **Flagship paper:**  
**When KPIs Lie: Governance Signals for AI-Optimized Call Centers**  
- [Read the PDF](paper/When_KPIs_Lie_Governance_Signals_for_AI_Optimized_Call_Centers.pdf)

---

## What problem this solves
KPIs are supposed to measure reality. But when KPIs become targets, they stop being honest sensors.  
That’s **Goodhart’s Law** — and AI/automation accelerates it by optimizing faster than humans can notice distortion.

This repo is a **practical framework** to detect early warning signs of KPI distortion by monitoring:
- **Outcomes** (what happened)
- **Mechanisms** (why it happened)
- **Trust rupture signals** (how the experience is degrading)
- **Drift & decoupling** (when KPI “wins” stop producing real-world wins)

**In plain terms:** it helps you catch the moment your dashboard starts lying with confidence.

---

## Core concepts (quick, non-fluffy)
### 1) Outcomes are lagging
Metrics like churn, cancels, repeat contacts, or 30DACC often move *after* customers have already “decided.”

### 2) Trust signals are leading
Language shifts, volatility, mismatch/failure-mode clustering, escalation intensity, and friction patterns show up earlier.

### 3) Drift is the danger zone
The biggest risk is **decoupling**:
> KPIs improve while underlying drivers worsen.

That’s the signature smell of Goodhart.

---

## What’s in this repository
### Paper
- `paper/When_KPIs_Lie_Governance_Signals_for_AI_Optimized_Call_Centers.pdf`

### Toolkit (code)
- `src/` contains runnable scripts/modules for:
  - cleaning/redaction
  - signal extraction
  - outcome-linked comparisons
  - drift checks
  - reporting + chart generation

### Artifacts (outputs)
- `output/reports/` contains markdown reports (tables, lift/log-lift outputs, summaries)
- `output/figures/` contains generated charts used for GitHub + Colab

---

## Repo structure
```text
<repo-root>/
  paper/
    When_KPIs_Lie_Governance_Signals_for_AI_Optimized_Call_Centers.pdf

  src/
    # framework + pipelines

  data/
    # local datasets (recommended gitignored)

  output/
    reports/
    figures/
    clean/
    features/
    logs/

  README.md
  requirements.txt
  .gitignore
