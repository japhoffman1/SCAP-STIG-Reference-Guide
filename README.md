# SCAP/STIG Reference Guide

A comprehensive reference guide for Security Content Automation Protocol (SCAP) and Security Technical Implementation Guide (STIG) tools, processes, and common findings. Designed to support DoD cybersecurity professionals in conducting compliance assessments, interpreting scan results, and remediating vulnerabilities in alignment with RMF and DoD cybersecurity policy.

---

## Purpose

This repository serves as a personal knowledge base and quick-reference guide for SCAP and STIG-based security assessments. It covers the core tools used in DoD environments, common STIG findings by severity, remediation guidance, and links to authoritative references — supporting efficient and accurate security assessment workflows.

---

## Repository Structure

```
scap-stig-reference-guide/
│
├── README.md                        # Project overview
├── tools/
│   ├── STIG_Viewer.md               # DISA STIG Viewer reference
│   ├── SCAP_Compliance_Checker.md   # SCC Tool reference
│   └── ACAS_Nessus.md               # ACAS/Nessus vulnerability scanning reference
├── controls/
│   ├── Common_CAT_I_Findings.md     # Critical findings reference
│   ├── Common_CAT_II_Findings.md    # Medium findings reference
│   └── Common_CAT_III_Findings.md   # Low findings reference
└── resources/
    └── Key_References.md            # DoD and NIST reference links
```

---

## What is SCAP?

Security Content Automation Protocol (SCAP) is a standardized framework developed by NIST for automating the process of checking systems against security configuration baselines. SCAP uses machine-readable content to automate vulnerability management, security measurement, and policy compliance evaluation.

### Core SCAP Components

| Component | Full Name | Purpose |
|-----------|-----------|---------|
| XCCDF | Extensible Configuration Checklist Description Format | Defines security checklists and benchmark rules |
| OVAL | Open Vulnerability and Assessment Language | Describes system state and vulnerability conditions |
| CVE | Common Vulnerabilities and Exposures | Standard identifier for known vulnerabilities |
| CVSS | Common Vulnerability Scoring System | Standardized vulnerability severity scoring |
| CPE | Common Platform Enumeration | Standardized naming for hardware and software |
| CCE | Common Configuration Enumeration | Identifiers for system configuration issues |

---

## What is a STIG?

A Security Technical Implementation Guide (STIG) is a cybersecurity configuration standard published by the Defense Information Systems Agency (DISA). STIGs provide prescriptive guidance for securing hardware and software used in DoD environments.

### Key Facts
- Published and maintained by **DISA**
- Available for hundreds of technologies including OS, applications, network devices, and databases
- Organized by **severity category**: CAT I (Critical), CAT II (Medium), CAT III (Low)
- Used as the basis for **security control assessments** under the RMF
- Reviewed and updated regularly — always use the **latest version**

---

## Quick Reference: Assessment Workflow

```
1. Download applicable STIG from DISA Cyber Exchange
        ↓
2. Load STIG into STIG Viewer or SCC Tool
        ↓
3. Run automated scan (SCAP/SCC) against target system
        ↓
4. Review scan results — identify Open findings
        ↓
5. Conduct manual checks for controls not covered by automation
        ↓
6. Document findings in checklist (CKL file)
        ↓
7. Remediate Open findings or document in POA&M
        ↓
8. Submit checklist as part of RMF package for ATO
```

---

## References

- [DISA Cyber Exchange — STIG Library](https://public.cyber.mil/stigs/)
- [DISA SCAP Tools](https://public.cyber.mil/stigs/scap/)
- [NIST SP 800-53 Rev 5](https://csrc.nist.gov/publications/detail/sp/800-53/rev-5/final)
- [NIST SCAP Overview](https://csrc.nist.gov/projects/security-content-automation-protocol)
- [DoD RMF Knowledge Service](https://rmfks.osd.mil)

---

## Author

Maintained as part of a personal cybersecurity portfolio demonstrating practical knowledge of DoD STIG assessment tools, SCAP automation, and RMF compliance processes.
