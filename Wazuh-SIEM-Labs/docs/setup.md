# SOC Home Lab — Setup Guide

This document describes the setup process for building the SOC home lab environment using Wazuh SIEM.

---

## 🧱 Environment Overview

### Core Components
- **Ubuntu Server VM** → Wazuh Manager / SIEM  
- **Windows 10 VM** → Endpoint with Wazuh Agent  
- **Kali Linux VM** → Attack simulation  
- **VMware Workstation** → Virtualization platform  

---

## ⚙️ Virtual Machine Setup

### Ubuntu Server (Wazuh Manager)
- OS: Ubuntu Server 24.04 LTS (recommended)
- Role:
  - Wazuh Manager  
  - Wazuh Indexer  
  - Wazuh Dashboard  
- Deployment model: **All-in-one**

**Installed components:**
- Log management
- Alerting engine
- SIEM dashboard
- Rule engine
- Indexer

---

### Windows 10 (Monitored Endpoint)
- Role: Log source
- Wazuh Agent installed
- Security event logging enabled
- Authentication monitoring enabled
- Endpoint telemetry active

---

### Kali Linux (Attack Simulation)
- Role: Controlled attack simulation
- Used for:
  - Authentication testing
  - Network-based attack simulation
  - SOC detection validation

---

## 🌐 Network Configuration

- VM Network Mode: **NAT**
- Inter-VM communication enabled
- Agent-to-manager connectivity verified
- Secure internal lab network

---

## 🔗 Agent Deployment

Steps:
1. Install Wazuh Agent on Windows 10 VM  
2. Configure manager IP address  
3. Register agent with Wazuh Manager  
4. Start Wazuh agent service  
5. Verify agent status = **Active** in dashboard  

---

## ✅ Verification Checklist

- Wazuh Manager running  
- Dashboard accessible  
- Agent service running  
- Agent status = Active  
- Logs flowing  
- Alerts generated  
- Dashboards updating  

---

## 🔍 Validation

The setup is considered successful when:
- Windows security events appear in Wazuh
- Alerts are generated in **Security Events**
- Agent is visible in **Management → Agents**
- Dashboard shows real-time activity

---

## 🎯 Outcome

The SOC environment is fully operational and ready for:
- Detection engineering  
- SOC alert analysis  
- Incident simulation  
- Multi-stage attack detection  
- Blue-team training  

---

## 📌 Notes
- All activity is performed in an isolated virtual environment  
- No external systems are targeted  
- Lab is for defensive security learning only  

