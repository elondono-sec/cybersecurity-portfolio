# Windows Server Vulnerability Assessment & Hardening

**Project Type:** Completed Guided Hands-On Cybersecurity Lab  
**Training Platform:** ACI Learning  
**Focus:** Vulnerability Assessment | Windows Security | Exploitation Validation | Remediation

## Project Overview

This project documents a guided cybersecurity lab involving the identification of security weaknesses in a Windows Server environment, controlled vulnerability exploitation, system hardening, and follow-up security testing.

The exercise was conducted in an authorized educational lab environment using intentionally vulnerable systems.

## Lab Environment & Tools

- Kali Linux — security testing workstation
- Windows Server 2016 — target server
- Nmap — host discovery and service enumeration
- Metasploit Framework — controlled vulnerability validation
- Windows Server administrative tools — security configuration and hardening
- SMB enumeration utilities — identification of Windows network services

## Objectives

1. Identify network services exposed by a Windows Server.
2. Examine security weaknesses associated with SMB and unnecessary services.
3. Demonstrate the potential impact of an exploitable vulnerability in a controlled lab.
4. Apply system-hardening measures to reduce the attack surface.
5. Perform follow-up testing to assess the effect of remediation.

## Methodology

### Phase 1 — Network Reconnaissance

Used Kali Linux and network enumeration tools to identify the Windows Server and examine exposed services.

The exercise included Nmap scanning and SMB service enumeration to understand the target's network-facing attack surface.

### Phase 2 — Vulnerability Assessment

Investigated a Windows SMB security weakness associated with MS17-010.

The guided exercise examined how an unpatched or insecurely configured service can expose a Windows system to unauthorized access.

### Phase 3 — Controlled Exploitation

Followed the authorized lab procedure using Metasploit to demonstrate the security impact of the identified vulnerability.

This activity was limited to the isolated training environment and was not performed against production or third-party systems.

### Phase 4 — Windows Server Hardening

Applied guided security-hardening procedures, including:

- Removing unnecessary IIS and FTP services
- Disabling unnecessary or insecure user accounts
- Reviewing exposed network services
- Reducing unnecessary access and attack paths

### Phase 5 — Post-Hardening Validation

Performed the lab's follow-up security checks to evaluate the hardened system.

The purpose was to compare the server's security exposure before and after configuration changes.

## Security Findings & Lessons Learned

| Security Concern | Potential Impact | Recommended Mitigation |
|---|---|---|
| Vulnerable SMB services | Unauthorized system access or remote code execution | Apply relevant security updates; disable SMBv1 where unnecessary |
| Unnecessary IIS/FTP services | Increased network attack surface | Remove unused server roles and services |
| Insecure or unnecessary accounts | Unauthorized authentication and privilege misuse | Disable unused accounts and enforce least privilege |
| Inadequate remediation verification | Security weaknesses may remain undetected | Rescan and validate security controls after changes |

## Defensive Recommendations

- Maintain an effective Windows Server patch-management process.
- Disable legacy protocols and unnecessary network services.
- Enforce least-privilege access and secure account administration.
- Restrict administrative access through appropriate network controls.
- Conduct regular vulnerability assessments.
- Validate remediation through documented follow-up testing.
- Maintain centralized security logging and monitor suspicious authentication activity.

## Skills Practiced

- Network reconnaissance and service enumeration
- Windows Server vulnerability assessment
- Controlled exploitation in an authorized lab
- Attack-surface reduction
- Windows Server hardening
- Remediation verification
- Technical security documentation

## Evidence & Scope

This project represents a completed guided hands-on ACI Learning exercise. The lab instructions were followed as part of required cybersecurity training.

Original screenshots, scan logs, and command outputs were not retained. Therefore, this report summarizes the lab workflow and security concepts rather than presenting independently preserved test evidence or measured results.

## Conclusion

This exercise provided practical experience with a fundamental vulnerability-management process: discovering exposed services, evaluating security weaknesses, understanding their potential impact, applying defensive controls, and performing follow-up validation.

It reinforced the importance of reducing unnecessary services, maintaining secure Windows configurations, and verifying that remediation efforts address identified risks.

---

**Ethical Use:** All exploitation activities were performed in an authorized educational lab environment.
