# Wazuh SIEM Setup Guide

## Environment
- Hypervisor: Oracle VM VirtualBox
- Wazuh Server OS: Ubuntu Server 22.04 LTS
- Endpoint: Windows 10
- Attacker: Kali Linux

## Step 1 — Install VirtualBox
- Download Oracle VM VirtualBox from virtualbox.org
- Install with default settings
- Create an internal network for all VMs

## Step 2 — Set Up Ubuntu Server VM
- Download Ubuntu Server 22.04 LTS ISO
- Create VM: 4GB RAM, 2 CPU cores, 50GB storage
- Install Ubuntu with default settings
- Set static IP address

## Step 3 — Install Wazuh on Ubuntu Server
```bash
curl -sO https://packages.wazuh.com/4.7/wazuh-install.sh
sudo bash ./wazuh-install.sh -a
```
- Access Wazuh dashboard at: https://[ubuntu-server-ip]
- Default credentials shown after installation

## Step 4 — Set Up Windows 10 VM
- Create Windows 10 VM: 4GB RAM, 2 CPU cores, 60GB storage
- Install Windows 10
- Connect to same internal network as Ubuntu Server

## Step 5 — Install Sysmon on Windows 10
```powershell
# Download Sysmon from Microsoft Sysinternals
# Download sysmonconfig.xml from SwiftOnSecurity GitHub
.\Sysmon64.exe -accepteula -i sysmonconfig.xml
```

## Step 6 — Install Wazuh Agent on Windows 10
- Download Wazuh agent from Wazuh dashboard
- During install, enter Ubuntu Server IP as the Wazuh manager address
- Start the Wazuh agent service
- Verify agent appears as Active in Wazuh dashboard

## Challenge Faced
Ubuntu 24.04 was not supported by Wazuh at time of setup.
Resolved by using Ubuntu 22.04 LTS instead.

## Verification
- Open Wazuh dashboard
- Go to Agents section
- Windows 10 should show as Active ✅
