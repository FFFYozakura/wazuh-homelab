# wazuh-homelab
Blue Team Home Lab with Wazuh 4.14.1 SIEM – real-time detection of brute-force, scanning and web attacks

# Wazuh Home Lab – Blue Team Training Environment

Fully functional Wazuh 4.14.1 SIEM laboratory for learning detection & response.

[![Wazuh](https://img.shields.io/badge/Wazuh-4.14.1-blue)](https://wazuh.com)
[![Ubuntu](https://img.shields.io/badge/Ubuntu-24.04-orange)](https://ubuntu.com)
[![Kali](https://img.shields.io/badge/Kali_Linux-2025.1-purple)](https://kali.org)
[![License](https://img.shields.io/badge/License-MIT-green)](LICENSE)

## Topology
![Lab Topology](topology.png)

## Features
- Wazuh All-in-One deployment (manager + dashboard)
- Linux agent (Ubuntu 24.04) with real-time monitoring
- Detection of:
  - Port scanning (nmap)
  - Brute-force attacks (hydra, medusa)
  - Web reconnaissance (nikto, gobuster, dirb)
  - File integrity monitoring (FIM)
  - Suspicious commands and processes

## Screenshots
- Dashboard overview
- Agent connected
- Brute-force alerts
- Nmap scan detection
- Web attack alerts

## Quick Start (VirtualBox)
1. Import `wazuh-4.14.1-all-in-one.ova`
2. Create Ubuntu 24.04 VM (Host-Only + NAT network)
3. Install Wazuh agent:
```bash
curl -so wazuh-agent.deb https://packages.wazuh.com/4.x/apt/pool/main/w/wazuh-agent/wazuh-agent_4.14.1-1_amd64.deb
sudo WAZUH_MANAGER="192.168.56.101" dpkg -i wazuh-agent.deb
sudo systemctl enable --now wazuh-agent
