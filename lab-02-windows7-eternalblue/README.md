# Lab 02 — Windows 7 Enterprise Penetration Test

## Overview

This lab documents a penetration testing assessment conducted against a legacy Windows 7 Enterprise system in an isolated and authorized lab environment.

The assessment followed a structured penetration testing methodology, including host discovery, network reconnaissance, service enumeration, vulnerability analysis, exploitation, and post-exploitation.

## Lab Environment

- **Attacker Machine:** Kali Linux
- **Target Machine:** Windows 7 Enterprise SP1
- **Virtualization Platform:** VMware Workstation
- **Network Type:** Host-only Network

## Methodology

The following penetration testing stages were performed:

1. Host Discovery
2. Full TCP Port Scanning
3. Service and OS Fingerprinting
4. Manual Service Enumeration
5. SMB Protocol Analysis
6. Vulnerability Assessment
7. Exploitation
8. Post-Exploitation
9. Security Recommendations

## Key Finding

The assessment identified the target as running the legacy **SMBv1** protocol and confirmed exposure to the **MS17-010** vulnerability, commonly known as **EternalBlue**.

Successful exploitation in the controlled lab environment resulted in remote code execution and SYSTEM-level access to the target machine, demonstrating the critical security risks associated with outdated and unpatched systems.

## Vulnerability

| Vulnerability | Severity | Impact |
|---|---|---|
| MS17-010 (EternalBlue) | Critical | Remote Code Execution |
| Weak Credential Management | High | Credential Compromise |
| Legacy SMBv1 Protocol | High | Increased Attack Surface |

## Tools Used

- Kali Linux
- Nmap
- Metasploit Framework
- Meterpreter
- SearchSploit / ExploitDB
- SMBClient
- RPCClient
- NetExec
- VMware Workstation

## Recommendations

- Decommission unsupported legacy operating systems.
- Apply all relevant security patches and updates.
- Disable SMBv1 where it is not explicitly required.
- Enforce strong password policies.
- Restrict administrative access.
- Implement network segmentation for legacy systems.

## Report

The complete penetration testing report, including reconnaissance results, vulnerability analysis, proof of concept, screenshots, post-exploitation findings, and remediation recommendations, is available in the PDF report included in this directory.

## ⚠️ Disclaimer

All penetration testing activities documented in this lab were performed in a controlled, isolated, and authorized lab environment for educational purposes only.

The techniques and tools demonstrated here should only be used against systems you own or have explicit authorization to test.