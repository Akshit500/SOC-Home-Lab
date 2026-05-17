# Brute Force Login Attack Detection

## Overview

A brute-force login attack simulation was performed from the Kali Linux virtual machine against the Windows 10 endpoint to generate failed authentication events and test threat detection capabilities within the SOC home lab.

The objective of this simulation was to:
- Simulate password guessing attacks
- Generate failed login events
- Monitor authentication activity
- Detect suspicious login attempts using Wazuh SIEM
- Investigate generated security alerts



## Attack Scenario

Brute-force attacks are commonly used by attackers to gain unauthorized access by repeatedly attempting different username and password combinations.

This simulation recreates that activity in a controlled lab environment to practice:
- Threat monitoring
- Authentication log analysis
- Alert investigation
- SOC operations


## Environment

| Machine | Role |
|---|---|
| Kali Linux | Attacker |
| Windows 10 | Target Endpoint |
| Ubuntu Server + Wazuh | SIEM Monitoring Server |



## Tools Used

- Hydra
- Kali Linux
- Wazuh SIEM
- Windows 10
- Sysmon



## Attack Execution

### Step 1 — Identify Target IP

Verified the Windows 10 virtual machine IP address.

Example:

```txt
192.168.x.x
```


### Step 2 — Launch Brute Force Attack

Executed the following Hydra command from Kali Linux:

```bash
hydra -l administrator -P rockyou.txt rdp://<target-ip>
```

Example:

```bash
hydra -l administrator -P rockyou.txt rdp://192.168.x.x
```


## What the Attack Does

The Hydra tool attempts multiple password combinations against the target system to simulate unauthorized login attempts.

This generates:
- Failed authentication logs
- Security event entries
- Suspicious login activity


## Detection and Monitoring

The Windows endpoint generated logs related to:
- Failed login attempts
- Authentication failures
- Suspicious account activity

These logs were forwarded to Wazuh through the Wazuh agent for analysis.


## Wazuh Alerts

Wazuh generated alerts related to:
- Multiple failed logins
- Authentication failures
- Potential brute-force activity

Alerts were monitored through the Wazuh dashboard.


## Investigation Process

The following information was analyzed:
- Source IP address
- Target username
- Number of failed login attempts
- Timestamp
- Alert severity
- Associated Windows event logs



## Security Impact

Brute-force attacks are commonly associated with:
- Unauthorized access attempts
- Credential attacks
- Account compromise
- Initial access techniques

Detecting repeated failed logins is important for identifying potential intrusions at an early stage.
