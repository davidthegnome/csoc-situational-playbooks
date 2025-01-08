# Denial-of-Service (DoS) Attack Playbook

## 1. Objective
This playbook provides a structured response to **Denial-of-Service (DoS) attacks**, where adversaries attempt to **disrupt or degrade services** by overwhelming network, application, or system resources. The playbook outlines **detection, investigation, containment, and remediation** steps.

---

## 2. Scope
Applicable to all **DoS attack scenarios**, including:

- **Volumetric attacks** (e.g., UDP flood, ICMP flood, SYN flood)
- **Application-layer attacks** (e.g., HTTP flood, Slowloris attack)
- **Protocol-based attacks** (e.g., TCP state exhaustion, DNS amplification)
- **Local resource exhaustion** (e.g., excessive process creation, memory leaks)

---

## 3. Detection Methods

### **Network Monitoring**
- Unusual **spikes in inbound/outbound traffic**.
- High **CPU or memory usage** on network devices.
- Abnormal patterns in **firewall logs** (e.g., excessive connections from a single IP).

### **Application & Server Logs**
- High **request rates** from single or multiple IPs.
- Frequent **503/504 (Service Unavailable) errors**.
- Increased **latency or timeouts** in application logs.

### **User Reports**
- Complaints of **slow or unresponsive services**.
- **Loss of access** to critical resources or applications.

---

## 4. Investigation & Containment

### **Identify Attack Characteristics**
- Analyze **traffic patterns** to determine the **type of DoS attack**.
- Identify **source IPs, protocols, and target endpoints**.
- Verify if **multiple vectors** are being used simultaneously.

### **Containment Steps**
- Implement **rate limiting** and **connection throttling** on affected services.
- Activate **DoS/DDoS protection mechanisms** in firewalls, IDS/IPS, and WAF.
- Drop or **filter malicious traffic** based on attack characteristics.
- **Isolate affected systems** if necessary to prevent further degradation.

---

## 5. Remediation & Mitigation

### **Technical Controls**
- Deploy **anti-DoS mechanisms** (e.g., **DDoS protection services, rate limiting**).
- Use **Web Application Firewalls (WAF)** to mitigate application-layer attacks.
- Implement **SYN cookies** and other **TCP-hardening techniques**.
- Enable **DNSSEC** and **secure recursive DNS** to prevent amplification attacks.

### **User Awareness & Training**
- Train **IT and security teams** on identifying and responding to **DoS incidents**.
- Educate users on **signs of slow network performance** due to attacks.

### **Process Improvements**
- Regularly **update firewall and IDS/IPS rules** to detect new DoS techniques.
- Establish **incident response procedures** for recurring DoS events.
- Conduct **periodic stress testing** to measure infrastructure resilience.

---

## 6. Escalation & Reporting
- Escalate **confirmed DoS attacks** to **network security and IT operations teams**.
- Notify **affected departments and stakeholders** about service impact.
- Engage **internet service providers (ISPs)** if attack traffic originates externally.
- Report **large-scale attacks** to relevant **regulatory authorities**, if necessary.

---

## 7. References & Resources
- **MITRE ATT&CK Framework** (DoS Techniques: `T1498`, `T1499`, etc.)
- **NIST Cybersecurity Framework** (*Identify, Protect, Detect, Respond, Recover*)
- **OWASP DoS Prevention Best Practices**

---
