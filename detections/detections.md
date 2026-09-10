# Security Detections

## Detection Overview

The Wazuh SIEM environment was tested with controlled security events generated on the Ubuntu endpoint.

The testing demonstrated two primary detection capabilities:

1. File Integrity Monitoring (FIM)
2. SSH authentication failure detection

---

## 1. File Integrity Monitoring

### Test

A test file was created and modified in the monitored `/etc` directory:

```bash
echo "FIM realtime test $(date)" | sudo tee -a /etc/wazuh-test.txt
