# Ubuntu server Installation 

## Overview 

Ubuntu Server 22.04 LTS was installed in Oracle VM VirtualBox to host the Wazuh SIEM platform for the SOC home lab environment.
The Ubuntu server acts as the centralized monitoring machine responsible for log collection, alert generation, and security event management.

## Why Ubuntu Server ?

Ubuntu Server was selected because it is :
* Lightweight
* Stable
* Widely used in enterprise enviournment
* Compatible with Wazuh SIEM
* Suitable for server-based security monitoring

## Virtual Machine Configuration

| Component | Configuration |
|---|---|
| Operating System | Ubuntu Server 22.04 LTS |
| RAM | 4 GB |
| CPU | 2 Cores |
| Storage | 40 GB |
| Network Adapter | Host-Only Adapter |

## Installation Steps

### Step 1 — Download Ubuntu Server ISO

Downloaded Ubuntu Server 22.04 LTS ISO from the official Ubuntu website.

### Step 2 — Create Virtual Machine

Created a new virtual machine in Oracle VM VirtualBox with the required hardware specifications.

### Step 3 — Attach ISO File

Attached the Ubuntu Server ISO file through VirtualBox storage settings.


### Step 4 — Configure Networking

Configured the network adapter using Host-Only mode to allow communication between the virtual machines in the SOC lab environment.

### Step 5 — Install Ubuntu Server

Installed Ubuntu Server using the default installation process.

Configured:
- Username
- Password
- Server hostname

### Step 6 — Enable OpenSSH

Enabled OpenSSH during installation to allow remote terminal access and server management.


### Step 7 — Update System Packages

Updated Ubuntu packages after installation using:

```bash
sudo apt update && sudo apt upgrade -y
