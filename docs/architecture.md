# SOC Home Lab — Architecture

This document describes the **logical and technical architecture** of the SOC home lab built using Wazuh SIEM.

---

## 🧭 Architecture Overview

The lab is designed to simulate a **real enterprise SOC environment** with centralized monitoring, detection, and analysis.

### Core Design Model

Endpoints → Wazuh Agent → Wazuh Manager → Indexer → Dashboard → SOC Analyst

---

## 🧱 Components

### 🛡 Wazuh Server (Ubuntu Server VM)
**Role:** Central SIEM platform  
**Functions:**
- Log ingestion  
- Event correlation  
- Detection rules  
- Alert generation  
- MITRE mapping  
- Dashboard visualization  

**Services:**
- Wazuh Manager  
- Wazuh Indexer  
- Wazuh Dashboard  

---

### 🖥 Windows 10 Endpoint VM
**Role:** Log source / monitored asset  
**Functions:**
- Windows Security logging  
- Authentication telemetry  
- Process monitoring  
- System activity logging  

**Component:**
- Wazuh Agent

---

### 🐉 Kali Linux VM
**Role:** Controlled attack simulation  
**Functions:**
- Authentication testing  
- Network attack simulation  
- Detection validation  
- SOC scenario generation  

---

### 💻 Host System
**Role:** Infrastructure platform  
**Functions:**
- VM orchestration  
- Network virtualization  
- Lab isolation  

---

## 🌐 Network Architecture

- Network type: **NAT**
- Internal lab network
- Isolated from public networks
- Controlled communication paths
- Secure agent–manager connectivity

---

## 🔗 Data Flow Model

Windows Events

↓

Wazuh Agent

↓

Wazuh Manager

↓

Rule Engine

↓

Indexer

↓

Dashboard

↓

SOC Analysis

---

## 🧠 SOC Workflow Mapping

| Layer | Function |
|------|--------|
| Endpoint  | Event generation |
| Agent     | Log collection |
| Manager   | Correlation & detection |
| Indexer   | Storage & indexing |
| Dashboard | Visualization |
| Analyst   | Triage & response |

---

## 🔍 Detection Architecture

- Rule-based detection  
- Pattern-based correlation  
- Authentication monitoring  
- Behavior-based indicators  
- MITRE ATT&CK mapping  
- Severity classification  

---

## 🎯 Design Goals

- Real SOC simulation  
- Modular lab design  
- Scalable architecture  
- Detection-first approach  
- Blue-team focused  
- Learning-oriented structure  

---

## 📐 Architecture Principles

- Centralized logging  
- Defense-first design  
- Least complexity  
- Realistic SOC workflows  
- Scalable lab model  
- Professional SOC structure  

---

## 🏁 Summary

This architecture enables:
- Real-time monitoring  
- Attack detection  
- SOC alert analysis  
- Incident simulation  
- Blue-team training  
- Detection engineering practice  

The design mirrors **enterprise SOC environments** in a controlled learning setup.



