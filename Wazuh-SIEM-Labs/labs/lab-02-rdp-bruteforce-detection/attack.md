# Lab 02 — RDP Brute-Force Detection

## 🎯 Objective
Simulate a real-world RDP brute-force attack and detect it using Wazuh SIEM while performing SOC-style alert investigation.

---

## 🧪 Lab Architecture

| Role | Machine |
|--------|------------|
| SIEM | Ubuntu Server (Wazuh Manager) |
| Victim | Windows 10 Endpoint |
| Attacker | Kali Linux |
| Attack Tool | Hydra |

---

## ⚔️ Attack Scenario

An attacker attempts to gain unauthorized access by repeatedly guessing the password of a Windows account over Remote Desktop Protocol (RDP).

This technique is commonly used during:

- Initial Access
- Credential Access

---

## 🔥 Attack Execution

Hydra was used to perform a password brute-force attack against the Windows endpoint.

**Target:** RDP (Port 3389)  
**Username:** hr.user  
**Wordlist:** rockyou.txt  

👉 See full attack steps:

➡️ **[Attack Documentation](attack.md)**

---

## 🚨 Detection Summary

Wazuh generated multiple high-severity alerts indicating authentication abuse.

### Key Alerts:
- Multiple Windows logon failures — **Level 10**
- User account locked out — **Level 9**
- Logon failure — Unknown user or bad password

👉 Full detection analysis:

➡️ **[Detection Breakdown](detection.md)**

---

## 🔎 SOC Investigation

During investigation, the following indicators were identified:

- Event ID: **4625**
- Logon Type: **3 (Network)**
- Authentication Package: **NTLM**
- Source IP traced to attacker machine
- MITRE Technique: **T1110 — Brute Force**

👉 View investigation:

➡️ **[Investigation Notes](investigation.md)**

---

## 📸 Evidence

| Step | Screenshot |
|--------|---------------|
| Hydra attack | screenshots/1-hydra.png |
| Severity 10 alert | screenshots/2-severity10.png |
| Account lockout | screenshots/3-lockout.png |
| Expanded alert | screenshots/4-expanded.png |
| Alert details | screenshots/5-details.png |
| JSON evidence | screenshots/6-json.png |

---

## 🧠 Skills Gained

- Brute-force attack detection  
- Authentication log analysis  
- SIEM alert triage  
- MITRE ATT&CK mapping  
- Incident investigation  
- Threat identification  

---

## ✅ Outcome

The simulated attack was successfully detected before compromise.

This lab demonstrates how SOC teams identify credential attacks early and respond proactively.

---

> Hands-on detection is the fastest way to become job-ready in cybersecurity.
