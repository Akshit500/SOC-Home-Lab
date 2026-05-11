# SOC-Home-Lab

A hands-on cybersecurity SOC (Security Operation Center) home lab project build using wazuh , kali linux , windows 10 ,sysmon and virtual box for threat detection ,log monitoring ,attack simulation and incident analysis .

## Project Overview

This project simulates a real world SOC environment where cyberattcks are generated ,monitored ,detected , and investigated using SIEM technology  and security monitoring tools .
The lab is designed to strenghten practical cybersecurity skills in :
*Security Monitoring 
*SIEM Managemnt 
* log analysis
* incident response
* windows event analysis
* Network reconnaissance detection

 ## Lab Architecture
 
  Kali Linux (Attacker)
  ↓
  Windows 10 + Sysmon + Wazuh Agent
  ↓
  Ububtu Servers + Wazuh SIEM
  ↓
  Security Alerts & Monitoring Dashboard

 ## Technologies used
  
  * Wazuh SIEM
  * Kali Linux
  * Windows 10
  * Ubuntu Server
  * Sysmon
  * Oracle VM Virtualbox
  * Nmap
  * Hydra
  * Wireshark

## Project Objective

  * Build in functional SOC monitoring enviornment
  * Configure centralized log collection
  * Simulate cyber attacks saftely in a lab
  * Detect suspicious activities and threats
  * Analyze security events and alerts
  * Create incident reports and detection rules

## Planned Attack Simulation 

* Brute force login attack
* Nmap port scanning
* Suspicious powershell execution
* Malware simulation using EICAR
* Failed login detectiion

## Planned Features 

* Centralized log monitoring 
* Customm Wazuh detection rules
* Sysmon Event callection
* Threat detection dashboard
* Incident investigation report
* MITRE ATT&CK mapping
* Python log analysis scripts

## Repository Structure 

SOC-home-lab/
|
|-architecture/
|-screenshots/
|-setup-guide/
|-attack-simulation/
|-detection-rules/
|-incident-report/
|-scripts/

## Current Progress

* Installed Oracle VM Virtual box
* Downloaded ubuntu server ISO
* Created Ubuntu Server VM
* Installed Wazuh SIEM
* Configured Windows 10 VM
* Installed Sysmon
* Connected Wazuh Agent
* Simulated Attack
* Created custom detection rules

## Why This Project 

This lab is designed to provide practical hands-on SOC analyst experience by simulating real-world cyber attack and monitoring them using SIEM technology 

THe project focuses on :
* Threat detection
* Log Analysis
* Security monitoring
* Incident investigation
* Attack simulation
* Blue team operations

## Future Improvements 

* Integrate sigma detection rule
* add malware traffic analysis using wireshark
* Create automated alert scripts using python
* Implement MITRE ATT&CK-based detection
* Add threat hunting scenarios
* Configure email alerting

## Skills Being developed 

* SIEM Administration
* Linux system Administration
* Windows Event montoring
* Threat detection
* Incident Response
* Network security monitoring
* Security Operations Center (SOC) Workflow
  
## Author
Akshit Rawat
