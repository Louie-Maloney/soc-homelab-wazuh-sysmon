# Ubuntu Wazuh Server Setup

## Purpose
This document describes the setup of the Ubuntu server used to host the Wazuh manager and dashboard for the SOC home lab.

## Environment
- Virtualization: VirtualBox
- Guest OS: Ubuntu Server 22.04 LTS
- VM Name: Ubuntu-Wazuh
- Hostname: wazuh-server
- Username: socadmin

## Virtual Machine Specifications
- CPU: 2 cores
- Memory: 4 GB RAM
- Disk: 40 GB (VDI, dynamically allocated)
- Network Mode: NAT

## Installation Steps
1. Created a new VirtualBox VM with the specifications above.
2. Attached the Ubuntu 22.04 Server ISO.
3. Installed Ubuntu using default settings and full disk allocation.
4. Enabled OpenSSH server during installation.
5. Removed installation ISO after completion.
6. Logged in successfully after reboot.

## Post-Installation Tasks
- Updated system packages using `apt update && apt upgrade`
- Verified network connectivity and IP assignment

## Validation
- Successful login to Ubuntu console
- Network connectivity confirmed
- System fully updated

## Notes
- Installation required manual removal of ISO after completion.
