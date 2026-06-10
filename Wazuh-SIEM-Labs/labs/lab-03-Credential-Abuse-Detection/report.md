# Lab 03 – Credential Abuse Detection

## Overview

This lab demonstrates how a successful authentication can be detected and investigated after multiple login attempts against a Windows endpoint.

A Kali Linux attacker machine was used to authenticate to a Windows 10 system monitored by Wazuh SIEM. The generated authentication events were collected, analyzed, and correlated to identify potential credential abuse activity.

---

## Lab Environment

| Component | Purpose |
|-----------|---------|
| Ubuntu Server | Wazuh Manager |
| Windows 10 | Monitored Endpoint |
| Kali Linux | Attacker Machine |
| Wazuh Agent | Log Collection |

---

## Attack Simulation

The attacker attempted authentication against the Windows endpoint using Hydra.

```bash
hydra -l hr.user -P passwords.txt rdp://192.xxx.xxx.142 -t 2
```

The attack resulted in successful authentication and generated Windows security events for analysis.

---

## Top 10 Findings

### 1. Successful Authentication Detected

- Event ID: **4624**
- Status: **Success**

### 2. Failed Authentication Activity Observed

- Event ID: **4625**
- Multiple failed login attempts detected before successful authentication.

### 3. Attacker Workstation Identified

- Hostname: **kali**

### 4. Source IP Address Identified

- IP Address: **192.xxx.xxx.142**

### 5. Target Account Identified

- Username: **hr.user**

### 6. Authentication Protocol Captured

- Protocol: **NTLM**

### 7. Security Logs Successfully Collected

- Windows authentication logs forwarded to Wazuh Manager.

### 8. Event Correlation Performed

```text
Failed Logons
      ↓
Successful Logon
      ↓
Potential Credential Abuse
```

### 9. MITRE ATT&CK Mapping

| Technique | ID |
|-----------|----|
| Brute Force | T1110 |

### 10. Potential Security Risk Identified

A successful authentication following repeated login attempts may indicate:

- Password guessing
- Credential compromise
- Unauthorized access attempt

---

## Evidence Summary

| Field | Value |
|---------|---------|
| Event ID (Success) | 4624 |
| Event ID (Failure) | 4625 |
| Source Host | kali |
| Source IP | 192.xxx.xxx.142 |
| Target User | hr.user |
| Authentication Package | NTLM |
| Detection Platform | Wazuh SIEM |

---


## Conclusion

This lab demonstrated the detection and investigation of authentication activity using Wazuh SIEM. By correlating failed and successful login events, it was possible to identify a potential credential abuse scenario and perform SOC-style analysis.

**Status:** Completed ✅

**MITRE ATT&CK:** T1110 – Brute Force

**Lab Series:** SOC Lab Series #3
