# Linux Server Compromise: Digital Forensic Investigation

**Project Type:** Completed Guided Hands-On Cybersecurity Lab  
**Training Platform:** ACI Learning  
**Focus:** Digital Forensics | Incident Response | Linux Security | Evidence Analysis

## Project Overview

This project documents a guided forensic investigation of a compromised Linux server using Autopsy and a provided forensic disk image.

The investigation focused on examining Linux system artifacts to reconstruct suspicious activity, identify evidence of unauthorized access, and understand the potential impact of a server compromise.

All work was conducted within an authorized educational lab environment.

## Lab Environment and Tools

- **Autopsy:** Digital forensic examination and artifact analysis
- **FTK Imager:** Forensic imaging and disk-image handling
- **Linux forensic image:** Provided evidence source
- **Linux system logs:** Authentication and system activity analysis
- **Apache web server logs:** Investigation of web-related activity
- **VirusTotal:** Malware reputation and file analysis

## Investigation Objectives

1. Examine a Linux forensic disk image.
2. Identify evidence of suspicious SSH authentication activity.
3. Investigate unauthorized user accounts and privilege levels.
4. Review command history to reconstruct attacker behavior.
5. Examine suspicious files and potential malware artifacts.
6. Identify evidence of web server compromise and possible data exposure.
7. Recommend defensive controls and incident response measures.

## Investigation Methodology

### Phase 1 — Evidence Examination

Followed the guided forensic workflow to examine the provided Linux disk image.

Used Autopsy to navigate the filesystem, identify relevant directories, and inspect evidence artifacts.

The exercise demonstrated the importance of preserving evidence integrity and documenting investigative findings.

### Phase 2 — Authentication Log Analysis

Examined Linux authentication records, including `/var/log/auth.log`, for indications of unauthorized SSH activity.

The investigation focused on distinguishing failed authentication attempts from successful access and examining associated account activity.

### Phase 3 — Unauthorized Account Investigation

Reviewed Linux account information to identify the suspicious `toor` account.

The lab demonstrated the significance of a user account with UID 0, which provides root-equivalent privileges.

This reinforced the importance of auditing privileged accounts and investigating unexpected changes to user databases.

### Phase 4 — Command History Analysis

Examined shell history artifacts, including `.bash_history`, to understand actions associated with the compromised account.

The guided investigation addressed suspicious command execution, changes to website content, and activity associated with credential exposure.

### Phase 5 — Suspicious File and Malware Analysis

Investigated the suspicious executable `shell.elf` and the role of file-reputation analysis in malware triage.

The exercise demonstrated how suspicious files can be correlated with authentication events and command history to reconstruct an intrusion.

### Phase 6 — Web Server Artifact Examination

Reviewed Apache-related artifacts to investigate website defacement and potential exposure of sensitive information.

This phase connected host-level forensic evidence with activity affecting a web-facing service.

## Investigative Findings

The training scenario illustrated the following indicators of compromise:

| Evidence Artifact | Security Significance |
|---|---|
| SSH authentication records | Possible unauthorized remote access |
| `toor` account with UID 0 | Unauthorized root-equivalent account and persistence risk |
| Shell command history | Evidence supporting reconstruction of attacker actions |
| `shell.elf` executable | Suspicious downloaded file requiring further analysis |
| Modified web content | Potential website defacement |
| Apache server artifacts | Additional context for web-related compromise and data exposure |

These findings reflect the guided lab scenario. Original screenshots, extracted logs, and independent forensic reports were not retained for this portfolio.

## Incident Response and Remediation Recommendations

### Containment
- Isolate affected systems when appropriate.
- Restrict unauthorized SSH access.
- Preserve forensic evidence before destructive changes.

### Eradication and Recovery
- Investigate and remove unauthorized privileged accounts.
- Rotate potentially exposed credentials.
- Analyze suspicious executables before removal.
- Restore altered web content from verified backups.
- Patch vulnerable software and review exposed services.

### Prevention and Detection
- Enforce least privilege and regularly audit UID 0 accounts.
- Use SSH key-based authentication and restrict administrative logins.
- Centralize authentication and web server logging.
- Monitor suspicious account creation and privileged command execution.
- Implement file integrity monitoring and appropriate endpoint protections.

## Skills Demonstrated

- Linux filesystem artifact examination
- Digital forensic investigation using Autopsy
- Authentication and SSH log analysis
- Privileged-account investigation
- Shell history examination
- Suspicious-file triage
- Incident timeline reconstruction
- Security findings documentation
- Incident response and remediation planning

## Evidence and Scope

This project represents a completed guided hands-on ACI Learning digital forensics exercise.

The investigation was performed using a provided training scenario and forensic evidence. The original lab screenshots, extracted artifacts, and command outputs were not retained.

Accordingly, this report documents the investigative workflow, scenario-based findings, and security lessons without claiming an independently verified forensic examination of a real-world incident.

## Conclusion

This investigation provided practical experience examining Linux forensic artifacts and understanding how multiple evidence sources can be combined to reconstruct unauthorized activity.

It reinforced the importance of authentication monitoring, privileged-account controls, evidence preservation, incident response, and secure Linux system administration.

---

**Ethical Use:** All investigative activities were performed within an authorized educational training environment.
