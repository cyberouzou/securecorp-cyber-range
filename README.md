
# SecureCorp Cyber Range – Enterprise Security Lab

## Overview

SecureCorp Cyber Range is a fully virtualized enterprise IT infrastructure designed for cybersecurity training, system administration practice, and attack/defense simulation.

The environment replicates a small-to-medium enterprise (SME) network using Proxmox virtualization, integrating Active Directory, network segmentation, security monitoring, and controlled attack scenarios.

The goal of this project is to demonstrate real-world skills in system administration, network engineering, and cybersecurity operations (SOC/Blue Team/Red Team basics).

---

## Objectives

- Build a complete enterprise-like IT infrastructure
- Implement secure network segmentation using VLANs
- Deploy a full Active Directory environment
- Configure centralized authentication and DNS/DHCP services
- Simulate cyberattacks in a controlled environment
- Implement detection and defense mechanisms
- Centralize logs and security events
- Apply hardening techniques on Windows and Linux systems

---

## Architecture

The infrastructure is based on Proxmox VE and segmented into multiple VLANs:

- Administration Network (VLAN 10)
- Server Network (VLAN 20)
- DMZ (VLAN 30)
- Attack Lab (VLAN 40)
- VPN Network (VLAN 50)

Core components:

- pfSense (Firewall, Routing, VPN, IDS/IPS)
- Windows Server (Active Directory, DNS, DHCP)
- Windows 11 (Domain-joined client)
- Ubuntu Server (Web services, logging)
- Wazuh (SIEM & monitoring)
- Suricata (Network IDS/IPS)
- Kali Linux (Attack simulation)

---

## Network Design

Internet
|
pfSense Firewall
|
| VLAN 10 | VLAN 20 | VLAN 30 | VLAN 40 | VLAN 50
| Admin | Servers | DMZ | Attacker| VPN


---

## Technologies Used

- Proxmox VE
- pfSense
- Windows Server 2022
- Active Directory Domain Services
- DNS / DHCP
- Windows 11
- Ubuntu Server
- Apache2
- Wazuh SIEM
- Suricata IDS/IPS
- Syslog (rsyslog)
- WireGuard VPN
- Kali Linux

---

## Security Features

- Network segmentation via VLANs
- Firewall rules (pfSense)
- Intrusion Detection System (Suricata)
- Security Information and Event Management (Wazuh)
- Centralized logging (Syslog)
- VPN remote access (WireGuard)
- Active Directory security policies (GPO)
- Linux hardening (Fail2Ban, SSH security)
- Windows hardening policies

---

## Attack Simulations

The environment includes controlled offensive security scenarios:

- Network scanning (Nmap)
- Brute-force attacks (Hydra)
- Active Directory enumeration (BloodHound)
- AD security auditing (PingCastle)
- Unauthorized access attempts
- Lateral movement simulation

---

## Defensive Mechanisms

- Firewall filtering and segmentation
- IDS/IPS alerting (Suricata)
- Log analysis and correlation (Wazuh)
- Account lockout policies
- GPO security restrictions
- Service hardening (SSH, SMB, RDP)

---

## Deployment Steps (Simplified)

1. Deploy Proxmox VE hypervisor
2. Configure pfSense firewall and VLANs
3. Install Windows Server and promote to Domain Controller
4. Configure DNS and DHCP services
5. Deploy Windows 11 client and join domain
6. Deploy Ubuntu server (web + logging)
7. Install Wazuh SIEM and agents
8. Configure Suricata IDS on pfSense
9. Enable WireGuard VPN access
10. Deploy Kali Linux for testing

---

## Screenshots

This repository includes:

- Network topology (Proxmox & VLANs)
- Active Directory structure
- GPO configuration
- Firewall rules (pfSense)
- Wazuh dashboards
- Suricata alerts
- Attack simulations results
- Log analysis examples

---

## Skills Demonstrated

- Windows Server Administration
- Active Directory Management
- Network Engineering (VLAN, routing, firewall)
- Cybersecurity operations (SOC fundamentals)
- IDS/IPS configuration
- SIEM monitoring and log analysis
- Linux system administration
- Infrastructure documentation
- Incident detection and response

---

## Author

Alem Aksil, Student in BTS SIO – SISR at Lycée Turgot in Paris
Specialization: Systems, Networks, Cybersecurity

Project carried out in a virtualized environment for educational purposes.

---

## Disclaimer

This project is strictly for educational and training purposes in a controlled environment.
No real-world systems are targeted.
