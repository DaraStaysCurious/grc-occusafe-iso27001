# NIST CSF Mapping
> OccuSafe has partial controls in one function.
> Five of six CSF functions are at zero or minimal maturity.

---

## Table of Contents
- [Executive Summary](#executive-summary)
- [CSF Function Overview](#csf-function-overview)
- [Function Assessments](#function-assessments)
- [Maturity Heatmap](#maturity-heatmap)
- [Priority Actions by Function](#priority-actions-by-function)
- [Contact](#contact)

---

## Executive Summary

This document maps OccuSafe's current security posture against
NIST Cybersecurity Framework 2.0. The CSF provides a plain-language
view of security maturity across six functions — designed for
executive and board-level communication.

OccuSafe's current posture reflects an organization that has never
had a formal security program. Five of six CSF functions are at
zero or minimal maturity. The one partial exception — Protect —
has three incomplete controls that exist informally rather than
by design.

---

## CSF Function Overview

**OccuSafe maturity by function:**

| Function | Maturity | Summary |
|----------|---------|---------|
| 🔴 Govern | None | No policies, roles, or security strategy defined |
| 🔴 Identify | Initiated | Risk assessment completed through this engagement only |
| 🟡 Protect | Partial | Three incomplete controls — TLS, basic AV, partial logging |
| 🔴 Detect | Minimal | CloudTrail partially enabled — no monitoring or alerting |
| 🔴 Respond | None | Zero incident response capability |
| 🔴 Recover | None | No DR plan, no verified backups, no recovery procedures |

---

## Function Assessments

### 🔴 Govern
**Establishing and monitoring cybersecurity risk management
strategy, policies, and accountability.**

| Subcategory | Requirement | Current state | Gap |
|-------------|------------|---------------|-----|
| GV.OC — Organizational context | Understand the organization's role and risk tolerance | Not defined | No risk appetite statement, no security strategy |
| GV.RM — Risk management strategy | Established risk management strategy | None | No formal risk management program |
| GV.RR — Roles and responsibilities | Defined cybersecurity roles | CTO informally — undocumented | No formal roles, accountability, or authority defined |
| GV.PO — Policy | Information security policies | None | No policies of any kind exist |
| GV.OV — Oversight | Management oversight of cybersecurity | Informal | No formal review cadence, no board reporting |

**Critical gap:** Without Govern, every other function lacks
the organizational foundation to operate effectively. Policies,
roles, and strategy must be established before controls can be
meaningfully implemented.

---

### 🔴 Identify
**Understanding assets, risks, and vulnerabilities.**

| Subcategory | Requirement | Current state | Gap |
|-------------|------------|---------------|-----|
| ID.AM — Asset management | Inventory of assets and data | Completed — this engagement | No formal asset inventory existed prior |
| ID.RA — Risk assessment | Systematic risk assessment process | Completed — this engagement | No process existed prior — single point of failure |
| ID.IM — Improvement | Lessons learned from incidents | S3 incident reviewed informally | Root cause unresolved at process level |

**Key finding:** OccuSafe's Identify function exists only because
of this assessment engagement. No ongoing process exists to
maintain asset inventory or conduct periodic risk assessments.
The function will revert to zero maturity without formal
institutionalization.

---

### 🟡 Protect
**Implementing safeguards to prevent or limit cybersecurity events.**

| Subcategory | Requirement | Current state | Gap |
|-------------|------------|---------------|-----|
| PR.AA — Identity management and access control | Access controls enforced | Not enforced at data level | Role-based access absent — minimum necessary violated |
| PR.AT — Awareness and training | Security awareness program | None | No training program of any kind |
| PR.DS — Data security | Data protection controls | Partial — TLS in transit | No encryption at rest, no data masking, no DLP |
| PR.PS — Platform security | Secure configuration management | None | No configuration baselines — S3 incident root cause |
| PR.IR — Technology infrastructure resilience | Backup and recovery | Informal — unverified | No formal backup policy, no recovery testing |

**Partial credit:** TLS encryption in transit, basic endpoint
protection, and partial CloudTrail logging exist — but all three
are incomplete, unformalized, and unverified. Protect is the
strongest function by default, not by design.

---

### 🔴 Detect
**Identifying cybersecurity events when they occur.**

| Subcategory | Requirement | Current state | Gap |
|-------------|------------|---------------|-----|
| DE.CM — Continuous monitoring | Ongoing monitoring of systems and networks | None | No SIEM, no alerting, no anomaly detection |
| DE.AE — Adverse event analysis | Analysis of cybersecurity events | None | No log review process, no incident triage |

**Critical gap:** OccuSafe cannot currently detect a security
event in progress. The S3 misconfiguration was discovered
internally by chance — not through monitoring. A data integrity
attack on safety records could occur and persist indefinitely
without detection.

---

### 🔴 Respond
**Taking action when a cybersecurity event is detected.**

| Subcategory | Requirement | Current state | Gap |
|-------------|------------|---------------|-----|
| RS.MA — Incident management | Defined incident response process | None | No IR plan, no defined roles, no escalation procedures |
| RS.AN — Incident analysis | Analyzing incidents to understand impact | None | No analysis capability or forensic procedures |
| RS.CO — Incident response reporting | Communication during incidents | None | No notification procedures — customers, regulators, legal |
| RS.MI — Incident mitigation | Containing and mitigating incidents | None | No containment procedures defined |

**Critical gap:** This is OccuSafe's weakest function. A PHI
breach, ransomware attack, or data integrity incident today
would be managed entirely by improvisation. HIPAA breach
notification requirements — 60-day notification to HHS,
individual notification to affected employees — would likely
be missed entirely.

---

### 🔴 Recover
**Restoring capabilities after a cybersecurity event.**

| Subcategory | Requirement | Current state | Gap |
|-------------|------------|---------------|-----|
| RC.RP — Incident recovery plan | Documented recovery procedures | None | No DR plan, no recovery procedures |
| RC.BC — Business continuity | Business continuity during recovery | None | No BCP, no defined RTO or RPO |
| RC.CO — Recovery communication | Communication during recovery | None | No stakeholder communication plan |

**Key terms:**
- **RTO — Recovery Time Objective:** How quickly must systems
  be restored? OccuSafe has no defined RTO.
- **RPO — Recovery Point Objective:** How much data loss is
  acceptable? OccuSafe has no defined RPO.

Without defined RTO and RPO, OccuSafe has no basis for designing
a recovery program — and no way to communicate recovery
expectations to customers during an outage.

---

## Maturity Heatmap

**OccuSafe CSF maturity at a glance:**

| Function | Maturity level | Color |
|----------|---------------|-------|
| Govern | 0 — None | 🔴 |
| Identify | 1 — Initiated | 🔴 |
| Protect | 2 — Partial | 🟡 |
| Detect | 1 — Minimal | 🔴 |
| Respond | 0 — None | 🔴 |
| Recover | 0 — None | 🔴 |

**Target maturity post-remediation (12 months):**

| Function | Target maturity | Color |
|----------|----------------|-------|
| Govern | 3 — Defined | 🟢 |
| Identify | 3 — Defined | 🟢 |
| Protect | 3 — Defined | 🟢 |
| Detect | 2 — Partial | 🟡 |
| Respond | 3 — Defined | 🟢 |
| Recover | 3 — Defined | 🟢 |

---

## Priority Actions by Function

**The single most important action for each function:**

| Function | Priority action | Why |
|----------|----------------|-----|
| Govern | Establish information security policy framework | Nothing else can be formalized without policies |
| Identify | Institutionalize risk assessment as an ongoing process | Current maturity disappears without a repeating process |
| Protect | Implement role-based access controls at data level | Closes the most critical ISO 27001 and HIPAA gaps simultaneously |
| Detect | Implement centralized log management and alerting | OccuSafe currently cannot detect incidents in progress |
| Respond | Develop and test incident response plan | HIPAA breach notification obligations cannot be met without it |
| Recover | Establish and test disaster recovery plan | Ransomware today = indefinite operational shutdown |

---

## Contact

**Dara Thomas** — GRC Analyst & Consultant | Human-Centered Risk & Compliance

[LinkedIn](YOUR_LINKEDIN_URL) · dara.thomas.grc@gmail.com · [GitHub Portfolio](https://github.com/DaraStaysCurious)

---

*Part of the [grc-occusafe-iso27001](../README.md) repository.*
*Next: [remediation-roadmap.md](remediation-roadmap.md)*
