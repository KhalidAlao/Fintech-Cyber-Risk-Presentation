# Cyber Risk Portfolio – PayPal UK Cyber Risk Intern (R0130999)

## Overview
This portfolio simulates a UK fintech’s cyber risk function using **Excel** and **Power BI (web version)** . All data is fictitious but based on real FCA, GDPR, and PCI DSS requirements.

> **Note:** A live Power BI link is not available, but full dashboard screenshots are included below and in the `/screenshots` folder.

---

## Repository Contents

| File / Folder | Description |
|---------------|-------------|
| `/data/NexPay_Cloud_Risk_Register.xlsx` | 10 cloud migration risks with inherent/residual scoring, control gaps, remediation owners, due dates, and regulatory mapping (NIST, PCI DSS, UK DPA). |
| `/data/NexPay_OpsResilience_Tracker.xlsx` | 5 Important Business Services (IBS), incident durations (avg 156 min), remediation logs, and 6 product changes with security assessment status. |
| `/data/mock_jira_export.csv` | Simulated Jira issues (RISK-101, INC-205, CHG-089) to demonstrate ticketing tool familiarity. |
| `/presentation/NexPay_Executive_Summary_April2026.pptx` | 6-slide deck prepared for a UK Technology Risk Committee. |
| `/screenshots/` | Three Power BI dashboard screenshots (see previews below). |
| `/docs/data_dictionary.md` | Explanation of columns used in the Excel files (documentation discipline). |

---

## Dashboard Previews (Screenshots)

### 1. Operational Risk Dashboard
*Tracks 10 cloud migration risks with residual risk scoring, control gaps, remediation owners, and a likelihood vs. impact scatter chart.*


**Key metrics:**
- 4 High residual risks (R‑001, R‑002, R‑005, R‑008)
- 4 Medium, 2 Low
- Risk categories: Cloud Misconfiguration, IAM, Insecure APIs, Backup & Recovery, etc.
- Regulatory mapping: NIST CSF, PCI DSS, UK DPA/GDPR

---

### 2. Product Governance Dashboard
*Monitors 6 product changes with security assessment status (Approved, In Review, Blocked), go‑live readiness, and security approvers.*


**Key findings:**
- 1 Blocked change (Cloud Migration Phase 1 – SQL injection found, fix required)
- 2 In Review (New Checkout Flow, Real‑time Balance API – awaiting pen tests)
- 3 Approved changes ready for go‑live

---

### 3. Operational Resilience Dashboard
*Tracks 5 Important Business Services (IBS) with RAG status (Red/Amber/Green), average incident duration (156.4 min), and remediation owners.*


**Key metrics:**
- 5 IBS monitored
- RAG distribution shown in pie chart
- Impact tolerance: e.g., 30 min for checkout, 24 hours for statements
- Remediation owners: Platform Eng, ML Ops, Payments Rel, etc.

---

## Skills Demonstrated

- **Excel:** Data modelling, tables, conditional formatting, date management
- **Power BI Service:** Creating visuals (scatter, donut, cards, bar charts, tables), dashboard storytelling
- **Risk frameworks:** NIST CSF, PCI DSS, ISO 27001
- **Regulatory:** UK DPA, GDPR, FCA operational resilience rules
- **Communication:** Executive summary slides, concise risk reporting

---
