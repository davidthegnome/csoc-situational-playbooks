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

## 3. Preperation
Applicable to all BEC scenarios, including:

- **Credential compromise** through phishing or brute force attacks.
- **Spoofed email attacks** impersonating executives or vendors.
- **Unauthorized email forwarding** and exfiltration.
- **Fraudulent wire transfer** or invoice scams.

---

## 4. Detection Methods (Detect)

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

## 5. Analysis (Respond)

### **Identify Affected Accounts**
- Check **login history** and **device information** for anomalies.
- Review **recent email activity** for unauthorized messages or rule changes.
- Search for **forwarding rules** to external domains.

---

## 5. Contain/Eradicate (Protect)

### **Containment Steps**
- **Immediately reset** compromised account passwords and enforce **MFA**.
- **Disable unauthorized email rules and forwarding**.
- **Revoke active sessions** for affected accounts.
- **Notify IT security, compliance, and impacted users**.

---

## 6. Remediation & Mitigation (Protect, Recover)

### **Technical Controls**
- Enforce **MFA** for all email accounts.
- Implement **email authentication policies** (SPF, DKIM, DMARC).
- Monitor **high-risk logins** with conditional access policies.
- Enable **endpoint detection** for credential theft attempts.

### **User Awareness & Training** (Protect, Detect)
- Educate employees on **phishing detection** and **safe email practices**.
- Regularly test **phishing simulations**.
- Encourage **reporting** of suspicious emails and activities.

### **Process Improvements** (Identify, Protect)
- Implement **financial verification policies** (e.g., verbal confirmation for wire transfers).
- Regularly **audit mailbox rules** and **access permissions**.
- Update **incident response procedures** based on lessons learned.

---

## 7. Escalation & Reporting (Respond, Recover)
- Escalate **confirmed BEC incidents** to security leadership.
- Notify **legal, compliance, and finance** teams if fraud is involved.
- Contact **affected third parties or customers** as necessary.
- Report **fraudulent transactions** to law enforcement and financial institutions.

---

## 8. References & Resources
- **MITRE ATT&CK Framework**
  | Technique ID | Name | Relevance to BEC |
  |-------------|---------------------------|-----------------------------------------------------|
  | **T1078** | Valid Accounts | Use of compromised credentials to access accounts. |
  | **T1566** | Phishing | Primary initial access vector for BEC. |
  | **T1114** | Email Collection | Threat actors accessing/storing email data. |
  | **T1113** | Screen Capture | Attackers capturing sensitive email communications. |
  | **T1056** | Input Capture | Credential theft via keyloggers or form grabbers. |
  | **T1204** | User Execution | Trick users into executing malicious attachments/links. |
  | **T1071** | Application Layer Protocol | C2 over email protocols (IMAP/SMTP). |
  | **T1098** | Account Manipulation | Threat actors modifying mailbox rules or MFA settings. |
  | **T1557** | Man-in-the-Middle | Intercepting email traffic to alter communications. |
  | **T1564** | Hide Artifacts | Hiding email forwarding rules or alerts from detection. |
  | **T1021** | Remote Services | Using compromised accounts to access internal services. |
  | **T1484** | Group Policy Modification | Modifying security policies to maintain access. |
- **NIST Cybersecurity Framework** [*Identify, Protect, Detect, Respond, Recover*](https://www.nist.gov/cybersecurity)
- **FBI IC3 Guidelines** for [BEC Prevention and Response](https://www.fbi.gov/how-we-can-help-you/scams-and-safety/common-frauds-and-scams/business-email-compromise)
