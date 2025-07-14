# SIEM Lab with Splunk, pfSense, n8n & Slack Integration

This project demonstrates a hands-on SIEM lab environment designed to simulate real-world SOC workflows with log collection, alert generation, and automation using n8n and Slack integration.

---

## 🌐 Network Diagram

![SIEM Lab Diagram](screenshots/SIEM%20Automation%20LAB.jpeg)

---

## 🔧 Lab Components

| Component            | Role                           | IP Address     |
|--------------------- |------------------------------- |----------------|
| pfSense Firewall     | Network segmentation           | 10.0.1.1       |
| Splunk               | SIEM platform                  | 10.0.1.110     |
| Windows Server 2022  | Domain Controller (SQUID.local)| 10.0.1.104     |
| Windows 10           | Domain-joined endpoint         | 10.0.1.120     |
| Kali Linux           | Attacker machine               | 70.0.1.101     |
| n8n                  | SOAR automation engine         | 10.0.1.10      |

---

1. **pfSense**
![pfSense interface](screenshots/pfSense.png)

---

2. **Windows Server**
![Domain Controller](screenshots/Windows%20Server.png)

---

3. **Domain PC**
![Domain PC](screenshots/windows10ip.png)

---

4. **Splunk SIEM**
![Splunk](screenshots/Splunkip.png)

---

5. **n8n Automation**
![n8n](screenshots/n8nip.png)

---

6. **Attacker IP**
![AttackPC](screenshots/kaliip.png)

---

## 🛠️ Features

- Log collection from Windows endpoints via Universal Forwarder
- Alert creation in Splunk for suspicious activity (e.g., PowerShell abuse, failed logons)
- Automated alert forwarding using n8n webhook
- Slack notifications with key alert details
- Network isolation between internal and attack zones via pfSense

---

## 🚀 How It Works

1. **Log Collection** → Windows logs are sent to Splunk via Universal Forwarder.
  
2. **Alert Detection** → Splunk searches detect anomalies and trigger alerts.
![SIEM](screenshots/splunksiem.png)

3. **n8n Webhook** → Splunk alert webhook forwards to n8n.
![n8nsetup](screenshots/n8nwebhooksetup.png)

4. **Automation** → n8n parses and sends alert to Slack channel.
![n8n](screenshots/splunkton8n.png)

5. **SOC Visibility** → Slack receives alert messages for analyst review.
![n8nautomation](screenshots/n8ntoslack.png)

---

## 📚 Learning Outcomes

- SIEM setup and log forwarding
- Alert creation and tuning
- SOAR automation using open-source tools
- Hands-on cybersecurity detection and response workflows

---

## 📌 Credits

This project was built by [Nishan Rajmulik](https://www.linkedin.com/in/nishanrajmulik) as part of a hands-on cybersecurity learning journey.

---
