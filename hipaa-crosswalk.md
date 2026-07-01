# HIPAA Crosswalk
> One remediation. Two frameworks closed.
> Where ISO 27001 and HIPAA overlap — and where they don't.

---

## Table of Contents
- [Executive Summary](#executive-summary)
- [HIPAA Background](#hipaa-background)
- [Crosswalk — ISO 27001 to HIPAA Security Rule](#crosswalk)
- [OccuSafe-Specific HIPAA Findings](#occusafe-specific-hipaa-findings)
- [Unified Remediation Opportunities](#unified-remediation-opportunities)
- [Contact](#contact)

---

## Executive Summary

OccuSafe processes employee Protected Health Information — injury
records, medical treatment data, and return-to-work documentation.
This makes HIPAA Security Rule compliance a requirement alongside
ISO 27001 certification.

This document maps ISO 27001 Annex A controls onto HIPAA Security
Rule safeguards — identifying where a single remediation closes
gaps in both frameworks simultaneously, and where HIPAA introduces
requirements beyond ISO 27001's scope.

**Key finding:** 14 of OccuSafe's most critical remediations
satisfy both ISO 27001 and HIPAA requirements. Unified remediation
reduces total implementation effort by an estimated 40%.

---

## HIPAA Background

**Two rules. One focus: protecting employee health information.**

| Rule | Scope | OccuSafe relevance |
|------|-------|-------------------|
| Privacy Rule | Who can access PHI and under what circumstances | Governs which OccuSafe stakeholders can access employee health records |
| Security Rule | How ePHI must be protected | Defines administrative, physical, and technical controls required |

**The Minimum Necessary Principle:**
Access to PHI must be limited to the minimum necessary to perform
a job function. At OccuSafe, this principle is currently violated
across multiple stakeholder groups.

| Stakeholder | Current access | Appropriate access | HIPAA concern |
|-------------|---------------|-------------------|---------------|
| Engineering Lead | Full production DB access | Masked test data only | **Highest risk** — engineers routinely exposed to real PHI during normal work |
| CEO | Undefined — no access controls | Summary reports only | Undefined access = potential overprivilege |
| CTO | Full system access | System access without PHI | Infrastructure access shouldn't include PHI |
| Head of Customer Success | Customer data access | Aggregated data only | Individual health records not required for role |
| HR Director | Full health record access | Full access — appropriate | Correct |
| Legal Counsel | Undefined | Specific records for specific cases | Conditional access not defined |

---

## Crosswalk

**ISO 27001 Annex A controls mapped to HIPAA Security Rule safeguards.**

### Administrative Safeguards

| HIPAA requirement | ISO 27001 control | Current state | Gap rating |
|------------------|------------------|---------------|-----------|
| Security management process — risk analysis | Clause 6 — Risk assessment | Completed — this document | ✅ Addressed |
| Security management process — risk management | A.5.1 — Information security policies | No formal policies | **Critical** |
| Assigned security responsibility | A.5.2 — Security roles | CTO informally — not documented | **Critical** |
| Workforce training and awareness | A.6.3 — Security awareness training | None | **Critical** |
| Evaluation — periodic security assessment | A.5.36 — Compliance review | None | **Moderate** |
| Business associate agreements | A.5.19 — Supplier relationships | No BAAs with HRIS vendors | **Critical** |

> **Note on Business Associate Agreements (BAAs):**
> HIPAA requires formal agreements with any vendor that handles
> PHI on OccuSafe's behalf. Workday, ADP, and BambooHR all
> process employee data that may include PHI. No BAAs currently
> exist — this is a standalone HIPAA requirement with no direct
> ISO 27001 equivalent.

---

### Physical Safeguards

| HIPAA requirement | ISO 27001 control | Current state | Gap rating |
|------------------|------------------|---------------|-----------|
| Facility access controls | A.7.1 — Physical security perimeters | N/A — AWS hosted | AWS responsible |
| Workstation use policy | A.7.7 — Clear desk and screen | No policy | **Moderate** |
| Workstation security | A.7.9 — Assets off-premises | No endpoint policy | **High** |
| Device and media controls | A.7.14 — Secure disposal | No disposal procedure | **Moderate** |

---

### Technical Safeguards

| HIPAA requirement | ISO 27001 control | Current state | Gap rating |
|------------------|------------------|---------------|-----------|
| Access controls — unique user IDs | A.8.3 — Information access restriction | Not enforced at data level | **Critical** |
| Access controls — emergency access | A.8.2 — Privileged access management | No formal program | **Critical** |
| Access controls — automatic logoff | A.8.3 — Information access restriction | Not implemented | **High** |
| Access controls — encryption and decryption | A.8.24 — Cryptography | Partial — TLS in transit only | **High** |
| Audit controls — activity logging | A.8.15 — Logging | Partial — CloudTrail only | **High** |
| Integrity controls — PHI alteration detection | A.5.33 — Protection of records | None | **Critical** |
| Transmission security — encryption in transit | A.8.24 — Cryptography | TLS implemented | ✅ Addressed |
| Data masking in non-production environments | A.8.11 — Data masking | None | **Critical** |

---

## OccuSafe-Specific HIPAA Findings

**Four findings unique to OccuSafe's PHI handling context:**

| Finding | HIPAA requirement | ISO 27001 equivalent | Rating |
|---------|------------------|---------------------|--------|
| No Business Associate Agreements with HRIS vendors | BAA requirement | A.5.19 — Supplier relationships | **Critical** |
| Engineers accessing real PHI in production | Minimum necessary principle | A.8.3 — Access restriction | **Critical** |
| No PHI data masking in non-production environments | Minimum necessary principle | A.8.11 — Data masking | **Critical** |
| No process for responding to patient rights requests | Privacy Rule — data subject rights | A.5.34 — Privacy and PII | **High** |

---

## Unified Remediation Opportunities

**Where one fix closes gaps in both frameworks:**

| Remediation | ISO 27001 controls closed | HIPAA safeguards closed |
|-------------|--------------------------|------------------------|
| Implement role-based access controls at data level | A.8.2, A.8.3 | Access controls — unique IDs, minimum necessary |
| Implement audit trail on all record modifications | A.5.33, A.8.15 | Audit controls, integrity controls |
| Implement data masking in non-production environments | A.8.11 | Minimum necessary, access controls |
| Establish security awareness training program | A.6.3 | Workforce training requirement |
| Formalize security roles and responsibilities | A.5.2 | Assigned security responsibility |
| Establish supplier security program + BAAs | A.5.19 | Business associate agreements |
| Implement MFA across all systems | A.8.5 | Access controls — authentication |
| Establish formal incident response plan | A.5.24, A.5.25, A.5.26 | Security incident procedures |
| Implement backup and DR program | A.8.13 | Contingency plan — backup |
| Establish vulnerability management program | A.8.8 | Security management process |
| Implement configuration management | A.8.9 | Security management process |
| Implement endpoint security policy | A.7.9 | Workstation security |
| Establish data retention and deletion policy | A.8.10 | Device and media controls |
| Implement cryptography policy and key management | A.8.24 | Encryption and decryption |

**14 unified remediations — each closing at least one ISO 27001
gap and one HIPAA requirement simultaneously.**

---

## Contact

**Dara Thomas** — GRC Analyst & Consultant | Human-Centered Risk & Compliance

[LinkedIn](YOUR_LINKEDIN_URL) · dara.thomas.grc@gmail.com · [GitHub Portfolio](https://github.com/DaraStaysCurious)

---

*Part of the [grc-occusafe-iso27001](../README.md) repository.*
*Next: [nist-csf-mapping.md](nist-csf-mapping.md)*
