# Active Directory - Gaining Shell Access

## Executive Summary
This lab demonstrates obtaining an initial shell on a Windows host within an Active Directory environment after successful network-based attacks. The objective is to establish command execution, validate access, and prepare for post-compromise enumeration.

> **Status:** Completed in Active Directory Home Lab

## Business Scenario
During an internal penetration test, an attacker gains an initial foothold on a domain-joined workstation. This shell becomes the starting point for domain enumeration and later attack stages.

## Objectives
- Gain an interactive shell.
- Validate command execution.
- Enumerate the compromised system.
- Prepare for Active Directory post-compromise activities.

## Lab Environment
- Kali Linux (Attacker)
- Windows Server 2022 (Domain Controller)
- Windows 10 Enterprise Client
- Active Directory Domain

## Tools Used
- Nmap
- Metasploit
- Windows CMD / PowerShell

## Methodology
1. Enumerate the target.
2. Exploit the vulnerable service.
3. Obtain a shell.
4. Verify access with `whoami`.
5. Collect host information using `hostname`, `ipconfig`, and `systeminfo`.
6. Continue with Active Directory enumeration.

## Commands
```powershell
whoami
hostname
ipconfig /all
systeminfo
net user
net localgroup administrators
```

## Attack Flow
Recon → Exploitation → Shell Access → Local Enumeration → AD Enumeration

## Screenshot Placeholders
- Initial Scan
- Exploitation
- Shell Access
- whoami
- hostname
- systeminfo

## MITRE ATT&CK
- T1190 – Exploit Public-Facing Application
- T1059 – Command and Scripting Interpreter
- T1082 – System Information Discovery
- T1033 – System Owner/User Discovery

## Detection
- Monitor suspicious process creation.
- Detect unusual PowerShell/CMD activity.
- Review endpoint telemetry.
- Monitor authentication anomalies.

## Mitigations
- Patch exposed services.
- Restrict unnecessary network access.
- Apply least privilege.
- Enable endpoint monitoring.
- Audit PowerShell usage.

## Lessons Learned
- Initial shell access is the starting point of the engagement.
- Validate privileges before moving laterally.
- Document all commands and findings.

## References
- MITRE ATT&CK
- Microsoft Security Documentation

---
**Part of the Active Directory Home Lab Series**
