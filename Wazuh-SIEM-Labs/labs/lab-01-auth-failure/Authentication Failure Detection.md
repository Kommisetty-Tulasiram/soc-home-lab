# LAB 01 — Authentication Failure Detection (Wazuh SIEM)

## 🎯 Objective
Detect and analyze **failed authentication attempts** on a Windows endpoint using Wazuh SIEM and perform SOC-style alert triage.

---

## 🏗️ Lab Setup
- **Wazuh Server:** Ubuntu Server VM  
- **Endpoint:** Windows 10 VM  
- **Agent:** Wazuh Agent installed on Windows  
- **Network:** NAT-based isolated lab network  

---

## 🧪 Detection Scenario
A controlled authentication failure scenario was simulated by entering incorrect login credentials multiple times on the Windows system.

This generated **Windows Security Event ID 4625**, which was collected and analyzed by Wazuh.

---

## 🛡️ Detection in Wazuh
Wazuh successfully:
- Ingested Windows security logs
- Detected repeated authentication failures
- Triggered authentication-related detection rules
- Generated alerts in the Security Events dashboard
- Mapped activity to MITRE ATT&CK techniques

---

## 🔍 Alert Details

**Alert Name:**  
`Logon failure – Unknown user or bad password`

**Rule ID:** 60122  
**Severity Level:** 5 (Low–Medium)  
**Event ID:** 4625  
**Logon Type:** Interactive  
**Detection Group:** `authentication_failed`  

**MITRE ATT&CK Mapping:**
- T1078 — Valid Accounts  
- T1531 — Account Access Removal  

---

## 🔑 Key Fields Analyzed
- `agent.name`
- `eventID`
- `logonType`
- `ipAddress`
- `targetUserName`
- `rule.description`
- `rule.level`
- `rule.firedtimes`

These fields were used to understand **who**, **from where**, and **how often** authentication failures occurred.

---

## 🧠 SOC Analysis
- Authentication failures originated from the local system
- No external IP involvement observed
- No remote service usage detected
- Pattern consistent with user error or low-risk authentication abuse

---

## 📊 SOC Classification

| Category | Value |
|--------|------|
| Incident Type | Authentication failure |
| Severity | Low |
| Risk Level | Low |
| Action | Log and monitor |
| Escalation | Not required |

---

## ✅ Outcome
- Log ingestion validated
- Detection rules triggered correctly
- Alerts visible in dashboard
- SOC analysis workflow completed successfully

This lab confirms that the SOC environment is capable of detecting and analyzing authentication-based security events.

---

## 📌 Learning Outcomes
- Understanding Windows authentication logs
- SIEM alert triage
- SOC-style alert interpretation
- MITRE ATT&CK mapping
- Detection-to-analysis workflow

---

## 🏁 Conclusion
This lab establishes the foundation for more advanced SOC detection scenarios such as credential abuse, brute-force attacks, and lateral movement.

It validates the end-to-end SOC pipeline from **event generation → detection → analysis → classification**.

---

## 📂 Screenshots
Screenshots for this lab are available in the `screenshots/` directory and include:
- Agent status
- Security dashboard overview
- Alerts list
- Alert details
- JSON event data

