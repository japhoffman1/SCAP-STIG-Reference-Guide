# SCAP Compliance Checker (SCC Tool)

## Overview
The SCAP Compliance Checker (SCC) is a DISA-developed tool that automates security configuration assessments against SCAP content. It scans target systems and produces detailed compliance reports, significantly reducing the manual effort required for STIG assessments.

---

## Key Features
- Automated scanning against SCAP benchmark content
- Supports Windows, Linux, and network device assessments
- Produces XCCDF results files compatible with STIG Viewer
- Generates HTML, XML, and text-based reports
- Identifies configuration findings without manual checklist review

---

## How SCC Fits Into the Assessment Process

```
Download SCAP Content (DISA)
        ↓
Load content into SCC Tool
        ↓
Run scan against target system (local or remote)
        ↓
SCC generates results file (.xml)
        ↓
Import results into STIG Viewer
        ↓
Review automated findings + conduct manual checks
        ↓
Finalize .ckl checklist for RMF submission
```

---

## Important Limitations
- SCC does **not** cover all STIG controls — some require manual verification
- Always supplement automated results with **manual checks**
- Results must be reviewed by a qualified assessor before submission
- SCC scans reflect the system state **at the time of scan** — rescan after remediation

---

## Common SCC Output Files

| File Type | Description |
|-----------|-------------|
| XCCDF Results (.xml) | Machine-readable results importable into STIG Viewer |
| HTML Report | Human-readable summary of findings |
| All Settings Report | Complete list of checked settings and results |

---

## Tips for Assessors
- Run SCC with **administrative/root privileges** for complete results
- Document the SCC version and SCAP content version used in your assessment report
- Use SCC results as a **starting point** — not a complete assessment
- Keep SCC and SCAP content updated to ensure current coverage

---

## Download
[DISA SCAP Tools — official download](https://public.cyber.mil/stigs/scap/)
