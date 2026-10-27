# Enterprise Security Monitoring Architecture

**Project Type:** Academic Cybersecurity Architecture Assessment  
**Course:** Purdue University Global — IN206M5  
**Focus:** Network Security | Security Monitoring | Network Segmentation | Centralized Logging

## Project Overview

This project presents an enterprise security monitoring architecture designed to improve network visibility, protect administrative access, and support security incident detection.

The assessment focused on integrating network segmentation, secure management protocols, centralized logging, and network traffic monitoring into a coordinated security design.

## Project Objectives

- Improve visibility into enterprise network activity.
- Separate systems and services using VLAN segmentation.
- Protect administrative access through a dedicated jump host.
- Secure network device monitoring using SNMPv3.
- Collect network flow telemetry using NetFlow/IPFIX.
- Protect centralized log transmission using TLS.
- Maintain consistent timestamps using NTP.
- Support incident detection, investigation, and auditing.

## Architecture Components

| Component | Security Purpose |
|---|---|
| VLAN segmentation | Separate network functions and reduce unnecessary access |
| SNMPv3 | Provide authenticated and encrypted network device monitoring |
| NetFlow/IPFIX | Collect traffic metadata for visibility and analysis |
| TLS-protected syslog | Protect log data during transmission |
| NTP | Synchronize timestamps across monitored systems |
| Administrative jump host | Centralize and restrict privileged management access |
| Centralized monitoring | Correlate security events across network infrastructure |

## Security Architecture

### 1. Network Segmentation

The architecture uses VLANs to separate network functions and establish logical security boundaries.

Segmentation supports access control, limits unnecessary communication between systems, and can reduce the impact of compromised devices.

### 2. Secure Device Monitoring

SNMPv3 provides authentication and privacy protections for monitoring network devices.

Compared with older SNMP configurations, authenticated and encrypted management traffic helps protect sensitive operational information.

### 3. Network Traffic Visibility

NetFlow/IPFIX provides network flow metadata that can help analysts identify unusual communication patterns, unexpected destinations, and potential lateral movement.

Flow records complement other security telemetry without requiring full packet capture for every connection.

### 4. Centralized Security Logging

TLS-protected syslog supports the secure transmission of system and network event records to a centralized logging platform.

Centralized logs improve investigation, auditing, and correlation across multiple devices.

### 5. Time Synchronization

NTP maintains consistent timestamps across monitored infrastructure.

Accurate timestamps are essential for reconstructing incident timelines and correlating events from different sources.

### 6. Privileged Administrative Access

A dedicated jump host provides a controlled entry point for administrative access.

This approach can reduce direct exposure of management interfaces and support more consistent monitoring of privileged activity.

## Example Monitoring Workflow

1. Network devices generate operational and security events.
2. Syslog messages are transmitted to a centralized logging destination.
3. NetFlow/IPFIX exports provide network traffic metadata.
4. SNMPv3 supports secure device status monitoring.
5. NTP helps align event timestamps across sources.
6. Security personnel correlate the collected information to investigate suspicious activity.

## Security Benefits

| Security Control | Expected Benefit |
|---|---|
| VLAN segmentation | Reduced unnecessary connectivity |
| SNMPv3 | More secure network management |
| NetFlow/IPFIX | Improved traffic visibility |
| TLS syslog | Protected log transmission |
| NTP | More reliable event correlation |
| Jump host | Better control over administrative access |
| Centralized monitoring | Improved detection and investigation capabilities |

## Skills Demonstrated

- Enterprise network security architecture
- Security monitoring design
- Network segmentation concepts
- Secure management protocols
- Network flow telemetry
- Centralized logging architecture
- Administrative access controls
- Security documentation and technical communication

## Project Scope and Evidence

This portfolio entry summarizes an academic architecture assessment.

The proposed design demonstrates security architecture planning and technical reasoning. It should not be interpreted as a fully deployed production monitoring environment or independently validated enterprise implementation.

The original academic assessment included an architecture diagram. The diagram is not reproduced in this repository.

## Conclusion

This project demonstrates how network segmentation, secure management, traffic telemetry, centralized logging, and controlled administrative access can work together to strengthen enterprise security monitoring.

The architecture reflects skills relevant to Security Operations Center (SOC) analysis, network security, vulnerability management, and security engineering.

---

**Portfolio Note:** Prepared as part of Purdue University Global cybersecurity coursework.
