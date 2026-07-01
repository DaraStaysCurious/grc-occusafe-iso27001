# ISO 27001 Gap Analysis
> OccuSafe has no formal security program.
> This document maps exactly what that means against
> ISO 27001:2022 Annex A requirements.

---

## Table of Contents
- [Executive Summary](#executive-summary)
- [Gap Analysis Approach](#gap-analysis-approach)
- [Organizational Controls](#organizational-controls)
- [People Controls](#people-controls)
- [Physical Controls](#physical-controls)
- [Technological Controls](#technological-controls)
- [Statement of Applicability Summary](#statement-of-applicability-summary)
- [Contact](#contact)

---

## Executive Summary

OccuSafe has no formal information security program. Security has
been managed informally by the CTO — producing a posture that is
reactive, undocumented, and unverified. This gap analysis maps
OccuSafe's current state against ISO 27001:2022 Annex A across
all four control themes.

**Summary of findings:**

| Theme | Controls assessed | Critical gaps | High gaps | Moderate gaps |
|-------|-----------------|--------------|-----------|---------------|
| Organizational | 15 | 4 | 6 | 3 |
| People | 6 | 2 | 3 | 1 |
| Physical | 8 | 0 | 1 | 2 |
| Technological | 18 | 6 | 7 | 3 |
| **Total** | **47** | **12** | **17** | **9** |

*Note: 46 of 93 Annex A controls assessed as not applicable —
primarily physical controls not relevant to a remote,
cloud-hosted environment. Full applicability determinations
in Statement of Applicability Summary below.*

---

## Gap Analysis Approach

**For each control, three determinations are made:**

| Field | Definition |
|-------|-----------|
| Current state | What OccuSafe has in place today |
| Gap | What's missing versus ISO 27001 requirement |
| Rating | Critical / High / Moderate / Low / Not Applicable |

**Rating definitions:**

| Rating | Definition |
|--------|-----------|
| Critical | Control absent — immediate risk to data integrity, availability, or confidentiality |
| High | Control partially present — significant gaps remain |
| Moderate | Control present but not formalized or verified |
| Low | Control present — minor improvements needed |
| N/A | Control not applicable to OccuSafe's environment |

---

## Organizational Controls

**Most significant gap area after Technological.**
No formal security policies, no defined roles, no supplier
management program, no incident response plan.

| Control | Requirement | Current state | Gap | Rating |
|---------|------------|---------------|-----|--------|
| A.5.1 — Information security policies | Documented, approved, communicated policies | No formal policies exist | Complete absence of policy framework | **Critical** |
| A.5.2 — Information security roles | Defined roles and responsibilities | CTO informally owns security — no formal definition | No documented roles, responsibilities, or accountability | **Critical** |
| A.5.5 — Contact with authorities | Defined process for regulatory contact | No process defined | No OSHA, HHS, or law enforcement contact procedure | **High** |
| A.5.7 — Threat intelligence | Process for gathering and acting on threat intel | None | No threat monitoring or intelligence function | **High** |
| A.5.19 — Supplier relationships | Security requirements for suppliers | No supplier security program | HRIS integrations — Workday, ADP, BambooHR — unassessed | **Critical** |
| A.5.24 — Incident response planning | Documented incident response plan | None | No IR plan, no defined roles, no communication procedures | **Critical** |
| A.5.25 — Incident assessment | Process for classifying and prioritizing incidents | None | No classification criteria or escalation procedures | **High** |
| A.5.26 — Response to incidents | Defined response procedures | None | No containment, eradication, or recovery procedures | **High** |
| A.5.27 — Learning from incidents | Post-incident review process | S3 incident reviewed informally — no formal process | Root cause of S3 incident unresolved at process level | **High** |
| A.5.28 — Evidence collection | Forensic evidence collection procedures | None | No chain of custody or evidence preservation process | **High** |
| A.5.33 — Protection of records | Controls ensuring record authenticity and integrity | None | No audit trail, no integrity verification on safety records | **Critical** |
| A.5.34 — Privacy and PII | Privacy controls for personal information | Informal — no formal privacy program | No data subject rights process, no privacy policy | **High** |
| A.5.36 — Compliance review | Regular review of security compliance | None | No internal audit function, no compliance review cadence | **Moderate** |
| A.5.37 — Documented operating procedures | Documented procedures for security operations | None | No documented procedures for any security operation | **Moderate** |

---

## People Controls

**Security awareness is completely absent.**
No training program, no screening process, no offboarding
security procedures.

| Control | Requirement | Current state | Gap | Rating |
|---------|------------|---------------|-----|--------|
| A.6.1 — Screening | Background verification for employees | No formal screening process | No background checks — especially concerning for staff with health data access | **Critical** |
| A.6.2 — Terms of employment | Security responsibilities in employment terms | Not included in employment contracts | No security obligations formally established for any employee | **High** |
| A.6.3 — Security awareness training | Regular security awareness and training | None | No training program of any kind — phishing, data handling, incident reporting | **Critical** |
| A.6.4 — Disciplinary process | Formal process for security violations | None | No defined consequences for security policy violations | **High** |
| A.6.5 — Responsibilities after termination | Security obligations post-employment | No offboarding security process | No credential revocation, no access removal procedure | **High** |
| A.6.7 — Remote working | Security controls for remote workers | Informal | Remote engineering team — no formal remote work security policy | **Moderate** |

---

## Physical Controls

**Lowest gap area — remote company on AWS infrastructure.**
AWS handles physical data center security under shared
responsibility model. OccuSafe's physical exposure is limited
to employee devices and home office environments.

| Control | Requirement | Current state | Gap | Rating |
|---------|------------|---------------|-----|--------|
| A.7.1 — Physical security perimeters | Defined physical security boundaries | N/A — AWS hosted | AWS responsible for data center physical security | **N/A** |
| A.7.2 — Physical entry controls | Access controls for physical facilities | N/A — no physical office | Remote company — not applicable | **N/A** |
| A.7.6 — Working in secure areas | Procedures for secure area working | N/A | Not applicable | **N/A** |
| A.7.7 — Clear desk and screen | Clear desk and screen policies | No policy | Remote workers — no formal clear desk or screen lock policy | **Moderate** |
| A.7.8 — Equipment siting | Secure equipment placement | N/A — AWS hosted | Not applicable | **N/A** |
| A.7.9 — Security of assets off-premises | Security for assets used outside facilities | No policy | Employee laptops and mobile devices — no formal endpoint security policy | **High** |
| A.7.11 — Supporting utilities | Protection of power and infrastructure | N/A — AWS hosted | AWS responsible | **N/A** |
| A.7.14 — Secure disposal of equipment | Secure disposal of equipment and media | No policy | No formal device disposal or data destruction procedure | **Moderate** |

---

## Technological Controls

**Most critical gap area.**
Multiple absent controls directly enabling the highest-priority
risks identified in the risk assessment — record alteration,
ransomware, insider access, and multi-tenant exposure.

| Control | Requirement | Current state | Gap | Rating |
|---------|------------|---------------|-----|--------|
| A.8.2 — Privileged access management | Controls on privileged access rights | Informal — CTO manages | No formal privileged access program, no PAM tooling | **Critical** |
| A.8.3 — Information access restriction | Access restrictions based on policy | No formal access control | Role-based access not enforced at data level | **Critical** |
| A.8.4 — Access to source code | Controls on source code access | Informal | No formal source code access restrictions or review process | **High** |
| A.8.5 — Secure authentication | Secure authentication procedures | Basic — no MFA enforced | MFA not enforced across platform or internal systems | **Critical** |
| A.8.7 — Protection against malware | Malware protection controls | Basic endpoint protection | No formal malware protection program or EDR tooling | **High** |
| A.8.8 — Management of technical vulnerabilities | Vulnerability management program | None | No vulnerability scanning, no patch management process | **Critical** |
| A.8.9 — Configuration management | Secure configuration management | None | No configuration baselines — S3 incident root cause unresolved | **Critical** |
| A.8.10 — Information deletion | Secure deletion of information | None | No data retention policy, no secure deletion procedure | **High** |
| A.8.11 — Data masking | Masking of sensitive data | None | Employee health data not masked in non-production environments | **High** |
| A.8.12 — Data leakage prevention | DLP controls | None | No DLP tooling or monitoring | **High** |
| A.8.13 — Information backup | Backup policy and procedures | Informal — unverified | No formal backup policy, no verified recovery testing | **Critical** |
| A.8.15 — Logging | Security event logging | Partial — AWS CloudTrail enabled | No centralized log management, no log review process | **High** |
| A.8.16 — Monitoring activities | Network and system monitoring | None | No security monitoring program or SIEM | **High** |
| A.8.17 — Clock synchronization | Synchronized clocks across systems | Unknown | No verified clock synchronization — affects audit trail integrity | **Moderate** |
| A.8.24 — Use of cryptography | Cryptography policy and key management | Partial — TLS in transit | No formal cryptography policy, no key management program | **High** |
| A.8.25 — Secure development lifecycle | Security in development process | None | No SDL, no security requirements in development process | **Moderate** |
| A.8.32 — Change management | Formal change management process | Informal | No change management process — configuration changes uncontrolled | **Critical** |
| A.8.34 — Protection of information systems during audit | Controls during audit activities | None | No procedure for protecting systems during assessment activities | **Moderate** |

---

## Statement of Applicability Summary

**93 Annex A controls — applicability determination:**

| Status | Count | Notes |
|--------|-------|-------|
| Applicable — implemented | 3 | TLS encryption, AWS CloudTrail partial, basic endpoint protection |
| Applicable — partially implemented | 8 | Controls present but not formalized or verified |
| Applicable — not implemented | 36 | Controls required but absent — primary remediation targets |
| Not applicable | 46 | Primarily physical controls — remote, AWS-hosted environment |

**The 3 implemented controls:**

| Control | Implementation status |
|---------|----------------------|
| A.8.24 — Cryptography (partial) | TLS in transit — no formal policy or key management |
| A.8.15 — Logging (partial) | AWS CloudTrail enabled — no centralized management |
| A.8.7 — Malware protection (partial) | Basic endpoint protection — no formal program |

*Full Statement of Applicability available as a standalone
document on request.*

---

## Contact

**Dara Thomas** — GRC Analyst & Consultant | Human-Centered Risk & Compliance

[LinkedIn](YOUR_LINKEDIN_URL) · dara.thomas.grc@gmail.com · [GitHub Portfolio](https://github.com/DaraStaysCurious)

---

*Part of the [grc-occusafe-iso27001](../README.md) repository.*
*Next: [hipaa-crosswalk.md](hipaa-crosswalk.md)*
