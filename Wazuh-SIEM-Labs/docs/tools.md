# SOC Home Lab — Tools & Technologies

This document lists and explains the tools and platforms used in the SOC home lab environment.

---

## 🛡 Wazuh SIEM

**Role:** Central Security Information and Event Management (SIEM)

**Functions:**
- Log ingestion  
- Event correlation  
- Detection rules  
- Alerting  
- MITRE ATT&CK mapping  
- Dashboard visualization  
- SOC monitoring  

**Components:**
- Wazuh Manager  
- Wazuh Indexer  
- Wazuh Dashboard  
- Wazuh Agent  

---

## 🐧 Ubuntu Server

**Role:** SIEM host platform

**Purpose:**
- Runs Wazuh Manager  
- Hosts indexer and dashboard  
- Central monitoring server  
- Detection engine platform  

**Why Ubuntu:**
- Stability  
- Enterprise usage  
- Server-grade OS  
- SOC-standard environment  

---

## 🪟 Windows 10

**Role:** Monitored endpoint

**Purpose:**
- Log generation  
- Authentication telemetry  
- Security event source  
- Endpoint monitoring  

**Key logs:**
- Windows Security Logs  
- Authentication logs  
- Process creation logs  
- System activity logs  

---

## 🐉 Kali Linux

**Role:** Controlled attack simulation

**Purpose:**
- Generate test attack activity  
- Validate detection  
- Simulate adversary behavior  
- SOC detection testing  

**Use case:**
- Not for exploitation learning  
- Only for defensive detection validation  

---

## 💻 VMware Workstation

**Role:** Virtualization platform

**Functions:**
- VM orchestration  
- Network virtualization  
- Lab isolation  
- Snapshot management  
- Multi-VM environments  

---

## 🧠 MITRE ATT&CK

**Role:** Threat modeling framework

**Purpose:**
- Technique classification  
- Tactic mapping  
- Threat modeling  
- SOC detection alignment  

---

## 🔍 SOC Tools & Concepts

**Integrated concepts:**
- SIEM  
- Log management  
- Detection engineering  
- Alert triage  
- Incident classification  
- SOC workflows  
- Blue-team operations  

---

## 🎯 Tool Selection Goals

- Enterprise relevance  
- SOC alignment  
- Real-world usage  
- Learning effectiveness  
- Detection-first approach  
- Blue-team focus  

---

## 🏁 Summary

The toolset is designed to:
- Simulate enterprise SOC environments  
- Provide hands-on detection experience  
- Support SOC learning paths  
- Build analyst-level skills  
- Enable realistic SOC workflows  

This lab focuses on **defensive security**, not offensive exploitation.

