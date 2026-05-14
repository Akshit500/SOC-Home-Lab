 Windows 10 Virtual Machine Installation

## Overview

A Windows 10 virtual machine was created in Oracle VM VirtualBox to act as the target system within the SOC home lab environment.

The Windows machine will be used for:
- Log generation
- Sysmon event monitoring
- Attack simulations
- Wazuh agent integration
- Threat detection testing



## Why Windows 10?

Windows 10 was selected because:
- It is widely used in enterprise environments
- Most security incidents target Windows systems
- Sysmon provides advanced Windows logging capabilities
- Wazuh supports Windows event monitoring


## Virtual Machine Configuration

| Component | Configuration |
|---|---|
| Operating System | Windows 10 Pro |
| RAM | 4 GB |
| CPU | 2 Cores |
| Storage | 50 GB |
| Network Adapter | Host-Only Adapter |



## Installation Steps

### Step 1 — Download Windows 10 ISO

Downloaded the Windows 10 ISO file from the official Microsoft website.



### Step 2 — Create Virtual Machine

Created a new Windows 10 virtual machine in Oracle VM VirtualBox.

### Step 3 — Configure Resources

Allocated:
- RAM
- CPU cores
- Storage space

Configured networking using Host-Only Adapter mode.


### Step 4 — Attach ISO File

Attached the Windows 10 ISO file through VirtualBox storage settings.


### Step 5 — Install Windows 10

Installed Windows 10 using the standard installation process.

Configured:
- Username
- Password
- System settings


### Step 6 — Install VirtualBox Guest Additions

Installed Guest Additions to improve:
- Display resolution
- Performance
- Clipboard functionality
- Fullscreen support
