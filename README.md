# NovaWireless Trust Signal Health Pipeline
**Integrity Control Layer + Trust Signal Scoring (synthetic case study).**

> **NovaWireless is a fictional brand used for demonstration.**  
> Code + methodology are designed to be **industry-agnostic**.

## What this repo does
Dashboards can “look fine” while reality quietly gets worse. This pipeline is a **Goodhart-aware monitoring workflow** that:

1) **Validates dataset integrity** (quality gate)
2) **Quarantines bad rows** (audit trail + reasons)
3) **Runs trust-signal scoring only on clean data**
4) Produces **reports + charts** you can review or publish

In plain English: it helps you catch the moment your KPI dashboard starts lying with confidence.

---

## Workflow (high level)
### Step 1 — Integrity Control Layer (data quality gate)
Checks for:
- missing required fields (timestamp, customer_phone, etc.)
- unparseable timestamps
- non-binary flags (when expected)
- CRT sanity range (if CRT exists)
- duplicate `interaction_id` handling (policy-based)

Outputs:
- `output/calls_clean.csv`
- `output/calls_quarantine.csv`
- `output/integrity_flags.csv`
- `output/integrity_summary.json`

### Step 2 — Trust Signal Analysis (runs on clean data)
Creates:
- scored dataset + engineered features
- rep / ivr / repeat-customer summaries
- drift scoring + narrative summary report
- charts and correlation heatmaps

Outputs (examples):
- `output/calls_scored_cleaned.csv`
- `output/rep_summary.csv`
- `output/ivr_summary.csv`
- `output/customer_repeat_summary.csv`
- `output/summary_report.txt`
- `output/*.png`

---

## Quick start
### 1) Install dependencies
```bash
pip install -r requirements.txt
