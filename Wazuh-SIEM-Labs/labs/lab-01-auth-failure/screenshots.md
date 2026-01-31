## 📸 LAB-01 Screenshots & Evidence

The following screenshots document the complete SOC workflow for **Authentication Failure Detection** using Wazuh SIEM.

---

### **Figure 1 — Wazuh Agent Status**
**File:** <img width="1915" height="1037" alt="Agents" src="https://github.com/user-attachments/assets/0bb38a88-f686-4233-86d0-3423b6ff3d6c" />

Shows the Windows endpoint (`WIN10-LAB-E1`) successfully connected to the Wazuh Manager with agent status marked as **Active**.

**Purpose:**  
Confirms endpoint onboarding and active log forwarding.

---

### **Figure 2 — Security Events Overview**
**File:** <img width="1910" height="1051" alt="Overview" src="https://github.com/user-attachments/assets/a4c27bcd-f0d0-4921-b115-a6f290b84f97" />


Displays the Wazuh **Security Events → Overview** dashboard, including alert counts, severity distribution, and MITRE ATT&CK visualization.

**Purpose:**  
Demonstrates centralized monitoring and SIEM visibility.

---

### **Figure 3 — Authentication Alerts List**
**File:** <img width="1917" height="1033" alt="Alerts" src="https://github.com/user-attachments/assets/bfeeb91d-0b30-44e8-bdb1-0cd78523596c" />


Shows multiple authentication-related alerts generated within a short time window under **Security Events → Alerts**.

**Purpose:**  
Validates detection of repeated authentication failures.

---

### **Figure 4 — Authentication Failure Alert (Expanded)**
**File:** <img width="1912" height="1037" alt="Brute-force " src="https://github.com/user-attachments/assets/a82309bc-d060-460c-8dda-1df84c320080" />



Expanded alert row showing:
- Alert name: `Logon failure – Unknown user or bad password`
- Rule level
- Detection group

**Purpose:**  
Highlights the specific SOC alert triggered by failed logon attempts.

---

### **Figure 5 — Alert Details View**
**File:** <img width="1912" height="1036" alt="BF_Details_tab" src="https://github.com/user-attachments/assets/af0b4cad-b29d-45f8-8dc8-7f9915d45d3e" />


Displays the alert **Details / Message** tab with Windows Security Event information, including:
- Event ID 4625
- Authentication failure message
- Logon context

**Purpose:**  
Provides analyst-readable evidence for investigation.

---

### **Figure 6 — Alert JSON View**
**File:** <img width="1917" height="1036" alt="BF_Details_JSON_tab" src="https://github.com/user-attachments/assets/f3630310-984c-4e5e-87d6-6c7a366b9a45" />


Shows the raw JSON event data used for SOC analysis, including key fields:
- `rule.description`
- `rule.level`
- `agent.name`
- `eventID`
- `logonType`
- `ipAddress`
- `rule.firedtimes`

**Purpose:**  
Demonstrates low-level forensic data analysis performed by a SOC analyst.

---

## 🔒 Data Handling Notes
- IP addresses have been partially masked.
- Usernames and hostnames are anonymized where necessary.
- No sensitive or real-world production data is included.

---

## 🧠 SOC Evidence Flow
The screenshots follow a structured SOC investigation flow:

**Agent Status → Monitoring Dashboard → Alert List → Alert Identification → Event Details → Raw Forensic Data**

This aligns with real-world SOC documentation and reporting practices.
