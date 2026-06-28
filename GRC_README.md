# PaySecure Data & Cloud Security Risk Assessment Report 2026
**Analyst:** Irene Adesina, GRC Team | **Organization:** Irene LLC | **Date:** June 26, 2026

![GRC](https://img.shields.io/badge/GRC-Risk_Assessment-red?style=for-the-badge)
![PCI-DSS](https://img.shields.io/badge/PCI--DSS-Compliance-blue?style=for-the-badge)
![ISO27001](https://img.shields.io/badge/ISO_27001-Framework-green?style=for-the-badge)
![Cloud Security](https://img.shields.io/badge/Cloud-Security-orange?style=for-the-badge)

---

## Overview

This repository contains the full GRC (Governance, Risk & Compliance) risk assessment conducted by **Irene LLC** for **PaySecure Ltd.**, a FinTech company handling customer payment data and transaction processing.

During an internal compliance audit, a cloud storage bucket containing customer transaction logs was found to be **publicly accessible** due to a misconfiguration error. While no confirmed breach occurred, the exposure of PII, card references, and transaction data posed a **CRITICAL risk** — violating PCI-DSS and ISO 27001 standards.

---

## Report Details

| Field | Details |
|-------|---------|
| **Report Title** | PaySecure's Data & Cloud Security Risk Assessment 2026 |
| **Reported By** | Irene Adesina, GRC Team — Irene LLC |
| **Reported On** | June 26, 2026 |
| **Survey Population** | 10 respondents |
| **Response Rate** | 90% (9 of 10 responded) |
| **Target Audience** | IT Team & Developer Team |
| **Frameworks** | PCI-DSS | ISO 27001 | NIST CSF |

---

## Objective

To assess PaySecure's security posture by evaluating data protection practices, control effectiveness, and employee compliance awareness — and to recommend mitigation measures using structured GRC tools.

---

## GRC Tools Used

| Tool | Purpose |
|------|---------|
| **Survey** | 10-question anonymous survey targeting IT & DevOps teams across 3 sections: Awareness, Practices & Compliance |
| **Interview Checklist** | 12 structured questions for Cloud Engineering, IT Security & Compliance teams to identify control gaps |
| **SWOT Analysis** | Evaluated PaySecure's internal strengths/weaknesses and external opportunities/threats |
| **Risk Register** | Documented, scored (Likelihood × Impact), and prioritized 8 identified risks with mitigation actions |

---

## Executive Summary

The Q1 2026 GRC investigation identified significant security gaps specifically regarding:
- **Access Control** — MFA not enforced on critical systems
- **Cloud Storage Visibility** — No automated misconfiguration detection
- **Data Classification** — No data classification policy in place

With a **90% response rate**, the data reveals critical misconfigurations and a lack of standardised processes. Current practices pose a **HIGH risk** for data leakage and non-compliance with PCI-DSS and ISO 27001.

---

## Survey Findings

| Survey Area | YES | NO | MAYBE | Risk Level |
|-------------|-----|----|-------|------------|
| Is sensitive data classified (public, internal, confidential)? | 11.1% | 66.7% | 22.2% | 🔴 CRITICAL |
| Is cloud configuration reviewed against best practices? | 0% | 77.8% | 22.2% | 🔴 CRITICAL |
| Is MFA enabled for critical systems? | 22.2% | 66.7% | 11.1% | 🟠 HIGH |
| Is a cybersecurity framework adopted (ISO/NIST)? | 0% | 77.8% | 22.2% | 🟠 HIGH |
| Is an Incident Response Plan (IRP) documented? | 0% | 77.8% | 22.2% | 🔴 CRITICAL |

**Average Non-Compliance Rate: 73% across all 5 survey areas**

---

## Key Findings

### 🔴 Finding 1 — Data Classification (CRITICAL)
- **Observation:** 66.7% confirmed NO data classification policy exists. Only 11.1% confirmed classified data — meaning most PII and transaction data is untagged and unprotected.
- **GRC Finding:** Violates PCI-DSS Requirement 3 (Protect Stored Data). Customer card data and PII cannot be properly secured without classification.

### 🔴 Finding 2 — Cloud Configuration Review (CRITICAL)
- **Observation:** 77.8% said NO cloud configuration reviews are conducted. Zero respondents confirmed regular reviews — the direct root cause of the misconfigured public bucket.
- **GRC Finding:** Violates ISO 27001 Annex A.12.1 (Operational Procedures) and PCI-DSS Req 6.4.

### 🟠 Finding 3 — MFA on Critical Systems (HIGH)
- **Observation:** 66.7% confirmed MFA is NOT enabled. Only 22.2% confirmed MFA is active — leaving critical infrastructure vulnerable to credential-based attacks.
- **GRC Finding:** Violates PCI-DSS Requirement 8.3 (Secure Authentication) and ISO 27001 Annex A.9.4.

### 🟠 Finding 4 — Cybersecurity Framework Adoption (HIGH)
- **Observation:** 77.8% confirmed NO cybersecurity framework is formally adopted. No structured baseline for security controls or compliance measurement exists.
- **GRC Finding:** Without ISO 27001 or NIST CSF, PaySecure has no standardised approach to risk management.

### 🔴 Finding 5 — Incident Response Plan (CRITICAL)
- **Observation:** 77.8% confirmed NO documented IRP exists. Zero respondents confirmed an IRP — PaySecure has no formal breach response capability.
- **GRC Finding:** Violates PCI-DSS Requirement 12.10 and ISO 27001 Annex A.16.1.

---

## Risk Register Summary

| # | Risk | Likelihood | Impact | Score | Level |
|---|------|-----------|--------|-------|-------|
| R01 | Public cloud bucket exposes customer PII & transaction logs | 4 | 5 | 20 | 🔴 CRITICAL |
| R02 | No automated misconfiguration detection | 4 | 4 | 16 | 🔴 CRITICAL |
| R03 | PCI-DSS non-compliance — fines & audit failure | 4 | 5 | 20 | 🔴 CRITICAL |
| R04 | ISO 27001 certification at risk of revocation | 3 | 5 | 15 | 🔴 CRITICAL |
| R05 | Unauthorized data access by external threat actors | 3 | 5 | 15 | 🔴 CRITICAL |
| R06 | Staff lack training on secure cloud configuration | 4 | 3 | 12 | 🟠 HIGH |
| R07 | No DLP controls on cloud storage buckets | 3 | 4 | 12 | 🟠 HIGH |
| R08 | Reputational damage & customer churn if breach disclosed | 2 | 5 | 10 | 🟠 HIGH |

**Risk Scoring: Likelihood × Impact (1–5 scale) | ≥12 = CRITICAL | 8–11 = HIGH**

---

## SWOT Analysis

### Strengths (Internal — Positive)
- Existing ISO 27001 certification framework in place
- Dedicated IT Security and Compliance teams
- Audit trail via cloud provider access logs
- Incident discovered internally before external exploitation

### Weaknesses (Internal — Negative)
- No automated misconfiguration detection tooling
- No Data Loss Prevention (DLP) controls on cloud buckets
- Insufficient staff training on secure cloud configuration
- No approval workflow for bucket permission changes

### Opportunities (External — Positive)
- Deploy CSPM tools (AWS Config, Microsoft Defender for Cloud)
- Adopt Zero Trust architecture for cloud access
- Strengthen ISO 27001 Annex A.9 & A.12 controls
- Conduct third-party cloud penetration testing

### Threats (External — Negative)
- Regulatory fines — PCI-DSS non-compliance penalties
- ISO 27001 certification revocation risk
- Reputational damage if breach becomes public
- Threat actors actively scanning for exposed cloud buckets

---

## Recommendations

| Priority | Area | Action | Deadline | Risk |
|----------|------|--------|----------|------|
| 1 | Cloud Configuration | Set bucket to PRIVATE immediately; enable block public access; rotate all credentials | **Immediate** | 🔴 CRITICAL |
| 2 | Data Classification | Implement data classification policy (Public/Internal/Confidential/Restricted); tag all PII | **30 Days** | 🔴 CRITICAL |
| 3 | Incident Response Plan | Draft IRP aligned to PCI-DSS Req 12.10 & ISO 27001 A.16.1; define escalation paths | **30 Days** | 🔴 CRITICAL |
| 4 | MFA Enforcement | Enable MFA on ALL critical systems — admin portals, cloud consoles, payment systems | **14 Days** | 🟠 HIGH |
| 5 | Framework Adoption | Formally adopt ISO 27001 or NIST CSF; appoint GRC lead; begin SoA documentation | **90 Days** | 🟠 HIGH |

---

## Control Gaps Identified

| Domain | Gap | Framework Control |
|--------|-----|------------------|
| People | No cloud security awareness training | PCI-DSS Req 12.6 \| ISO A.7.2.2 |
| People | No defined owner for bucket permission reviews | ISO A.9.2.3 |
| Process | No change management process for bucket configs | PCI-DSS Req 6.4 \| ISO A.12.1.2 |
| Process | No incident response plan for data exposure | PCI-DSS Req 12.10 \| ISO A.16.1 |
| Process | No periodic access permission audit | ISO A.9.4.1 |
| Technology | No CSPM / misconfiguration scanning tool | PCI-DSS Req 11.3 \| ISO A.12.6 |
| Technology | No DLP controls on cloud storage | PCI-DSS Req 3.4 \| ISO A.13.2 |
| Technology | No alerting when bucket permissions change | ISO A.12.4.1 |

---

## Compliance Alignment

| Framework | Controls Applied |
|-----------|----------------|
| **PCI-DSS** | Req 3 (Data Protection), Req 6.4 (Change Mgmt), Req 8.3 (MFA), Req 11.3 (Security Testing), Req 12.10 (IRP) |
| **ISO 27001** | A.7.2.2 (Training), A.9.2.3 (Access Rights), A.9.4 (Authentication), A.12.1 (Operations), A.16.1 (Incidents) |
| **NIST CSF** | Identify, Protect, Detect, Respond, Recover functions |

---

## Repository Contents

```
PaySecure-GRC-Risk-Assessment-2026/
│
├── README.md                              # This file
├── PaySecure_GRC_WithFindings.pptx        # Full 18-slide PowerPoint presentation
├── PaySecure_GRC_WithFindings.pdf         # PDF version for easy viewing
│
├── Survey/
│   └── Google_Forms_Survey_Results.png    # Screenshots of actual survey responses
│
└── Report/
    ├── Executive_Summary.md               # Summary of findings
    └── Risk_Register.md                   # Full risk register
```

---

## References

| Source | URL |
|--------|-----|
| NIST SP 800-61r3 (2025) | https://csrc.nist.gov/pubs/sp/800/61/r3 |
| PCI-DSS v4.0 | https://www.pcisecuritystandards.org |
| ISO/IEC 27001:2022 | https://www.iso.org/standard/27001 |
| Splunk Add-on for Apache | https://docs.splunk.com/AddOns/ApacheWebServer |
| CIS Controls v8 | https://cisecurity.org/controls/v8 |
| OWASP Top 10 (2021) | https://owasp.org/Top10 |

---

> **Next Review Date:** September 26, 2026
> **Report Prepared by:** Irene Adesina, GRC Team — Irene LLC

*🛡️ Irene LLC — Governance, Risk & Compliance | Protecting PaySecure, One Control at a Time*
