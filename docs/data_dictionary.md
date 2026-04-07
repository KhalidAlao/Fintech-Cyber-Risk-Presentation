# Data Dictionary – Cyber Risk Portfolio

This document defines all columns used in the Excel data files for the NexPay cyber risk simulation.

---

## 1. NexPay_Cloud_Risk_Register.xlsx

| Column Name | Data Type | Description | Allowed Values / Examples |
|-------------|-----------|-------------|---------------------------|
| Risk ID | String | Unique identifier for each risk | R‑001, R‑002, …, R‑010 |
| Risk Category | String | Area of cyber risk | Cloud Misconfiguration, IAM, Data Residency, Insecure APIs, Backup & Recovery, etc. |
| Risk Description | String | Detailed explanation of the risk and potential impact | Free text |
| Inherent Risk | Categorical | Risk level assuming no controls | High, Medium, Low |
| Control Effectiveness | String | How well existing controls mitigate the risk | Effective, Partially Effective, Ineffective, Not Started |
| Residual Risk | Categorical | Risk level after considering existing controls | High, Medium, Low |
| Remediation Owner | String | Team responsible for fixing the control gap | Cloud Engineering, IAM Team, Product Security, SecOps, Architecture, etc. |
| Status | String | Current progress of remediation | Not Started, In Progress, Mitigated, At Risk, Done |
| Regulatory Mapping | String | Relevant regulations or frameworks | NIST CSF PR.IP‑1, PCI DSS 6.5, UK DPA Art.32, etc. |
| Last Updated | Date | Most recent update to the risk record | DD‑MMM‑YYYY (e.g., 02‑Apr‑2026) |
| Likelihood (1-5) | Integer | Probability of risk occurring (1 = very low, 5 = very high) | 1, 2, 3, 4, 5 |
| Impact (1-5) | Integer | Severity if risk occurs (1 = low impact, 5 = critical) | 1, 2, 3, 4, 5 |
| Control Gap | String | Specific missing control or weakness | "No automated CSPM", "DAST pipeline missing", etc. |
| Remediation Target Date | Date | Deadline for completing remediation | DD/MM/YYYY (e.g., 30/06/2026) |
| Evidence of Progress | String | Latest update on remediation actions | Free text (e.g., "CSPM PoC started") |

---

## 2. NexPay_OpsResilience_Tracker.xlsx

### Sheet 1: IBS_Tracker (Important Business Services)

| Column Name | Data Type | Description | Allowed Values / Examples |
|-------------|-----------|-------------|---------------------------|
| Service ID | String | Unique identifier for the business service | IBS‑001, IBS‑002, …, IBS‑005 |
| IBS Name | String | Name of the Important Business Service | Instant P2P Transfers, Merchant Settlement, etc. |
| Description | String | Brief explanation of what the service does | Free text |
| Impact Tolerance (mins) | Integer | Maximum acceptable outage duration in minutes | 30, 120, 240, 1440 |
| Current RAG | String | Current resilience status | Red, Amber, Green |
| Last Incident Date | Date | Most recent incident affecting this service | DD‑MMM‑YYYY |
| Incident Duration (mins) | Integer | How long the last incident lasted | Integer (e.g., 35, 180) |
| Issue Description | String | Summary of what went wrong | Free text |
| Root Cause | String | Underlying reason for the incident | Free text (e.g., "DB connection pool exhausted") |
| Remediation Action | String | Actions taken or planned to prevent recurrence | Free text |
| Remediation Owner | String | Team responsible for the fix | Platform Eng, Payments Eng, ML Ops, etc. |
| Remediation Due Date | Date | Deadline for remediation completion | DD‑MMM‑YYYY |
| Status | String | Current state of remediation | Not Started, In Progress, Completed, At Risk |

### Sheet 2: Issue_Remediation_Log

| Column Name | Data Type | Description | Allowed Values / Examples |
|-------------|-----------|-------------|---------------------------|
| Issue ID | String | Unique identifier for the incident or issue | IR‑001, IR‑002, … |
| IBS ID | String | References the affected Important Business Service | IBS‑001, IBS‑003, etc. |
| Date Identified | Date | When the issue was first discovered | DD‑MMM‑YYYY |
| Issue Summary | String | Short description of the problem | Free text |
| Severity | String | Impact level of the issue | Critical, High, Medium, Low |
| Root Cause Category | String | Type of underlying failure | Capacity, Resilience, Certificate Mgmt, Memory leak, etc. |
| Remediation Task | String | Specific action to resolve the issue | Free text |
| Task Owner | String | Team or person assigned | Platform Eng, ML Ops, etc. |
| Planned Date | Date | Target completion date | DD‑MMM‑YYYY |
| Actual Completion | Date | Date the task was finished (if done) | DD‑MMM‑YYYY or blank |
| Status | String | Current progress | Not Started, In Progress, Done, At Risk |

### Sheet 3: Product_Change_Governance

| Column Name | Data Type | Description | Allowed Values / Examples |
|-------------|-----------|-------------|---------------------------|
| Change ID | String | Unique identifier for the change request | CH‑001, CH‑002, …, CH‑006 |
| Product/Feature | String | Name of the product or feature being changed | New Checkout Flow, Mobile App v4.2, etc. |
| Change Type | String | Classification of the change | Major, Minor, Infrastructure, Patch |
| Security Assessment Status | String | Overall security review stage | Approved, In Review, Blocked |
| DAST Result | String | Dynamic Application Security Test outcome | Pass, Fail, N/A, Pending |
| SAST Result | String | Static Application Security Test outcome | Pass, Fail, N/A, Pending |
| Pen Test Result | String | Penetration testing outcome | Pass, Fail, N/A, Pending |
| Third‑Party Library Scan | String | Result of dependency/vulnerability scan | Pass, Fail, N/A |
| Go‑Live Readiness | String | RAG status for production deployment | Green, Amber, Red |
| Planned Go‑Live Date | Date | Scheduled deployment date | DD‑MMM‑YYYY |
| Security Approver | String | Person/role who approved the change | AppSec Lead, CISO Office, Data Governance |
| Notes | String | Additional context or blockers | Free text |

---

## 3. mock_jira_export.csv

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| Issue Key | String | Unique Jira ticket identifier (prefix + number) |
| Summary | String | Brief title of the issue |
| Issue Type | String | Classification (Risk, Incident, Change) |
| Priority | String | Urgency/importance (Critical, High, Medium, Low) |
| Status | String | Current workflow state |
| Assignee | String | Team or person responsible |
| Created | Date | Ticket creation date |
| Due Date | Date | Target completion date |
| Resolution | String | How the issue was resolved (blank if open) |

---

## Notes

- All dates follow the format `YYYY-MM-DD` in the CSV and `DD-MMM-YYYY` or `DD/MM/YYYY` in Excel (depending on regional settings).
- RAG stands for Red (critical), Amber (warning), Green (healthy).
- This data is fictitious and used solely for portfolio purposes.
