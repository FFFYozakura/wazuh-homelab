# Wazuh Home Lab – Blue Team Training Environment

Fully functional Wazuh 4.14.1 SIEM laboratory for learning detection & response.

[![Wazuh](https://img.shields.io/badge/Wazuh-4.14.1-blue)](https://wazuh.com)
[![Ubuntu](https://img.shields.io/badge/Ubuntu-24.04-orange)](https://ubuntu.com)
[![Kali](https://img.shields.io/badge/Kali_Linux-2025.4-purple)](https://kali.org)
[![License](https://img.shields.io/badge/License-MIT-green)](LICENSE)

## Topology
![Lab Topology](topology.png)
*(Coming soon)*

## Features
- Wazuh All-in-One deployment
- Ubuntu 24.04 agent (real-time monitoring)
- Detection of port scanning, brute-force, web attacks, FIM, rootkits

## Screenshots
![Dashboard](screenshots/IMG_20251202_213258_450.jpg)
![Agents](screenshots/agents.png)
![Security Events](screenshots/events.png)
*(more coming soon)*

## Quick Start (VirtualBox)

1. Import `wazuh-4.14.1-all-in-one.ova`
2. Create Ubuntu 24.04 VM (Host-Only + NAT)
3. Install & connect agent:
```bash
curl -so wazuh-agent.deb https://packages.wazuh.com/4.x/apt/pool/main/w/wazuh-agent/wazuh-agent_4.14.1-1_amd64.deb
sudo WAZUH_MANAGER="192.168.56.101" dpkg -i wazuh-agent.deb
sudo systemctl enable --now wazuh-agent
```
4.Attack from Kali → enjoy real-time alerts!
## FUTURE PLANS
Custom Sigma rules for web-attacks
ModSecurity + NGINX WAF
Suricata NIDS integration
Automated PDF reports (Python)
MIT License © 2025–2026 FFFYozakura
