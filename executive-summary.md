# Executive Summary
> OccuSafe's greatest security risk isn't a hacker.
> It's a falsified safety record that nobody knows was changed.

---

## Table of Contents
- [Situation](#situation)
- [What We Found](#what-we-found)
- [What's At Risk](#whats-at-risk)
- [What Needs to Happen](#what-needs-to-happen)
- [The Path to Certification](#the-path-to-certification)
- [Contact](#contact)

---

## Situation

OccuSafe processes some of the most sensitive workplace data that
exists — employee injury records, OSHA logs, incident investigations,
and return-to-work documentation. Customers trust OccuSafe to keep
those records accurate, complete, and available when they need them.

This assessment evaluated OccuSafe's current security posture
against ISO 27001:2022, HIPAA, and NIST CSF. The finding is direct:
OccuSafe has no formal security program. Security has been managed
informally — producing a posture that is reactive, undocumented,
and unverified.

---

## What We Found

**38 security gaps. 12 are critical.**

| Risk level | Count | Meaning |
|-----------|-------|---------|
| Critical | 12 | Immediate risk — no control exists |
| High | 17 | Significant risk — control incomplete |
| Moderate | 9 | Control present but unformalized |

**The four most significant findings:**

| Finding | Why it matters |
|---------|---------------|
| No audit trail on record modifications | Safety records can be altered without detection — silently and indefinitely |
| No disaster recovery plan | Ransomware attack today = indefinite operational shutdown with no recovery path |
| No access controls at data level | Employee health records accessible beyond HR — HIPAA violation |
| No incident response plan | A PHI breach today would be managed by improvisation — HIPAA notification deadlines would be missed |

---

## What's At Risk

**Three categories of harm — in order of severity:**

**1. Safety harm**
Falsified incident investigations mean root causes never get fixed.
Accidents recur. People get hurt again. This is OccuSafe's
domain-specific risk — and the one that distinguishes this
assessment from a standard SaaS security review.

**2. Regulatory and legal harm**
- OSHA inspection with inaccessible records = immediate citation
- HIPAA breach without notification = HHS investigation, fines
  up to $1.9M per violation category
- Altered records in litigation = evidence tampering exposure
- Lost enterprise deals = continued revenue impact

**3. Reputational harm**
OccuSafe's product is trust. Customers trust that their safety
records are accurate, complete, and protected. A breach —
especially one involving employee health data — would
fundamentally undermine that trust across all 200 customers
simultaneously.

---

## What Needs to Happen

**12 critical actions in the first 30 days:**

| Priority | Action | Owner |
|----------|--------|-------|
| 1 | Implement audit trail on all record modifications | Engineering Lead |
| 2 | Develop and test incident response plan | CTO + Legal |
| 3 | Implement role-based access controls at data level | Engineering Lead |
| 4 | Enforce MFA across all systems | Engineering Lead |
| 5 | Establish and test disaster recovery plan | CTO |
| 6 | Implement formal backup policy and verification | Engineering Lead |
| 7 | Execute Business Associate Agreements with HRIS vendors | Legal + HR |
| 8 | Implement data masking in non-production environments | Engineering Lead |
| 9 | Establish cloud configuration management process | CTO + Engineering |
| 10 | Implement privileged access management | CTO |
| 11 | Define security roles and responsibilities | CEO + CTO |
| 12 | Establish information security policy framework | CTO + Legal |

*Full remediation roadmap with all 38 findings, owners, timelines,
and framework mappings in [remediation-roadmap.md](remediation-roadmap.md).*

---

## The Path to Certification

**ISO 27001 certification in 12 months is achievable.**

| Milestone | Timeline |
|-----------|---------|
| Phase 1 complete — 12 critical findings resolved | Month 1 |
| Phase 2 complete — 17 high findings resolved | Month 3 |
| Phase 3 complete — 9 moderate findings resolved | Month 6 |
| Internal audit — verify all controls implemented | Month 8 |
| Stage 1 audit — documentation review | Month 10 |
| Stage 2 audit — implementation verification | Month 12 |
| ISO 27001 certificate issued | Month 12 |

**The business case:**
OccuSafe lost two enterprise deals in six months without
certification. Average enterprise contract value in the EHS
SaaS market ranges from $50K–$200K annually. ISO 27001
certification removes the primary barrier to closing those
deals — making the certification investment self-funding
within the first renewed or new enterprise contract.

---

## Contact

**Dara Thomas** — GRC Analyst & Consultant | Human-Centered Risk & Compliance

[LinkedIn](YOUR_LINKEDIN_URL) · dara.thomas.grc@gmail.com · [GitHub Portfolio](https://github.com/DaraStaysCurious)

---

*Part of the [grc-occusafe-iso27001](../README.md) repository.*
*Return to: [README.md](../README.md)*
