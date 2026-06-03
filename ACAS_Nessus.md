# ACAS / Nessus Vulnerability Scanner

## Overview
The Assured Compliance Assessment Solution (ACAS) is the DoD enterprise vulnerability scanning solution built on Tenable's Nessus and Security Center platforms. ACAS is used across DoD to identify vulnerabilities, misconfigurations, and compliance gaps across networks and systems.

---

## ACAS Components

| Component | Purpose |
|-----------|---------|
| Tenable Security Center | Centralized management console for scan management and reporting |
| Nessus Scanner | Active scanning engine that probes target systems for vulnerabilities |
| Nessus Network Monitor (NNM) | Passive monitoring of network traffic for vulnerability identification |

---

## Key Capabilities
- Network-wide vulnerability scanning
- STIG and compliance benchmark scanning
- Credentialed and non-credentialed scan modes
- CVE-based vulnerability identification and CVSS scoring
- Integration with SIEM platforms for continuous monitoring
- Detailed remediation guidance per finding

---

## Scan Types

| Scan Type | Description |
|-----------|-------------|
| Credentialed Scan | Uses system credentials for deep inspection — more accurate results |
| Non-Credentialed Scan | External probe without login — identifies exposed vulnerabilities only |
| Compliance Scan | Checks system configuration against STIG or CIS benchmarks |
| Discovery Scan | Identifies active hosts and open ports on the network |

---

## ACAS Workflow

```
Define scan policy and targets in Security Center
        ↓
Run credentialed vulnerability scan against target systems
        ↓
Review scan results — filter by severity (Critical, High, Medium, Low)
        ↓
Cross-reference findings with applicable STIGs
        ↓
Initiate remediation for critical and high findings
        ↓
Rescan to verify remediation effectiveness
        ↓
Export report for RMF documentation and continuous monitoring records
```

---

## Understanding CVSS Scores

| CVSS Score | Severity | Priority |
|------------|----------|---------|
| 9.0 – 10.0 | Critical | Immediate remediation required |
| 7.0 – 8.9  | High     | Remediate within 30 days |
| 4.0 – 6.9  | Medium   | Remediate within 90 days |
| 0.1 – 3.9  | Low      | Remediate within 180 days or accept risk |

---

## Tips for Assessors
- Always run **credentialed scans** when possible — uncredentialed scans miss the majority of findings
- Schedule regular scans as part of your **Continuous Monitoring Strategy**
- Document scan results and retain reports as part of your RMF package
- Use ACAS findings to prioritize remediation efforts alongside STIG findings
- Correlate ACAS CVEs with STIG Vuln IDs where applicable for comprehensive reporting

---

## References
- [DoD ACAS Program](https://www.disa.mil/cybersecurity/network-defense/acas)
- [Tenable Nessus Documentation](https://docs.tenable.com/nessus)
