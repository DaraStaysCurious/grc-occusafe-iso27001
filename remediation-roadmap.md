# Remediation Roadmap
> Every finding has an owner, a due date, and a definition
> of done. A roadmap without those three things is a wish list.

---

## Table of Contents
- [Executive Summary](#executive-summary)
- [Prioritization Framework](#prioritization-framework)
- [Phase 1 — Immediate Actions](#phase-1--immediate-actions)
- [Phase 2 — Short Term](#phase-2--short-term)
- [Phase 3 — Medium Term](#phase-3--medium-term)
- [Full Remediation Table](#full-remediation-table)
- [Contact](#contact)

---

## Executive Summary

This roadmap sequences OccuSafe's remediation activities across
three phases — Immediate, Short Term, and Medium Term — against
a 12-month ISO 27001 certification timeline.

38 findings require remediation. 12 are critical. All 12 critical
findings must be resolved before certification audit Stage 2.

**Remediation summary:**

| Phase | Timeline | Findings | Focus |
|-------|---------|---------|-------|
| Phase 1 — Immediate | 0–30 days | 12 critical | Stop the bleeding |
| Phase 2 — Short term | 31–90 days | 17 high | Build the foundation |
| Phase 3 — Medium term | 91–180 days | 9 moderate | Formalize and verify |

---

## Prioritization Framework

**Findings prioritized by two factors:**

| Factor | Definition |
|--------|-----------|
| Risk rating | Critical / High / Moderate — from gap analysis |
| Effort vs. impact | Low effort + high impact findings addressed first |

**Effort/impact matrix:**

| | High Impact | Low Impact |
|-|------------|-----------|
| **Low Effort** | Do first | Do if time permits |
| **High Effort** | Plan carefully | Deprioritize |

---

## Phase 1 — Immediate Actions
### 0–30 Days — Stop the Bleeding

**12 critical findings. All must be resolved before Phase 2.**

| # | Finding | Owner | Effort | Frameworks closed |
|---|---------|-------|--------|------------------|
| 1 | Implement audit trail on all record modifications | Engineering Lead | Medium | ISO A.5.33, HIPAA Technical |
| 2 | Establish formal incident response plan | CTO + Legal | Medium | ISO A.5.24–26, NIST Respond |
| 3 | Implement role-based access controls at data level | Engineering Lead | High | ISO A.8.3, HIPAA Technical |
| 4 | Enforce MFA across all systems | Engineering Lead | Low | ISO A.8.5, HIPAA Technical |
| 5 | Establish and test disaster recovery plan | CTO | High | ISO A.8.13, NIST Recover |
| 6 | Implement formal backup policy and verification | Engineering Lead | Medium | ISO A.8.13, NIST Recover |
| 7 | Execute Business Associate Agreements with HRIS vendors | Legal + HR Director | Low | HIPAA Administrative |
| 8 | Implement data masking in non-production environments | Engineering Lead | Medium | ISO A.8.11, HIPAA Technical |
| 9 | Establish cloud configuration management process | CTO + Engineering | Medium | ISO A.8.9, NIST Protect |
| 10 | Implement formal privileged access management | CTO | Medium | ISO A.8.2, HIPAA Technical |
| 11 | Define and document security roles and responsibilities | CEO + CTO | Low | ISO A.5.2, NIST Govern |
| 12 | Establish information security policy framework | CTO + Legal | Medium | ISO A.5.1, NIST Govern |

---

## Phase 2 — Short Term
### 31–90 Days — Build the Foundation

**17 high-priority findings. Required for certification readiness.**

| # | Finding | Owner | Effort | Frameworks closed |
|---|---------|-------|--------|------------------|
| 13 | Implement security awareness training program | HR Director | Medium | ISO A.6.3, HIPAA Administrative |
| 14 | Establish vulnerability management program | Engineering Lead | Medium | ISO A.8.8, NIST Identify |
| 15 | Implement centralized log management and alerting | Engineering Lead | High | ISO A.8.15–16, NIST Detect |
| 16 | Establish supplier security program | CTO | Medium | ISO A.5.19, HIPAA Administrative |
| 17 | Implement endpoint security policy for remote workers | CTO | Low | ISO A.7.9, HIPAA Physical |
| 18 | Implement formal change management process | Engineering Lead | Medium | ISO A.8.32, NIST Protect |
| 19 | Establish data retention and deletion policy | Legal + HR Director | Low | ISO A.8.10, HIPAA Technical |
| 20 | Implement DLP controls | Engineering Lead | High | ISO A.8.12, NIST Protect |
| 21 | Establish formal cryptography policy and key management | CTO + Engineering | Medium | ISO A.8.24, HIPAA Technical |
| 22 | Implement employee background screening process | HR Director | Low | ISO A.6.1, HIPAA Administrative |
| 23 | Establish security terms in employment contracts | Legal + HR Director | Low | ISO A.6.2, HIPAA Administrative |
| 24 | Define and document offboarding security procedures | HR Director | Low | ISO A.6.5, HIPAA Administrative |
| 25 | Implement automatic session logoff | Engineering Lead | Low | ISO A.8.3, HIPAA Technical |
| 26 | Establish formal remote work security policy | CTO | Low | ISO A.6.7, HIPAA Physical |
| 27 | Implement secure development lifecycle | Engineering Lead | High | ISO A.8.25, NIST Protect |
| 28 | Establish threat intelligence function | CTO | Medium | ISO A.5.7, NIST Identify |
| 29 | Define disciplinary process for security violations | HR Director + Legal | Low | ISO A.6.4, HIPAA Administrative |

---

## Phase 3 — Medium Term
### 91–180 Days — Formalize and Verify

**9 moderate findings. Required for sustained certification.**

| # | Finding | Owner | Effort | Frameworks closed |
|---|---------|-------|--------|------------------|
| 30 | Implement clear desk and screen lock policy | HR Director | Low | ISO A.7.7, HIPAA Physical |
| 31 | Establish secure equipment disposal procedure | CTO | Low | ISO A.7.14, HIPAA Physical |
| 32 | Implement geographic redundancy — second AWS region | Engineering Lead | High | ISO A.8.13, NIST Recover |
| 33 | Establish internal audit and compliance review function | CTO | Medium | ISO A.5.36, NIST Govern |
| 34 | Document operating procedures for all security operations | CTO | Medium | ISO A.5.37, NIST Govern |
| 35 | Verify clock synchronization across all systems | Engineering Lead | Low | ISO A.8.17 |
| 36 | Establish audit system protection procedures | Engineering Lead | Low | ISO A.8.34 |
| 37 | Define process for responding to data subject rights requests | Legal + HR Director | Low | ISO A.5.34, HIPAA Privacy |
| 38 | Establish regulatory contact procedures | Legal | Low | ISO A.5.5, NIST Respond |

---

## Full Remediation Table

**All 38 findings — sortable by phase, owner, and framework:**

| # | Finding | Phase | Owner | Rating | ISO 27001 | HIPAA | NIST CSF |
|---|---------|-------|-------|--------|-----------|-------|---------|
| 1 | Audit trail on record modifications | 1 | Engineering | Critical | A.5.33 | Technical | Protect |
| 2 | Incident response plan | 1 | CTO + Legal | Critical | A.5.24–26 | Administrative | Respond |
| 3 | Role-based access controls | 1 | Engineering | Critical | A.8.3 | Technical | Protect |
| 4 | MFA enforcement | 1 | Engineering | Critical | A.8.5 | Technical | Protect |
| 5 | Disaster recovery plan | 1 | CTO | Critical | A.8.13 | — | Recover |
| 6 | Backup policy and verification | 1 | Engineering | Critical | A.8.13 | — | Recover |
| 7 | Business associate agreements | 1 | Legal + HR | Critical | A.5.19 | Administrative | Govern |
| 8 | Data masking — non-production | 1 | Engineering | Critical | A.8.11 | Technical | Protect |
| 9 | Cloud configuration management | 1 | CTO + Eng | Critical | A.8.9 | — | Protect |
| 10 | Privileged access management | 1 | CTO | Critical | A.8.2 | Technical | Protect |
| 11 | Security roles and responsibilities | 1 | CEO + CTO | Critical | A.5.2 | Administrative | Govern |
| 12 | Information security policy framework | 1 | CTO + Legal | Critical | A.5.1 | Administrative | Govern |
| 13 | Security awareness training | 2 | HR Director | High | A.6.3 | Administrative | Protect |
| 14 | Vulnerability management program | 2 | Engineering | High | A.8.8 | — | Identify |
| 15 | Centralized log management | 2 | Engineering | High | A.8.15–16 | Technical | Detect |
| 16 | Supplier security program | 2 | CTO | High | A.5.19 | Administrative | Govern |
| 17 | Endpoint security policy | 2 | CTO | High | A.7.9 | Physical | Protect |
| 18 | Change management process | 2 | Engineering | High | A.8.32 | — | Protect |
| 19 | Data retention and deletion policy | 2 | Legal + HR | High | A.8.10 | Technical | Protect |
| 20 | DLP controls | 2 | Engineering | High | A.8.12 | — | Protect |
| 21 | Cryptography policy and key management | 2 | CTO + Eng | High | A.8.24 | Technical | Protect |
| 22 | Background screening process | 2 | HR Director | High | A.6.1 | Administrative | Govern |
| 23 | Security terms in employment contracts | 2 | Legal + HR | High | A.6.2 | Administrative | Govern |
| 24 | Offboarding security procedures | 2 | HR Director | High | A.6.5 | Administrative | Govern |
| 25 | Automatic session logoff | 2 | Engineering | High | A.8.3 | Technical | Protect |
| 26 | Remote work security policy | 2 | CTO | High | A.6.7 | Physical | Protect |
| 27 | Secure development lifecycle | 2 | Engineering | High | A.8.25 | — | Protect |
| 28 | Threat intelligence function | 2 | CTO | High | A.5.7 | — | Identify |
| 29 | Disciplinary process | 2 | HR + Legal | High | A.6.4 | Administrative | Govern |
| 30 | Clear desk and screen lock policy | 3 | HR Director | Moderate | A.7.7 | Physical | Protect |
| 31 | Secure equipment disposal | 3 | CTO | Moderate | A.7.14 | Physical | Protect |
| 32 | Geographic redundancy | 3 | Engineering | Moderate | A.8.13 | — | Recover |
| 33 | Internal audit function | 3 | CTO | Moderate | A.5.36 | — | Govern |
| 34 | Documented operating procedures | 3 | CTO | Moderate | A.5.37 | — | Govern |
| 35 | Clock synchronization | 3 | Engineering | Moderate | A.8.17 | — | Protect |
| 36 | Audit system protection | 3 | Engineering | Moderate | A.8.34 | — | Protect |
| 37 | Data subject rights process | 3 | Legal + HR | Moderate | A.5.34 | Privacy | Govern |
| 38 | Regulatory contact procedures | 3 | Legal | Moderate | A.5.5 | — | Respond |

---

## Contact

**Dara Thomas** — GRC Analyst & Consultant | Human-Centered Risk & Compliance

[LinkedIn](YOUR_LINKEDIN_URL) · dara.thomas.grc@gmail.com · [GitHub Portfolio](https://github.com/DaraStaysCurious)

---

*Part of the [grc-occusafe-iso27001](../README.md) repository.*
*Next: [executive-summary.md](executive-summary.md)*
