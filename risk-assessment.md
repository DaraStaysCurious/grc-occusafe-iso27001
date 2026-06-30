# Risk Assessment
> The most dangerous threats to OccuSafe aren't the ones that
> stop operations. They're the ones nobody notices until
> someone gets hurt again.

---

## Table of Contents
- [Executive Summary](#executive-summary)
- [Methodology](#methodology)
- [Threat Identification](#threat-identification)
- [Vulnerability Identification](#vulnerability-identification)
- [Risk Scoring](#risk-scoring)
- [Risk Priority Summary](#risk-priority-summary)
- [Contact](#contact)

---

## Executive Summary

This risk assessment applies NIST 800-30 methodology — informed
by the OHS-derived risk framework documented in
[risk-assessment-methodology](https://github.com/DaraStaysCurious/risk-assessment-methodology)
— to OccuSafe's current security posture.

The assessment identifies four threat categories. Data integrity
threats are prioritized above availability, insider, and external
threats — because falsified safety records cause recurring harm
that may never be detected, while availability threats are
immediately visible and trigger immediate response.

---

## Methodology

**Framework:** NIST 800-30 — Guide for Conducting Risk Assessments

**Risk scoring model:** Likelihood × Exposure × Impact
*(Three-variable model derived from Fine-Kinney — see
[risk-scoring-crosswalk.md](https://github.com/DaraStaysCurious/risk-assessment-methodology/blob/main/risk-scoring-crosswalk.md))*

**Risk levels:**

| Score | Risk Level | Action |
|-------|-----------|--------|
| Very High | Immediate remediation required | Stop / contain |
| High | Remediation within 30 days | Priority action |
| Moderate | Remediation within 90 days | Planned action |
| Low | Monitor | Ongoing awareness |

**Finding sources used in this assessment:**

| Source | Findings generated |
|--------|-------------------|
| Stakeholder interviews | CTO resistance, informal security posture |
| Infrastructure review | S3 misconfiguration history, no DR plan |
| Documentation review | No formal policies, no access control program |
| Prior incident analysis | S3 exposure — root cause unresolved at process level |

---

## Threat Identification

**Four threat categories identified, ranked by risk priority.**

### Threat 1: Data Integrity — Alteration of Safety Records

| Element | Detail |
|---------|--------|
| **Threat source** | Malicious insider, compromised customer account, external attacker with platform access |
| **Threat event** | Alteration of OSHA logs, incident investigations, witness statements, corrective action records |
| **Why it's the highest priority** | Silent and undetectable — falsified records look identical to legitimate ones; root causes never fixed; accidents recur |
| **OHS parallel** | Carbon monoxide vs. fire — invisible until catastrophic |
| **Affected assets** | OSHA injury logs, incident investigation records, witness statements, corrective action records |

---

### Threat 2: Availability — Ransomware and Data Loss

| Element | Detail |
|---------|--------|
| **Threat source** | Ransomware groups, infrastructure failure, accidental deletion |
| **Threat event** | Encryption or destruction of OccuSafe database — complete operational shutdown |
| **Why it's high priority** | No disaster recovery plan; no verified backups; OSHA inspection during outage = immediate regulatory violation |
| **OHS parallel** | All safety records in one filing cabinet with no copies and no contingency plan |
| **Affected assets** | AWS production environment, RDS database, S3 storage, all customer data |

---

### Threat 3: Insider Threat — Unauthorized Access and Accidental Exposure

| Element | Detail |
|---------|--------|
| **Threat source** | Employees with excessive access, accidental misconfiguration, unauthorized data pulls |
| **Threat event** | Employee health data accessed beyond HR; customer data exposed across tenant boundaries |
| **Why it's high priority** | No formal access control program; S3 incident caused by insider misconfiguration; CTO managing security informally |
| **OHS parallel** | No restricted areas — anyone can walk into chemical storage |
| **Affected assets** | Employee health records, customer organizational data, multi-tenant data boundaries |

---

### Threat 4: External Attack — Targeted Platform Breach

| Element | Detail |
|---------|--------|
| **Threat source** | Ransomware groups, opportunistic hackers, data brokers |
| **Threat event** | Platform breach exposing all 200 customer datasets simultaneously |
| **Why it's elevated** | B2B SaaS platforms are high-value targets — one breach affects all customers; misconfiguration history suggests hardening gaps |
| **OHS parallel** | Warehouse storing 200 companies' goods with no security cameras and an unlocked back door |
| **Affected assets** | All customer data, employee health records, OSHA logs |

---

## Vulnerability Identification

**Vulnerabilities mapped to threat categories:**

| Vulnerability | Type | Threat category | Severity |
|---------------|------|----------------|----------|
| No audit trail on record modifications | Technical | Data Integrity | Critical |
| No document integrity verification | Technical | Data Integrity | Critical |
| No disaster recovery plan | Process | Availability | Critical |
| No verified backup process | Technical | Availability | Critical |
| No formal access control program | Process | Insider | Critical |
| Role-based access not enforced at data level | Technical | Insider | High |
| Multi-tenant isolation unverified | Technical | External / Insider | High |
| No cloud configuration review process | Process | External / Insider | High |
| No formal incident response plan | Process | External | High |
| Security awareness training absent | People | All categories | High |
| CTO resistance to security findings | Organizational | All categories | Predisposing condition |
| Single AWS region — no geographic redundancy | Technical | Availability | Moderate |

---

## Risk Scoring

**Risks scored using Likelihood × Exposure × Impact:**

| Risk | Likelihood | Exposure | Impact | Risk Level |
|------|-----------|---------|--------|-----------|
| Record alteration — no audit trail | High | High | Very High | **Very High** |
| Ransomware — no DR plan | Moderate | High | Very High | **Very High** |
| Insider data exposure — no access controls | High | High | High | **Very High** |
| Multi-tenant data breach | Moderate | High | Very High | **High** |
| External platform breach | Moderate | High | High | **High** |
| Accidental misconfiguration | High | High | Moderate | **High** |
| Unavailability during OSHA inspection | Low | Moderate | Very High | **Moderate** |

---

## Risk Priority Summary

**Four findings require immediate action before any other
remediation activity begins.**

| Priority | Finding | Rationale |
|----------|---------|-----------|
| 1 | Implement audit trail on all record modifications | Silent integrity attacks are undetectable without it |
| 2 | Establish and test disaster recovery plan | No recovery path from ransomware currently exists |
| 3 | Implement formal access control program | Insider threat and accidental exposure risk is unacceptably high |
| 4 | Verify multi-tenant data isolation | 200 customers exposed if tenant boundaries fail |

*Full gap analysis, control mapping, and remediation roadmap
in subsequent documents.*

---

## Contact

**Dara Thomas** — GRC Analyst & Consultant | Human-Centered Risk & Compliance

[LinkedIn](YOUR_LINKEDIN_URL) · dara.thomas.grc@gmail.com · [GitHub Portfolio](https://github.com/DaraStaysCurious)

---

*Part of the [grc-occusafe-iso27001](../README.md) repository.*
*Next: [iso27001-gap-analysis.md](iso27001-gap-analysis.md)*
