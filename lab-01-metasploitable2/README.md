# Lab 01 — Metasploitable2 Penetration Testing

## Overview

This lab focuses on setting up an isolated penetration testing environment and practicing the fundamental stages of a penetration test against an intentionally vulnerable Metasploitable2 machine.

The assessment covers environment preparation, network reconnaissance, service enumeration, vulnerability identification, and exploitation using the Metasploit Framework.

## Lab Environment

- **Attacker Machine:** Kali Linux
- **Target Machine:** Metasploitable2
- **Virtualization Platform:** VMware Workstation
- **Network Type:** Host-only Network

## Methodology

The following penetration testing stages were performed:

1. Lab Environment Setup
2. Network Discovery
3. Port and Service Enumeration
4. Operating System Fingerprinting
5. Vulnerability Identification
6. Exploitation
7. Post-Exploitation Enumeration

## Key Finding

During service enumeration, the target was identified as running **VSFTPD 2.3.4**, a vulnerable version of the FTP service.

The vulnerability was successfully exploited using the Metasploit Framework, resulting in unauthorized remote access to the target system within the controlled lab environment.

## Tools Used

- Kali Linux
- Nmap
- Metasploit Framework
- Metasploitable2
- VMware Workstation

## Report

The complete penetration testing report, including methodology, commands, screenshots, exploitation steps, and reflections, is available in the PDF report included in this directory.

## ⚠️ Disclaimer

All penetration testing activities documented in this lab were performed in a controlled, isolated, and authorized lab environment for educational purposes only.

The techniques and tools demonstrated here should only be used against systems you own or have explicit authorization to test.