# Sysmon Installation and Configuration

## Overview

Sysmon (System Monitor) was installed on the Windows 10 virtual machine to provide advanced system activity logging for threat detection and security monitoring.

Sysmon enhances Windows event logging by recording detailed information about:
- Process creation
- Network connections
- PowerShell execution
- File modifications
- Process hashes
- System activity

These logs will later be collected and analyzed using Wazuh SIEM.

## Why Sysmon?

Default Windows logs provide limited visibility into system activity.

Sysmon improves monitoring capabilities by generating detailed telemetry useful for:
- Threat detection
- Malware analysis
- Incident investigation
- Suspicious activity monitoring
- SOC operations

## Tools Used

- Sysmon
- Windows 10
- PowerShell
- Oracle VM VirtualBox

## Installation Steps

### Step 1 — Download Sysmon

Downloaded Sysmon from the Microsoft Sysinternals website.


### Step 2 — Extract Files

Extracted the Sysmon package on the Windows 10 virtual machine.


### Step 3 — Open PowerShell as Administrator

Launched PowerShell with administrative privileges.


### Step 4 — Install Sysmon

Executed the installation command:

```powershell
sysmon64.exe -i

