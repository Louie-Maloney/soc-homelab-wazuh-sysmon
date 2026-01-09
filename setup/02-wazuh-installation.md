# Wazuh Installation

## Purpose
This document describes the installation of the Wazuh manager and dashboard on the Ubuntu server used in the SOC home lab.

## Installation Method
- Official Wazuh all-in-one installation script
- Target version: 4.7
- Command used: sudo bash wazuh-install.sh -a


## Installer Compatibility Check
During installation, the script reported that the operating system was not in its recommended systems list and stopped execution.

Error message indicated supported systems such as:
- Red Hat Enterprise Linux
- CentOS
- Amazon Linux

Although Ubuntu 22.04 LTS is supported in practice, the installer’s OS detection check was overly restrictive.

### Resolution
The installation was re-run using the official override flag to bypass the OS compatibility check:

sudo bash wazuh-install.sh -a --ignore-check

This allowed the installation to proceed successfully.

## Components Installed
- Wazuh Manager
- OpenSearch
- Wazuh Dashboard

## Validation
- `wazuh-manager` service running
- `opensearch` service running
- Wazuh dashboard accessible via web browser

## Notes
- OS compatibility check was bypassed using `--ignore-check` on Ubuntu 22.04 LTS
- Dashboard uses a self-signed TLS certificate
- Credentials generated during installation were stored securely and not committed to the repository
