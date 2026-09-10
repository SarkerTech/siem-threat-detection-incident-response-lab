# SIEM Threat Detection & Incident Response Lab

A hands-on cybersecurity lab implementing a cloud-based SIEM environment with Wazuh on AWS EC2.

The project demonstrates endpoint monitoring, File Integrity Monitoring (FIM), SSH authentication detection, alert investigation, and MITRE ATT&CK mapping.

## 🛠️ Technologies

- AWS EC2
- Wazuh 4.13.1
- Ubuntu Linux
- Wazuh Agent
- Wazuh Manager
- SSH
- File Integrity Monitoring
- MITRE ATT&CK
- SIEM
- GitHub

## 🏗️ Architecture

```text
                 AWS Cloud
                     |
             +-------v-------+
             | Wazuh Manager |
             |   EC2 Server  |
             +-------+-------+
                     |
               TCP 1514/1515
                     |
             +-------v-------+
             | Ubuntu Agent  |
             |    EC2        |
             +---------------+
                     |
             Security Events
                     |
             +-------v-------+
             | Wazuh Alerts  |
             +-------+-------+
                     |
             Investigation
                     |
             MITRE ATT&CK