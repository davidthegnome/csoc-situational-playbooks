# Man-in-the-Middle (MITM) Attack Playbook

## 1. Objective
This playbook provides a structured response to **Man-in-the-Middle (MITM) attacks**, where adversaries intercept, alter, or relay communications between two parties to steal data, manipulate transactions, or gain unauthorized access. The playbook outlines **detection, investigation, containment, and remediation** steps.

---

## 2. Scope
Applicable to all **MITM attack scenarios**, including:

- **ARP spoofing and poisoning**
- **DNS spoofing and hijacking**
- **HTTPS/TLS stripping attacks**
- **Wi-Fi eavesdropping and rogue access points**
- **Session hijacking and replay attacks**

---

## 3. Detection Methods

### **Network Monitoring**
- Unusual **ARP traffic** or **duplicate IP addresses** in logs.
- Unexpected **SSL/TLS certificate changes**.
- High volume of **DNS query failures** or **alterations**.
- Multiple devices on the network experiencing **connection resets**.

### **Endpoint Detection**
- Unexpected **proxy settings** or **DNS configurations**.
- **Unauthorized certificates** installed.
- **Session timeouts** and **forced logouts** across multiple users.

### **User Reports**
- Reports of **suspicious login prompts, redirects, or security warnings**.
- Users experiencing **credential reuse warnings** without initiating logins.

---

## 4. Investigation & Containment

### **Identify Affected Systems**
- Analyze **network traffic** for anomalous behavior.
- Identify compromised **endpoints, routers, or access points**.
- Verify if **sensitive communications** were intercepted or altered.

### **Containment Steps**
- **Isolate compromised** network segments and endpoints.
- Remove **unauthorized certificates** and restore secure configurations.
- **Block rogue devices** or access points from the network.
- Enforce **encrypted communications** using **VPNs or TLS**.

---

## 5. Remediation & Mitigation

### **Technical Controls**
- Implement **network segmentation** to reduce exposure.
- Enable **DNSSEC** to prevent DNS spoofing.
- Deploy **HTTPS everywhere** and enforce **HSTS (HTTP Strict Transport Security)**.
- Use **ARP inspection and dynamic ARP protection**.
- Enable **multi-factor authentication (MFA)** to mitigate session hijacking.

### **User Awareness & Training**
- Educate users on **risks of unsecured public Wi-Fi**.
- Promote the use of **VPNs** for secure communications.
- Encourage **reporting of suspicious login prompts and connection issues**.

### **Process Improvements**
- Regularly **audit network configurations** and **certificate deployments**.
- Monitor logs for **unexpected changes in communication patterns**.
- Establish a **baseline of normal network activity** to quickly detect anomalies.

---

## 6. Escalation & Reporting
- Escalate **confirmed MITM attacks** to **security operations and IT teams**.
- Notify **affected users and departments**.
- Engage **law enforcement** or **third-party forensic teams** if needed.
- Report incidents to **regulatory bodies** if **customer or sensitive data** was exposed.

---

## 7. References & Resources
- **NIST Cybersecurity Framework** (*Identify, Protect, Detect, Respond, Recover*)
- **OWASP Secure Communications Guidelines**

### MITRE ATT&CK Framework

| **Technique ID**                                                                 | **Name**                                  | **Relevance to MITM**                                                                                                                       |
|----------------------------------------------------------------------------------|-------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**T1557**](https://attack.mitre.org/techniques/T1557/)                          | **Adversary-in-the-Middle**               | Core MITM technique: intercept and manipulate communications between systems or users.                                                       |
| [T1557.001](https://attack.mitre.org/techniques/T1557/001)                      | LLMNR/NBT-NS Poisoning and Relay          | Exploits local name resolution protocols (LLMNR/NetBIOS) to intercept or relay authentication attempts.                                      |
| [T1557.002](https://attack.mitre.org/techniques/T1557/002)                      | ARP Cache Poisoning                       | Redirects LAN traffic by injecting false ARP responses, causing victims to route traffic via the adversary’s system.                        |
| [T1557.003](https://attack.mitre.org/techniques/T1557/003)                      | DHCP Spoofing                             | Provides malicious DHCP configuration, rerouting traffic through attacker-controlled gateways.                                               |
| [**T1565.002**](https://attack.mitre.org/techniques/T1565/002)                  | **Transmitted Data Manipulation**         | Attackers alter data in transit (e.g., injecting malicious commands or changing payloads) to compromise integrity/confidentiality.           |
| [**T1556**](https://attack.mitre.org/techniques/T1556/)                          | **Modify Authentication Process**         | Attackers may tamper with or bypass authentication workflows to harvest credentials or position themselves for MITM.                        |
| [**T1090**](https://attack.mitre.org/techniques/T1090/)                          | **Proxy**                                 | Adversaries route traffic through malicious proxies or redirectors to maintain stealth or intercept communications.                          |
| [**T1071**](https://attack.mitre.org/techniques/T1071/)                          | **Application Layer Protocol**            | Abusing (or downgrading) protocols such as HTTP/HTTPS or DNS to intercept and manipulate application-layer traffic.                          |

