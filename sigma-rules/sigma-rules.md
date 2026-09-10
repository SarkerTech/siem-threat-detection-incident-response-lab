# Sigma Detection Rules

## 1. SSH Authentication Failure

This rule represents the detection logic for failed SSH authentication attempts observed in the Wazuh SIEM lab.

```yaml
title: SSH Authentication Failure
id: lab-ssh-authentication-failure
status: experimental
description: Detect failed SSH authentication attempts
logsource:
  product: linux
  service: sshd

detection:
  selection:
    message|contains:
      - "Failed password"
      - "authentication failure"
      - "Invalid user"
  condition: selection

level: medium

tags:
  - attack.credential_access
  - attack.t1110.001
  - attack.lateral_movement
  - attack.t1021.004