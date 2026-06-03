# Common CAT II & III STIG Findings

---

# CAT II — Medium Severity Findings

CAT II findings represent elevated risk vulnerabilities that should be remediated promptly. They are common in STIG assessments and frequently appear in RMF POA&M packages.

---

## Finding 1: Password Complexity Not Enforced

**Severity:** CAT II  
**NIST 800-53 Control:** IA-5 (Authenticator Management)

### Description
The system does not enforce password complexity requirements such as minimum length, character variety, or expiration policies. Weak passwords are easily compromised through brute force or dictionary attacks.

### Remediation
- Configure password policy to require minimum 15 characters
- Enforce complexity (uppercase, lowercase, numbers, special characters)
- Set maximum password age per DoD policy (typically 60 days)
- Prevent reuse of last 24 passwords

---

## Finding 2: Session Timeout Not Configured

**Severity:** CAT II  
**NIST 800-53 Control:** AC-11 (Session Lock)

### Description
The system does not automatically lock or terminate idle sessions after a defined period of inactivity. Unattended sessions can be exploited by unauthorized users with physical or remote access.

### Remediation
- Configure session timeout to 15 minutes of inactivity
- Require reauthentication to resume a locked session
- Apply setting to all access methods (console, remote, web)

---

## Finding 3: System Not Patched to Current Level

**Severity:** CAT II  
**NIST 800-53 Control:** SI-2 (Flaw Remediation)

### Description
The system has missing security patches or updates, leaving known vulnerabilities unaddressed. Unpatched systems are a primary attack vector in both targeted and automated attacks.

### Remediation
- Identify all missing patches using ACAS or WSUS/SCCM
- Apply critical and high patches within 30 days per DoD policy
- Document patching activity and rescan to verify
- Establish a recurring patch management cycle

---

## Finding 4: Unnecessary Services Running

**Severity:** CAT II  
**NIST 800-53 Control:** CM-7 (Least Functionality)

### Description
The system is running services, ports, or protocols that are not required for its operational function. Unnecessary services increase the attack surface and may introduce unknown vulnerabilities.

### Remediation
- Audit all running services and open ports
- Disable or remove services not required for system function
- Document approved services in the System Security Plan
- Rescan to verify unnecessary services are no longer active

---

## Finding 5: Antivirus Not Updated

**Severity:** CAT II  
**NIST 800-53 Control:** SI-3 (Malicious Code Protection)

### Description
Antivirus software is installed but definitions are outdated, reducing effectiveness against current malware threats.

### Remediation
- Update antivirus definitions to current version
- Configure automatic updates for definition files
- Verify antivirus is actively scanning and reporting to centralized management console

---

# CAT III — Low Severity Findings

CAT III findings carry lower immediate risk but should be tracked and remediated to maintain a strong security posture and avoid accumulation of low-level vulnerabilities.

---

## Finding 1: Security Banners Not Displayed

**Severity:** CAT III  
**NIST 800-53 Control:** AC-8 (System Use Notification)

### Description
The system does not display a DoD-approved warning banner at login. Banners establish legal notice of monitoring and are required on all DoD systems.

### Remediation
- Configure login banner with DoD-approved text
- Apply to all access methods — console, SSH, web portals
- Verify banner displays before authentication prompt

---

## Finding 2: System Documentation Not Current

**Severity:** CAT III  
**NIST 800-53 Control:** PL-2 (System Security Plan)

### Description
System documentation including the System Security Plan (SSP), network diagrams, or hardware/software inventory is outdated or incomplete.

### Remediation
- Review and update all system documentation
- Ensure SSP reflects current system architecture and configurations
- Establish a documentation review cycle aligned with system changes

---

## Finding 3: Account Review Not Performed

**Severity:** CAT III  
**NIST 800-53 Control:** AC-2 (Account Management)

### Description
User accounts have not been reviewed on a regular schedule to verify they are still required and appropriately privileged.

### Remediation
- Conduct immediate account audit
- Remove or disable accounts for separated personnel
- Establish quarterly account review process
- Document review process in SSP

---

*Reference: [DISA STIG Library](https://public.cyber.mil/stigs/) | [NIST SP 800-53 Rev 5](https://csrc.nist.gov/publications/detail/sp/800-53/rev-5/final)*
