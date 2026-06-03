# STIG Compliance Checklist

**System Name:** [Enter System Name]  
**System Owner:** [Enter System Owner]  
**Assessment Date:** [Enter Date]  
**Assessed By:** [Enter Name]  
**STIG Version:** General / Generic  
**RMF Package Status:** [Pre-ATO / IATO / ATO]  

---

## Summary Dashboard

| Category | Total Controls | Closed | Open | In Progress | Not Applicable | Findings |
|----------|---------------|--------|------|-------------|----------------|----------|
| CAT I    | 5             | 3      | 1    | 0           | 1              | 1        |
| CAT II   | 10            | 6      | 2    | 1           | 1              | 2        |
| CAT III  | 5             | 4      | 0    | 0           | 1              | 1        |
| **Total**| **20**        | **13** | **3**| **1**       | **3**          | **4**    |

---

## CAT I — Critical Controls

| Control ID | Control Title | Status | Notes |
|------------|--------------|--------|-------|
| V-001      | Default Passwords Must Be Changed | ✅ Closed | All default credentials removed and replaced with complex passwords |
| V-002      | Unnecessary Services Must Be Disabled | ✅ Closed | Non-essential services identified and disabled during initial hardening |
| V-003      | System Must Use Multifactor Authentication | ❌ Open | MFA not yet configured — remediation required before ATO |
| V-004      | Audit Logging Must Be Enabled | ✅ Closed | Audit logging enabled and verified; logs forwarded to SIEM |
| V-005      | Remote Access Must Be Encrypted | 🔵 Not Applicable | System does not support remote access in current configuration |

---

## CAT II — Medium Controls

| Control ID | Control Title | Status | Notes |
|------------|--------------|--------|-------|
| V-006      | Session Timeout Must Be Configured | ✅ Closed | Session timeout set to 15 minutes per policy |
| V-007      | Password Complexity Requirements Must Be Enforced | ✅ Closed | Password policy enforced via group policy settings |
| V-008      | System Must Be Patched to Current Level | ⚠️ In Progress | Patch cycle in progress; estimated completion within 30 days |
| V-009      | Unnecessary User Accounts Must Be Removed | 🟡 Finding | Two dormant accounts identified — see CAT_II_Findings.md |
| V-010      | File Permissions Must Be Restricted | ✅ Closed | File permission audit completed; permissions tightened |
| V-011      | Antivirus Must Be Installed and Updated | ✅ Closed | Antivirus active, definitions current as of assessment date |
| V-012      | System Firewall Must Be Enabled | ✅ Closed | Host-based firewall enabled and rules reviewed |
| V-013      | Network Traffic Must Be Monitored | 🟡 Finding | SIEM integration incomplete — see CAT_II_Findings.md |
| V-014      | Data at Rest Must Be Encrypted | ❌ Open | Encryption not implemented on all data stores — remediation required |
| V-015      | System Banners Must Be Displayed | 🔵 Not Applicable | System operates in isolated environment without login banner requirement |

---

## CAT III — Low Controls

| Control ID | Control Title | Status | Notes |
|------------|--------------|--------|-------|
| V-016      | System Documentation Must Be Maintained | ✅ Closed | System security plan (SSP) and network diagrams current |
| V-017      | Security Awareness Training Must Be Current | ✅ Closed | All users current on annual security awareness training |
| V-018      | Backup Procedures Must Be Documented | ✅ Closed | Backup and recovery procedures documented and tested |
| V-019      | Physical Security Controls Must Be In Place | 🟡 Finding | Server room access log review identified gap — see CAT_III_Findings.md |
| V-020      | Configuration Management Must Be Maintained | 🔵 Not Applicable | System under decommission; CM process not applicable |

---

## Remediation Plan

| Control ID | Category | Remediation Action | Responsible Party | Target Date |
|------------|----------|--------------------|-------------------|-------------|
| V-003      | CAT I    | Configure and test MFA solution | System Admin | [Date] |
| V-008      | CAT II   | Complete patching cycle and verify | Patch Manager | [Date] |
| V-009      | CAT II   | Disable or remove dormant accounts | System Admin | [Date] |
| V-013      | CAT II   | Complete SIEM integration and test | Security Engineer | [Date] |
| V-014      | CAT II   | Implement encryption on remaining data stores | Security Engineer | [Date] |
| V-019      | CAT III  | Update physical access procedures and log review process | Facility Manager | [Date] |

---

*Last Updated: [Enter Date] | Next Review: [Enter Date]*
