### 🛡️ Wazuh SIEM Lab — SSH Brute-Force Detection 

A hands-on homelab simulating real-world attack detection and compliance hardening using Wazuh SIEM.

### 📋 Project Overview

This lab demonstrates end-to-end security monitoring: simulating a brute-force attack, and detecting it with custom Wazuh rules. All findings are mapped to industry frameworks used in GRC and compliance roles.

### Lab Environment:

### Component
- **Host OS**- Ubuntu 25.04
- **SIEM** - Wazuh 4.x (Server IP: 172.16.0.10)
- **Attacker** - Ubuntu
- **Target** - Metasploitable 3 (172.16.0.12)
- **Network** - Bridged Adapter + NAT

### 🎯 Project 1 — SSH Brute-Force Detection
**Objective**- 
Simulate a credential-stuffing attack and detect it using custom Wazuh detection rules mapped to MITRE ATT&CK.

**What I did** 

**1. SSH into Metasploitable 3** VM using Command Prompt

**2. Installed and deployed** Wazuh agents on Ubuntu (172.16.0.11) and Metasploitable 3 (172.16.0.12) VMs 

**3. Created custom Wazuh detection rules** (Rule IDs 100001–100004) in XML targeting SSH authentication failures and brute-force thresholds

**4. Ran a Hydra brute-force Attack** from Ubuntu terminal against Metasploitable 3 over SSH

**5. Confirmed detection** in Wazuh Security Events dashboard — alerts fired as expected

**6. Mapped findings** to MITRE ATT&CK, NIST SP 800-53, and NIST CSF 2.0

### Framework Mapping

- **Control**- MITRE ATT&CK

  **Mapping**-  T1110 — Brute Force, T1110.001 — Password Guessing

- **Control**- NIST SP 800-53

  **Mapping** - SI-4 (System Monitoring), AU-2 (Event Logging), AC-7 (Unsuccessful Login Attempts)

- **Control**- NIST CSF 2.0

  **Mapping**- DE.CM-01 (Networks and network services are monitored)

  ### Screenshots

  <img width="959" height="598" alt="SSH Meta" src="https://github.com/user-attachments/assets/151d82e8-28a8-46b8-a6c4-eed827f8bb8d"
 />

<img width="959" height="599" alt="Agents" src="https://github.com/user-attachments/assets/e84b3147-a3e4-4743-921d-df408c86c187" />

<img width="959" height="530" alt="rules" src="https://github.com/user-attachments/assets/1c911b2e-584e-46df-b690-18d760f32221" />

<img width="949" height="599" alt="SSH   Brute Fore" src="https://github.com/user-attachments/assets/a7937bcb-97a0-4782-9249-cd40ec771c7f" />

<img width="473" height="466" alt="rule ID" src="https://github.com/user-attachments/assets/eb956359-fbb3-413e-a150-c82a67265990" />

<img width="498" height="518" alt="SSH details" src="https://github.com/user-attachments/assets/1899824b-d4ae-4387-b882-b464bc7e8b3d" />

<img width="668" height="503" alt="MITRE" src="https://github.com/user-attachments/assets/034eefd9-3b33-45ec-9d79-8afa3f71a17d" />


