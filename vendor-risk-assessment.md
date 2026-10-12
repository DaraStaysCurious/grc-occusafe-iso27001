# Vendor & Third-Party Risk Assessment - OccuSafe HRIS Integrations

> The ISO 27001 gap analysis in this repo rated **A.5.19 - Supplier
> Relationships** as **Critical**, citing three unassessed HRIS
> integrations: Workday, ADP, and BambooHR. This document closes the assessment portion of that gap. The supplier security program and the AWS Business Associate Agreement remain open items in remediation-roadmap.md.

---

## Table of Contents

- [Executive Summary](#executive-summary)
- [Scope](#scope)
- [Vendor Profiles & Data Exposure](#vendor-profiles--data-exposure)
- [Attestation Review](#attestation-review)
- [Risk Rating](#risk-rating)
- [Remediation & Monitoring Plan](#remediation--monitoring-plan)
- [Contact](#contact)

---

## Executive Summary

OccuSafe's platform allows its 200 mid-market employer customers to
sync their employee rosters automatically, so that safety training
assignments, incident records, and certification tracking stay
current without manual data entry. The three most commonly requested
integrations are Workday, ADP, and BambooHR - none of which had been
formally assessed prior to this review.

This assessment evaluates each vendor's publicly documented security
attestations, identifies where attestation access is restricted or
scope is ambiguous, and assigns a residual risk rating consistent
with the methodology used throughout this repo.

---

## Scope

**Data flowing from each vendor into OccuSafe:** employee name,
employee ID, department, job title, employment status, and hire
date - sufficient to assign safety training and associate incident
records to the correct individual. Full payroll, compensation, and
banking data are explicitly out of scope for this integration and
are not transmitted to OccuSafe.

---

## Vendor Profiles & Data Exposure

| Vendor | Role for OccuSafe | Data Category | Sensitivity |
|---|---|---|---|
| Workday | Customer-side HRIS roster sync | Employee PII (name, ID, department, role) | Medium |
| ADP | Customer-side payroll/HR roster sync | Employee PII (name, ID, department, role) | Medium |
| BambooHR | Customer-side HRIS roster sync | Employee PII (name, ID, department, role) | Medium |

None of the three integrations touch employee health data, safety
incident content, or financial account data - those remain inside
OccuSafe's own environment, governed by the controls in the main
gap analysis.

---

## Attestation Review

| Vendor | Publicly Documented Attestations | Access | Source |
|---|---|---|---|
| **Workday** | SOC 1 Type II, SOC 2 Type II, SOC 3, ISO 27001, ISO 27701, ISO 27018, ISO 27017, ISO 42001, FedRAMP Moderate | Full public Trust & Compliance Center; detailed reports available to customers/prospects on request | compliance.workday.com |
| **ADP** | SOC 1 & SOC 2 reports; ISO/IEC 27001 and 27701 certifications for select services and locations | Restricted - reports and ISO certificates require a signed NDA through an ADP account team; scope of ISO certification is not stated as universal across all products/regions | adp.com/about-adp/data-security |
| **BambooHR** | SOC 1 & SOC 2 Type II (annual third-party audit); "maintains records in accordance with ISO 27001 standards" | Trust Center requires NDA registration (trust.bamboohr.com) | bamboohr.com/legal/security, bamboohr.com/legal/data-processing-agreement |

**Two findings worth flagging directly:**
1. ADP's ISO 27001/27701 certification is explicitly scoped to
   "select services and locations" - this needs to be confirmed
   against the specific ADP product OccuSafe's customers actually
   use before it can be relied on.
2. BambooHR's own Data Processing Agreement commits to maintaining
   records "in accordance with ISO 27001 ... standards" - that
   phrasing is not the same as holding a certified ISMS. It should
   be confirmed directly with BambooHR whether this is a formal
   certification or an internal alignment claim.

---

## Risk Rating

| Vendor | Data Sensitivity | Attestation Strength | Residual Risk |
|---|---|---|---|
| Workday | Medium | Strong — full public trust center, broadest certification set, FedRAMP Moderate | **Low** |
| ADP | Medium | Moderate — certifications exist but access is NDA-gated and scope is unconfirmed | **Moderate** |
| BambooHR | Medium | Moderate — SOC 2 Type II confirmed; ISO 27001 status ambiguous pending vendor confirmation | **Moderate** |

---

## Remediation & Monitoring Plan

- Request and review current SOC 2 Type II reports from ADP and
  BambooHR under NDA prior to any new customer integration going
  live; confirm subservice organizations covered.
- Obtain written confirmation from ADP of which specific product(s)
  and region(s) its ISO 27001/27701 certification covers.
- Request direct clarification from BambooHR on whether its ISO
  27001 posture is a certified ISMS or an internal alignment claim.
- Add all three vendors to the enterprise vendor register with a
  12-month reassessment cadence, consistent with A.5.19.
- Make SOC 2 report refresh and ISO clarification a standing
  condition of integration renewal, not a one-time check.

---

## Contact

**Dara Thomas** — GRC Analyst & Consultant | Human-Centered Risk & Compliance

[LinkedIn](https://www.linkedin.com/in/darafthomas/) · dara.thomas.grc@gmail.com · [GitHub Portfolio](https://github.com/DaraStaysCurious)

---

*Part of the [grc-occusafe-iso27001](https://github.com/DaraStaysCurious/grc-occusafe-iso27001) repository. Closes gap A.5.19 from [iso27001-gap-analysis.md](https://github.com/DaraStaysCurious/grc-occusafe-iso27001/blob/main/iso27001-gap-analysis.md).*
