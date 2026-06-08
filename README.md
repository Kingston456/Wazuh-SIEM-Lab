### 🛡️ Wazuh SIEM Lab — SSH Brute-Force Detection 

A hands-on homelab simulating real-world attack detection and compliance hardening using Wazuh SIEM.

### 📋 Project Overview

This lab demonstrates end-to-end security monitoring: simulating a brute-force attack, detecting it with custom Wazuh rules, and hardening the target system against SCA failures. All findings are mapped to industry frameworks used in GRC and compliance roles.

### Lab Environment:

### Component
- **Host OS**- Ubuntu 25.04
- **SIEM** - Wazuh 4.x (Server IP: 172.16.0.10)
- **Attacker** - Kali Linux
- **Target** - Metasploitable 3 (172.16.0.12)
- **Network** - Bridged Adapter + NAT

### 🎯 Project 1 — SSH Brute-Force Detection
**Objective**- 
Simulate a credential-stuffing attack and detect it using custom Wazuh detection rules mapped to MITRE ATT&CK.

**What I did** 

**1. SSH into Metasploitable 3** VM using Command Prompt

**2. Installed and deployed** Wazuh agents on Ubuntu (172.16.0.11) and Metasploitable 3 (172.16.0.12) VM's 

**3. Created Custom Wazuh detection rules** (Rule IDs 100001–100004) in XML targeting SSH authentication failures and brute-force thresholds

**4. Ran a Hydra Brute-Force Attack** from Kali Linux against Metasploitable 3 over SSH

**5. Confirmed detection** in Wazuh Security Events dashboard — alerts fired as expected

**6. Mapped Findings** to MITRE ATT&CK and NIST SP 800-53

### Framework Mapping

- **Control**- MITRE ATT&CK

  **Mapping**-  T1110 — Brute Force, T1110.001 — Password Guessing

- **Control**- NIST SP 800-53

  **Mapping** - SI-4 (System Monitoring), AU-2 (Event Logging), AC-7 (Unsuccessful Login Attempts)

- **Control**- NIST CSF 2.0

  **Mapping**- DE.CM-01 (Networks and network services are monitored)

  ### Screenshots



