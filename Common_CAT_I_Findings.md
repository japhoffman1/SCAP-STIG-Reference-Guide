# Common CAT I — Critical STIG Findings

CAT I findings represent the most severe vulnerabilities in a STIG assessment. These must be remediated immediately or formally accepted via a POA&M with Authorizing Official (AO) approval. CAT I findings can prevent an ATO from being granted.

---

## Finding 1: Default Passwords Not Changed

**Severity:** CAT I  
**Applicable STIGs:** General OS, Network Devices, Applications  
**NIST 800-53 Control:** IA-5 (Authenticator Management)

### Description
Default vendor-supplied passwords have not been changed on one or more system accounts or services. Default credentials are publicly known and are among the first vectors exploited by attackers.

### Remediation
- Identify all accounts using default credentials
- Immediately change all default passwords to complex, unique values meeting DoD password policy
- Disable or remove default accounts that are not operationally required
- Document changes in system configuration records

---

## Finding 2: Multifactor Authentication Not Enforced

**Severity:** CAT I  
**Applicable STIGs:** General OS, Applications, Network Devices  
**NIST 800-53 Control:** IA-2 (Identification and Authentication)

### Description
The system does not enforce multifactor authentication (MFA) for user or privileged access. Single-factor authentication significantly increases the risk of unauthorized access through credential theft or brute force.

### Remediation
- Deploy an approved MFA solution
- Enforce MFA for all user accounts, with priority on privileged accounts
- Test MFA across all access methods (local, remote, web)
- Document MFA configuration in the SSP

---

## Finding 3: Unencrypted Data Transmission

**Severity:** CAT I  
**Applicable STIGs:** General OS, Web Servers, Applications  
**NIST 800-53 Control:** SC-8 (Transmission Confidentiality and Integrity)

### Description
The system transmits sensitive data over unencrypted channels (e.g., HTTP, Telnet, FTP). Unencrypted transmission exposes data to interception and man-in-the-middle attacks.

### Remediation
- Disable unencrypted protocols (Telnet, FTP, HTTP)
- Enforce use of encrypted alternatives (SSH, SFTP, HTTPS)
- Verify encryption is enforced through firewall rules or application configuration
- Conduct a follow-up scan to confirm unencrypted services are no longer active

---

## Finding 4: Audit Logging Not Enabled

**Severity:** CAT I  
**Applicable STIGs:** General OS, Databases, Applications  
**NIST 800-53 Control:** AU-2 (Event Logging), AU-12 (Audit Record Generation)

### Description
The system does not have audit logging enabled or configured to capture required security events. Without audit logs, security incidents cannot be detected, investigated, or responded to effectively.

### Remediation
- Enable audit logging for all required event types per STIG guidance
- Configure log forwarding to a centralized SIEM or log management platform
- Verify log retention meets DoD requirements (minimum 1 year)
- Test logging by generating sample events and confirming capture

---

## Finding 5: Privileged Access Not Restricted

**Severity:** CAT I  
**Applicable STIGs:** General OS, Databases, Applications  
**NIST 800-53 Control:** AC-6 (Least Privilege)

### Description
Administrative or privileged access is not restricted to authorized personnel or is granted more broadly than operationally required. Excessive privilege increases the blast radius of a compromised account.

### Remediation
- Audit all privileged accounts and remove unnecessary privileges
- Implement role-based access control (RBAC) aligned to job functions
- Separate privileged accounts from standard user accounts
- Review privileged access on a quarterly basis and document in SSP

---

*Reference: [DISA STIG Library](https://public.cyber.mil/stigs/) | [NIST SP 800-53 Rev 5](https://csrc.nist.gov/publications/detail/sp/800-53/rev-5/final)*
