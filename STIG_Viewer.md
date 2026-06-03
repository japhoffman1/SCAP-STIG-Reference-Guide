# DISA STIG Viewer

## Overview
STIG Viewer is a free tool published by DISA that allows cybersecurity professionals to load, view, and manage STIG checklists. It is the primary tool used in DoD environments for manual STIG assessments and documenting compliance status.

---

## Key Features
- Load and view STIG benchmark files (.xml format)
- Create and manage checklist files (.ckl format)
- Document finding status: Not a Finding, Open, Not Applicable, Not Reviewed
- Add comments and severity justifications to individual controls
- Export checklists for RMF package submission

---

## Common Status Values

| Status | Meaning |
|--------|---------|
| Not a Finding | Control has been verified as compliant |
| Open | Vulnerability exists and requires remediation |
| Not Applicable | Control does not apply to this system |
| Not Reviewed | Control has not yet been assessed |

---

## Typical Workflow

1. Download the applicable STIG XML file from [DISA Cyber Exchange](https://public.cyber.mil/stigs/)
2. Open STIG Viewer and import the STIG benchmark
3. Create a new checklist (.ckl) for the target system
4. Work through each control — document status and comments
5. Save and export the .ckl file for inclusion in the RMF package

---

## Tips for Assessors
- Always use the **latest version** of the STIG — versions are updated regularly
- Document **why** a control is Not Applicable — vague justifications will be rejected
- For Open findings, include enough detail to support POA&M entry
- Cross-reference findings with **NIST SP 800-53** controls where applicable

---

## Download
[DISA STIG Viewer — official download](https://public.cyber.mil/stigs/srg-stig-tools/)
