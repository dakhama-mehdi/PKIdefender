# PKI_Defender

![Status](https://img.shields.io/badge/status-in%20progress-yellow)
![PowerShell](https://img.shields.io/badge/PowerShell-5391FE?logo=powershell&logoColor=white)
![Platform](https://img.shields.io/badge/platform-Windows-0078D6?logo=windows&logoColor=white)
![AD CS](https://img.shields.io/badge/Active%20Directory-Certificate%20Services-0078D6)

**Robust PowerShell module for AD CS (Active Directory Certificate Services) forensics and defense against ongoing PKI attacks.**

[Online Example] : [View Online Example](https://dakhama-mehdi.github.io/PKIdefender/Examples/PKI_Defender_Report.html)

---

## Why PKI_Defender

Active Directory Certificate Services (AD CS) is one of the most under-monitored parts of an AD environment. A single misconfigured certificate template (an ESC1–ESC8-style privilege escalation path) or a forgotten "ghost" template can grant an attacker domain-wide persistence — and most SOCs have no visibility into it at all.

PKI_Defender is a lightweight, **read-only audit module**: it scans your AD CS environment, flags exploitable misconfigurations and orphaned/ghost templates, and reports on what needs fixing — without touching certificate requests or approvals. Nothing is changed on your CA.

## Features

- Detects common ESC-style AD CS misconfigurations (vulnerable template ACLs, enrollment rights, EKU issues, etc.)
- Identifies "ghost" certificate templates (published/enabled templates no longer in active use, or with stale/incoherent configuration)
- Designed to run from a monitoring server  **does not require installation on the CA itself**
- Read/audit mode only —no automatic Approve/Deny action on certificate requests
- Structured output suitable for reporting and remediation tracking

## Scope & assumptions

- Targets a **single-forest** AD CS environment (multi-forest is not currently supported)
- Runs remotely against your PKI/AD CS, from a supervision/monitoring server
- Requires read access to AD CS configuration and certificate templates

## Requirements

- PowerShell version, e.g. 5.1+
- Network/AD access to the target PKI environment


## About

Built by **Mehdi Dakama**, Microsoft MVP, independent consultant specializing in the Microsoft identity & security stack (Active Directory, PKI, MFA).

Available for PKI/AD CS audits, hardening, and deployment support

