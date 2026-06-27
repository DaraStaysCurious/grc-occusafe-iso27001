# Scope and Context
> Before assessing risk, understand the environment.
> Before understanding the environment, talk to the people inside it.

---

## Table of Contents
- [Company Profile](#company-profile)
- [Assessment Scope](#assessment-scope)
- [Asset Inventory](#asset-inventory)
- [Data Classification](#data-classification)
- [Stakeholder Map](#stakeholder-map)
- [Assessment Constraints](#assessment-constraints)
- [Contact](#contact)

---

## Company Profile

**OccuSafe Technologies** — B2B SaaS workforce health and safety
compliance platform. Helps mid-market employers manage OSHA
recordkeeping, incident reporting, corrective action tracking,
safety inspections, and employee training records.

| Attribute | Detail |
|-----------|--------|
| **Headquarters** | Atlanta, GA — fully remote engineering team |
| **Employees** | 85 |
| **Customers** | 200 mid-market employers |
| **Industries served** | Manufacturing, logistics, healthcare, construction |
| **Revenue** | $12M ARR — Series B, growing 40% YoY |
| **Infrastructure** | AWS — EC2, RDS, S3, CloudFront |
| **Architecture** | Single-tenant (enterprise) / multi-tenant (mid-market) |
| **Integrations** | Workday, ADP, BambooHR |
| **Prior security posture** | Informal — no formal security program to date |

**Why ISO 27001 now:**
Three enterprise prospects required ISO 27001 certification as a
condition of signing. OccuSafe lost two deals in six months without
it. Certification is now a board-level priority.

**Prior incident:**
8 months ago — misconfigured S3 bucket briefly exposed non-sensitive
customer configuration data. Discovered internally, resolved within
24 hours. No customer notification required. Root cause: no formal
cloud configuration review process.

---

## Assessment Scope

**In scope:**

| Area | Detail |
|------|--------|
| Cloud infrastructure | AWS environment — EC2, RDS, S3, CloudFront |
| Web application | Customer-facing platform and admin portal |
| Mobile application | Field inspection app — iOS and Android |
| Data processing | All customer data ingestion, storage, and retrieval |
| Third-party integrations | HRIS system connections — Workday, ADP, BambooHR |
| People and processes | Security awareness, access management, incident response |

**Out of scope:**
- Customer internal systems and networks
- Third-party HRIS platforms
- Physical security of customer facilities

---

## Asset Inventory

**Information assets ranked by criticality:**

| Asset | Type | Criticality | Primary CIA concern |
|-------|------|------------|-------------------|
| Employee health records | Data | Critical | Confidentiality + Integrity |
| Incident investigation records | Data | Critical | Integrity + Availability |
| OSHA recordable injury logs | Data | Critical | Integrity + Availability |
| Witness statements and photographs | Data | High | Integrity |
| Corrective action records | Data | High | Integrity + Availability |
| Employee training records | Data | High | Availability |
| Customer organizational data | Data | High | Confidentiality |
| AWS production environment | Infrastructure | Critical | Availability |
| Web application | System | Critical | Integrity + Availability |
| Mobile application | System | High | Integrity |
| HRIS integrations | System | High | Confidentiality + Integrity |
| Source code repository | System | High | Integrity |

---

## Data Classification

**OccuSafe data classified by sensitivity:**

| Classification | Definition | Examples |
|---------------|-----------|---------|
| **Restricted** | Highest sensitivity — breach causes serious harm | Employee health records, OSHA injury logs, incident investigations |
| **Confidential** | Sensitive — breach causes significant harm | Customer organizational data, corrective action records, training records |
| **Internal** | Internal use only — breach causes moderate harm | System configuration data, internal communications |
| **Public** | No sensitivity — available externally | Marketing materials, product documentation |

---

## Stakeholder Map

**Key stakeholders identified through assessment interviews:**

| Stakeholder | Role | Primary concern | Assessment relevance |
|-------------|------|----------------|---------------------|
| CEO | Executive sponsor | Certification timeline, enterprise deals | Risk appetite, resource authorization |
| CTO | Technical owner | Infrastructure security, S3 incident history | Control implementation authority |
| Head of Customer Success | Customer voice | Client data protection, trust | Customer-facing risk impact |
| HR Director | Employee data owner | Health data handling, medical privacy | HIPAA compliance, data classification |
| Engineering Lead | Implementation owner | Technical control deployment | Remediation execution |
| Legal Counsel | Risk and liability | Breach notification, OSHA liability | Incident response, legal requirements |

**Key finding from stakeholder interviews:**
The CTO is defensive about the S3 incident and resistant to
external assessment findings. This is documented as a predisposing
condition — organizational resistance to security findings is itself
a risk factor that affects control implementation likelihood.

---

## Assessment Constraints

**Factors that affect assessment scope or findings:**

| Constraint | Impact |
|------------|--------|
| No formal security program exists | Baseline is informal — gap analysis will be extensive |
| CTO resistance to findings | Control implementation risk is elevated |
| 12-month certification timeline | Remediation roadmap must be sequenced realistically |
| Remote engineering team | Physical security controls have limited applicability |
| Multi-tenant architecture | Data isolation controls require independent verification |
| Prior S3 incident unresolved at process level | Root cause — no cloud configuration review — remains open |

---

## Contact

**Dara Thomas** — GRC Analyst & Consultant | Human-Centered Risk & Compliance

[LinkedIn](YOUR_LINKEDIN_URL) · dara.thomas.grc@gmail.com · [GitHub Portfolio](https://github.com/DaraStaysCurious)

---

*Part of the [grc-occusafe-iso27001](../README.md) repository.*
*Next: [risk-assessment.md](risk-assessment.md)*
