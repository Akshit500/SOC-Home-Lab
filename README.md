# 🛡️ SOC Home Lab — Wazuh SIEM | Threat Detection & Log Monitoring

![Wazuh](https://img.shields.io/badge/SIEM-Wazuh-blue?style=for-the-badge)
![Kali](https://img.shields.io/badge/Attacker-Kali_Linux-red?style=for-the-badge)
![Windows](https://img.shields.io/badge/Endpoint-Windows_10-0078D6?style=for-the-badge&logo=windows)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge)
![Platform](https://img.shields.io/badge/Platform-VirtualBox-orange?style=for-the-badge)

> A hands-on Security Operations Center (SOC) home lab simulating real-world threat detection, log monitoring, and attack simulation using open-source tools.

---

## 📌 Project Overview

This project builds a functional SOC environment from scratch, where cyberattacks are generated, monitored, detected, and investigated using SIEM technology. It replicates the core workflow of a real SOC analyst — from configuring log collection to detecting active threats on a dashboard.

**Core skills practiced:**
- Security monitoring & SIEM administration
- Log analysis and Windows Event monitoring
- Incident response and investigation
- Network reconnaissance detection
- Attack simulation (Blue Team perspective)

---

## 🏗️ Lab Architecture

```
┌─────────────────┐         ┌──────────────────────────┐         ┌─────────────────────────┐
│   Kali Linux    │ ──────► │  Windows 10 + Sysmon     │ ──────► │  Ubuntu Server          │
│   (Attacker)    │         │  + Wazuh Agent           │         │  + Wazuh SIEM           │
│                 │         │  (Monitored Endpoint)    │         │  (Log Collection &      │
│  Nmap, Hydra,   │         │                          │         │   Alerting Dashboard)   │
│  Wireshark      │         │                          │         │                         │
└─────────────────┘         └──────────────────────────┘         └─────────────────────────┘
```

All machines run as virtual machines inside **Oracle VM VirtualBox** on an isolated internal network.

---

## 🛠️ Technologies Used

| Tool | Role |
|------|------|
| **Wazuh SIEM** | Central log collection, alerting, and security dashboard |
| **Ubuntu Server 22.04** | Hosts the Wazuh manager |
| **Windows 10** | Monitored endpoint with Wazuh agent installed |
| **Sysmon** | Deep Windows event telemetry (process creation, network connections) |
| **Kali Linux** | Attack simulation machine |
| **Oracle VM VirtualBox** | Hypervisor — hosts all VMs |
| **Nmap** | Port scanning and network reconnaissance |
| **Hydra** | Brute force attack simulation |
| **Wireshark** | Network traffic analysis |

---

## ✅ What I Built

- [x] Installed and configured Oracle VM VirtualBox
- [x] Deployed Ubuntu Server 22.04 VM
- [x] Installed and configured Wazuh SIEM on Ubuntu Server
- [x] Set up Windows 10 VM as a monitored endpoint
- [x] Installed Sysmon on Windows 10 for enhanced event logging
- [x] Enrolled Windows 10 as a Wazuh agent (connected to Wazuh manager)
- [x] Configured centralized log collection (Windows Event Logs + Sysmon)
- [x] Simulated attacks from Kali Linux
- [x] Detected and analyzed alerts on the Wazuh dashboard
- [x] Created custom Wazuh detection rules

---

## ⚔️ Attack Simulations Performed

| Attack | Tool Used | Detection Method |
|--------|-----------|-----------------|
| Brute force login | Hydra | Failed login alerts (Event ID 4625) |
| Port scanning | Nmap | Network reconnaissance detection |
| Suspicious PowerShell execution | Manual | Sysmon + Wazuh rule trigger |
| Malware simulation | EICAR test file | Wazuh file integrity monitoring |
| Failed login detection | Manual | Windows Security Event logs |

---

## 📁 Repository Structure

```
SOC-Home-Lab/
│
├── screenshots/          # Lab screenshots and dashboard captures
├── setup-guide/          # Step-by-step setup documentation
├── attack-simulations/   # Attack commands and methods used
├── detection-rules/      # Custom Wazuh rules created
├── incident-reports/     # Sample incident investigation reports
└── README.md
```

---

## 🔑 Key Windows Event IDs Monitored

| Event ID | Description |
|----------|-------------|
| 4625 | Failed login attempt |
| 4624 | Successful login |
| 4688 | New process created |
| 4672 | Special privileges assigned |
| 1 (Sysmon) | Process creation with full command line |
| 3 (Sysmon) | Network connection detected |

---

## 🧱 Challenges & How I Solved Them

**Problem:** Wazuh installation failed on Ubuntu 24.04 LTS.

**Root cause:** Ubuntu 24.04 is not officially supported by Wazuh at this time.

**Solution:** Migrated to Ubuntu 22.04 LTS (Wazuh's officially supported version). This taught me the importance of checking official documentation for version compatibility before deployment — a skill directly applicable to real SOC environments.

---

## 🚀 Future Improvements

- [ ] Integrate Sigma detection rules
- [ ] Add malware traffic analysis using Wireshark
- [ ] Create automated alert scripts using Python
- [ ] Implement MITRE ATT&CK framework mapping
- [ ] Add threat hunting scenarios
- [ ] Configure email alerting for high-severity events

---

## 📚 Skills Developed

- SIEM deployment and administration (Wazuh)
- Linux system administration (Ubuntu Server)
- Windows endpoint monitoring and Sysmon configuration
- Threat detection and alert triage
- Incident response workflow
- Network security monitoring
- Attack simulation and blue team analysis

---

## 👤 Author

**Akshit Rawat**
- GitHub: [@Akshit500](https://github.com/Akshit500)
- LinkedIn: *[www.linkedin.com/in/akshit-rawat-b01810279]*

---
## ⚠️ Disclaimer
This project was built entirely in an isolated virtual lab environment 
using Oracle VM VirtualBox. All attack simulations were performed only 
on virtual machines I own and control. No real systems, networks, or 
individuals were targeted. This repository is for educational and 
portfolio purposes only. Do not replicate these techniques on any 
system without explicit written permission.

