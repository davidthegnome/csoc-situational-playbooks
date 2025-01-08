# Business Email Compromise (BEC) Incident Response Playbook

## 1. Objective
This playbook provides a structured response to **Business Email Compromise (BEC)** incidents, which involve attackers gaining unauthorized access to business email accounts to conduct fraud, data theft, or further compromise. It includes **detection, investigation, containment, and remediation** steps.

---

## 2. Scope
Applicable to all BEC scenarios, including:

- **Credential compromise** through phishing or brute force attacks.
- **Spoofed email attacks** impersonating executives or vendors.
- **Unauthorized email forwarding** and exfiltration.
- **Fraudulent wire transfer** or invoice scams.

---

## 3. Detection Methods

### **User Reports**
- Employees report **suspicious emails**, **login alerts**, or **unauthorized email rule changes**.

### **SIEM Alerts**
- Logins from **unusual IPs** or **geolocations**.
- Multiple **failed login attempts** followed by success.
- Unusual **email forwarding** or **mailbox rule modifications**.

### **Email Security Solutions**
- Indicators of spoofing (**DMARC, SPF, DKIM failures**).
- **Suspicious attachments or links**.
- Multiple emails with **financial requests** or **urgent language**.

---

## 4. Investigation & Containment

### **Identify Affected Accounts**
- Check **login history** and **device information** for anomalies.
- Review **recent email activity** for unauthorized messages or rule changes.
- Search for **forwarding rules** to external domains.

### **Containment Steps**
- **Immediately reset** compromised account passwords and enforce **MFA**.
- **Disable unauthorized email rules and forwarding**.
- **Revoke active sessions** for affected accounts.
- **Notify IT security, compliance, and impacted users**.

---

## 5. Remediation & Mitigation

### **Technical Controls**
- Enforce **MFA** for all email accounts.
- Implement **email authentication policies** (SPF, DKIM, DMARC).
- Monitor **high-risk logins** with conditional access policies.
- Enable **endpoint detection** for credential theft attempts.

### **User Awareness & Training**
- Educate employees on **phishing detection** and **safe email practices**.
- Regularly test **phishing simulations**.
- Encourage **reporting** of suspicious emails and activities.

### **Process Improvements**
- Implement **financial verification policies** (e.g., verbal confirmation for wire transfers).
- Regularly **audit mailbox rules** and **access permissions**.
- Update **incident response procedures** based on lessons learned.

---

## 6. Escalation & Reporting
- Escalate **confirmed BEC incidents** to security leadership.
- Notify **legal, compliance, and finance** teams if fraud is involved.
- Contact **affected third parties or customers** as necessary.
- Report **fraudulent transactions** to law enforcement and financial institutions.

---

## 7. References & Resources
- **MITRE ATT&CK Framework** (BEC Techniques: `T1078`, `T1566`, `T1114`, etc.)
- **NIST Cybersecurity Framework** (*Identify, Protect, Detect, Respond, Recover*)
- **FBI IC3 Guidelines** for BEC Prevention and Response
