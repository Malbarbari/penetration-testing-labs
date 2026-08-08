# Lab 04 – Web Application Penetration Test (LazySysAdmin)

## Overview

This lab documents a penetration test performed against the **LazySysAdmin** Linux VM in a controlled educational environment.

The objective was to identify exposed services, discover security weaknesses, gain access to the web application, obtain a shell, and escalate privileges to **root**.

## Main Steps

- Performed reconnaissance and service enumeration.
- Enumerated SMB shares and discovered sensitive files.
- Identified exposed credentials and WordPress configuration data.
- Accessed phpMyAdmin and WordPress administrative functionality.
- Obtained remote code execution and a shell as `www-data`.
- Reused discovered credentials to access the `togie` account.
- Enumerated sudo permissions and escalated privileges to `root`.

## Key Findings

### Anonymous SMB Access
The SMB service allowed anonymous access to the `share$` directory, exposing sensitive files and application data.

**Severity:** Medium

### Credential Disclosure
Weak and hardcoded credentials were discovered in exposed files, including WordPress configuration data.

**Severity:** High

### Unauthorized Web Application Access
The exposed credentials enabled access to administrative web services and the WordPress database.

**Severity:** High

### Remote Code Execution
Administrative access was leveraged to execute a PHP payload and obtain a shell on the target system.

**Severity:** Critical

### Privilege Escalation
The local user `togie` had excessive sudo permissions, allowing escalation to:

```text
uid=0(root)
```

**Severity:** Critical

## Security Impact

The identified vulnerabilities affected:

- **Confidentiality:** Sensitive credentials and files were exposed.
- **Integrity:** Administrative and system-level modifications were possible.
- **Availability:** Root access could allow disruption of system services.

## Recommendations

- Disable anonymous SMB access.
- Remove plaintext and hardcoded credentials.
- Use strong and unique passwords.
- Restrict access to phpMyAdmin and administrative interfaces.
- Apply least privilege to users and sudo permissions.
- Keep WordPress, plugins, themes, and system packages updated.

## Tools Used

- Nmap
- Netdiscover
- smbclient
- phpMyAdmin
- WordPress
- Metasploit Framework
- msfvenom
- curl

## Disclaimer

This project was completed strictly in a **controlled and authorized educational lab environment**.

## Author

**Mohammad Ali**  
Cybersecurity Student
