# Wazuh Agent Installation and Configuration

## Overview

The Wazuh agent was installed on the Windows 10 virtual machine to enable communication between the endpoint and the Wazuh SIEM server.

The agent is responsible for:
- Collecting Windows event logs
- Forwarding security events
- Monitoring endpoint activity
- Sending telemetry to the Wazuh server

This integration allows centralized monitoring and threat detection within the SOC home lab environment.

## Why Wazuh Agent?

The Wazuh agent enables endpoint visibility by forwarding logs and system activity to the Wazuh server for analysis.

It plays a critical role in:
- Security monitoring
- Threat detection
- Incident analysis
- Centralized logging
- SOC operations

## Environment Configuration

| Component | Details |
|---|---|
| Endpoint | Windows 10 VM |
| SIEM Server | Ubuntu Server + Wazuh |
| Network Mode | Host-Only Adapter |
## Installation Steps

### Step 1 — Download Wazuh Agent

Downloaded the Wazuh Windows agent from the official Wazuh website.


### Step 2 — Run Installer

Executed the Wazuh agent installer on the Windows 10 virtual machine.


### Step 3 — Configure Wazuh Server IP

Entered the Wazuh server IP address during installation.

### Step 4 — Complete Installation

Completed the installation process and configured the agent service.

### Step 5 — Start Wazuh Service

Started the Wazuh agent service using:

```powershell
NET START WazuhSvc
```

