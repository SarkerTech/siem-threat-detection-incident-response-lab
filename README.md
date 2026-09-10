# SIEM Threat Detection & Incident Response Lab

A hands-on cybersecurity lab built with **AWS EC2 and Wazuh SIEM** to practice security monitoring, alert investigation, file integrity monitoring, and SSH attack detection.

## What I Built

- Deployed Wazuh Manager on AWS EC2
- Connected an Ubuntu Linux endpoint as a Wazuh agent
- Configured communication between the manager and agent
- Tested File Integrity Monitoring (FIM)
- Detected failed SSH authentication attempts
- Investigated Wazuh security alerts
- Mapped detections to MITRE ATT&CK techniques
- Created a basic Sigma detection rule

## Environment

| Component | Details |
|---|---|
| Cloud | AWS EC2 |
| SIEM | Wazuh 4.13.1 |
| Manager | Ubuntu Linux |
| Agent | Ubuntu Linux |
| Agent ID | 002 |
| Monitoring | FIM, SSH logs |
| MITRE ATT&CK | T1110.001, T1021.004 |

## Detections

### File Integrity Monitoring

Created a test file:

`/etc/wazuh-test.txt`

Wazuh detected the new file with **Rule 554**.

### SSH Authentication

Generated a controlled failed SSH login:

`ssh wronguser@localhost`

Wazuh detected the event with **Rule 5710**.

The alert included:

- Source IP: `127.0.0.1`
- User: `wronguser`
- Service: `sshd`

## MITRE ATT&CK

The SSH detection was mapped to:

- **T1110.001** — Password Guessing
- **T1021.004** — SSH

## Screenshots

### Wazuh Agent Connected
![Wazuh Agent](screenshots/wazuh-agent-connected-dashboard.png)

### File Integrity Alert
![FIM Alert](screenshots/fim-file-added-alert.png)

### SSH Failed Login
![SSH Alert](screenshots/ssh-failed-login-alert.png)

### Alert Investigation
![SSH Investigation](screenshots/ssh-alert-investigation.png)

### MITRE ATT&CK Mapping
![MITRE Mapping](screenshots/mitre-attack-ssh-mapping.png)

## Project Structure

```text
architecture/
detections/
incident-reports/
iocs/
logs/
screenshots/
sigma-rules/
README.md

---

## Author

**SarkerTech**


