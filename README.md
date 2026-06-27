# grc-occusafe-iso27001
> In a safety management platform, a tampered record is more
> dangerous than a stolen one. This assessment leads with that truth.

---

## Table of Contents
- [Executive Summary](#executive-summary)
- [Why This Assessment Is Distinctive](#why-this-assessment-is-distinctive)
- [Scope and Frameworks](#scope-and-frameworks)
- [Repository Contents](#repository-contents)
- [Key Findings Preview](#key-findings-preview)
- [Contact](#contact)

---

## Executive Summary

OccuSafe Technologies is a B2B SaaS platform serving 200 mid-market
employers across manufacturing, logistics, healthcare, and
construction. This project documents a full ISO 27001 readiness
assessment — with HIPAA and NIST CSF layered in — conducted against
a platform whose core product is the accurate, complete, and
tamper-proof documentation of workplace safety records.

The assessment applies the OHS-derived risk methodology documented
in [`risk-assessment-methodology`](https://github.com/DaraStaysCurious/risk-assessment-methodology)
— bringing a decade of safety management domain expertise to bear
on a platform built for safety managers.

---

## Why This Assessment Is Distinctive

**Most security assessments lead with confidentiality.
This one leads with integrity — and here's why.**

A falsified incident report doesn't just expose data. It means
the root cause of an accident never gets fixed — and someone
gets hurt again. On a platform where OSHA logs, witness statements,
and corrective action records are the product, record integrity
isn't a security concern. It's a safety concern.

**The CIA triad, reordered for OccuSafe's risk context:**

| Priority | CIA Element | OccuSafe risk |
|----------|------------|---------------|
| 1st | **Integrity** | Altered records → failed OSHA inspections, repeated accidents, criminal liability |
| 2nd | **Availability** | Inaccessible records → regulatory violations, ransomware = operational shutdown |
| 3rd | **Confidentiality** | Exposed health data → employee reluctance to report injuries, legal liability |

---

## Scope and Frameworks

**Organization:** OccuSafe Technologies — 85 employees, Atlanta GA,
AWS cloud infrastructure, 200 mid-market customers

**Frameworks applied:**

| Framework | Purpose |
|-----------|---------|
| ISO 27001:2022 | Primary certification framework — ISMS requirements and Annex A controls |
| HIPAA Security Rule | Employee health data protection — administrative, physical, technical safeguards |
| NIST CSF | Findings mapped to Identify, Protect, Detect, Respond, Recover functions |
| NIST 800-30 | Underlying risk assessment methodology |

**Data in scope:**

| Data type | Sensitivity | Primary concern |
|-----------|------------|----------------|
| Employee health records | High | Confidentiality + Integrity |
| Incident investigation records | High | Integrity + Availability |
| OSHA recordable injury logs | High | Integrity + Availability |
| Customer organizational data | Medium | Confidentiality |
| Employee training records | Medium | Availability |

---

## Repository Contents

| Document | What it covers | Status |
|----------|---------------|--------|
| `README.md` | Project overview and assessment framing | ✅ Complete |
| [`scope-and-context.md`](scope-and-context.md) | Company profile, asset inventory, stakeholder map | ✅ Complete |
| [`risk-assessment.md`](risk-assessment.md) | NIST 800-30 threat and vulnerability analysis | ✅ Complete |
| [`iso27001-gap-analysis.md`](iso27001-gap-analysis.md) | Annex A controls mapped against current state | ✅ Complete |
| [`hipaa-crosswalk.md`](hipaa-crosswalk.md) | ISO 27001 controls mapped to HIPAA safeguards | ✅ Complete |
| [`nist-csf-mapping.md`](nist-csf-mapping.md) | Findings mapped to NIST CSF functions | ✅ Complete |
| [`remediation-roadmap.md`](remediation-roadmap.md) | Prioritized findings with effort/impact matrix | ✅ Complete |
| [`executive-summary.md`](executive-summary.md) | CEO-level one-pager — board ready | ✅ Complete |

---

## Key Findings Preview

- **Critical:** No formal data integrity controls — OSHA logs and
  incident records are alterable without audit trail
- **Critical:** No disaster recovery plan — ransomware attack would
  produce complete operational shutdown with no recovery path
- **High:** Employee health data accessible beyond HR — role-based
  access controls not enforced at data level
- **High:** Multi-tenant data isolation not formally verified —
  customer data separation relies on application logic without
  independent validation

*Full findings, risk scores, and remediation roadmap in the
documents above.*

---

## Contact

**Dara Thomas** — GRC Analyst & Consultant | Human-Centered Risk & Compliance

[LinkedIn](YOUR_LINKEDIN_URL) · dara.thomas.grc@gmail.com · [GitHub Portfolio](https://github.com/DaraStaysCurious)

---

*Part of the [DaraStaysCurious](https://github.com/DaraStaysCurious)
GRC & Cloud Security portfolio.*
*Methodology: [risk-assessment-methodology](https://github.com/DaraStaysCurious/risk-assessment-methodology)*
