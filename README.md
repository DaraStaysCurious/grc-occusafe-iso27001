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
| NIST CSF 2.0 | Findings mapped to the Govern, Identify, Protect, Detect, Respond, and Recover functions |
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
| [`vendor-risk-assessment.md`](vendor-risk-assessment.md) | HRIS integration vendor risk review (Workday, ADP, BambooHR): attestation review, risk ratings, monitoring plan | ✅ Complete |

---

## Key Findings Preview

- **Critical:** No formal data integrity controls — OSHA logs and
  incident records are alterable without audit trail
- **Critical:** No disaster recovery plan — ransomware attack would
  produce complete operational shutdown with no recovery path
- **Critical:** Employee health data accessible beyond HR — role-based access controls not enforced at data level
- **High:** Multi-tenant data isolation not formally verified —
  customer data separation relies on application logic without
  independent validation

*Full findings, risk scores, and remediation roadmap in the
documents above.*

---

Platform Implementation

The gap analysis above documents what OccuSafe needs. This section shows it operationalized as a working data model in ServiceNow App Engine Studio, not just described but actually configured.

Using a ServiceNow developer instance, I built a compliance data model in App Engine Studio (ServiceNow's GRC/IRM module is subscription-gated even on free developer tiers, so I built the equivalent structure directly):

Policy table — 3 governing policies (Information Security, Incident Response, Access Control), each mapped to the ISO 27001 domains they cover.
Control table — 8 controls pulled directly from this repo's gap analysis (A.5.1, A.5.24, A.8.2, A.8.3, A.8.5, A.8.8, A.8.13, A.8.32), each carrying its actual current-state / target-state language from the assessment above, linked to its governing policy.
Risk table — the four key findings from the executive summary, each linked to the specific control that mitigates it.

The result is a working relational chain — Risk → Mitigating Control → Governing Policy — the same structure underlying commercial platforms like Vanta, Drata, or Archer.
<img width="1695" height="1112" alt="Screenshot 2026-09-08 at 7 04 27 PM" src="https://github.com/user-attachments/assets/8a0bb1ac-e49a-4bee-904e-a0e596294127" />
Policy library - three governing policies mapped to ISO 27001, each built from a documented Critical-rated gap in the assessment above.
<img width="1689" height="1114" alt="Screenshot 2026-09-08 at 7 02 14 PM" src="https://github.com/user-attachments/assets/baaa4172-4fa5-4666-9eab-b412d1e81183" />
Control library - eight Annex A controls from the gap analysis, each carrying its current-state/target-state language and linked back to its governing policy.
<img width="1688" height="1110" alt="Screenshot 2026-09-08 at 7 09 10 PM" src="https://github.com/user-attachments/assets/1e86248a-1cee-4f8f-a987-dfdafae6b230" />
Risk register - the four key findings from the executive summary, each linked to its mitigating control via a Reference field.
<img width="1680" height="1112" alt="Screenshot 2026-09-08 at 6 59 57 PM" src="https://github.com/user-attachments/assets/fceef039-9b75-4ff7-b540-df85bfbcd397" />
The full relational chain in practice: a real risk (alterable safety records, no audit trail) linked directly to the control that mitigates it (A.8.32 — Change management).

---

## Contact

**Dara Thomas** — GRC Analyst & Consultant | Human-Centered Risk & Compliance

[LinkedIn](YOUR_LINKEDIN_URL) · dara.thomas.grc@gmail.com · [GitHub Portfolio](https://github.com/DaraStaysCurious)

---

*Part of the [DaraStaysCurious](https://github.com/DaraStaysCurious)
GRC & Cloud Security portfolio.*
*Methodology: [risk-assessment-methodology](https://github.com/DaraStaysCurious/risk-assessment-methodology)*
