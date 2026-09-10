# Incident Report — SSH Authentication Attack

## Incident Summary

A controlled SSH authentication attack was simulated against the Ubuntu endpoint. Wazuh successfully collected the event, generated a security alert, and mapped the activity to MITRE ATT&CK.

## Incident Details

| Field | Value |
|---|---|
| Affected Agent | `ip-172-31-81-68` |
| Agent ID | `002` |
| Source IP | `127.0.0.1` |
| Source User | `wronguser` |
| Service | SSH |
| Rule ID | `5710` |
| Severity | Level 5 |
| Decoder | `sshd` |

## Attack Simulation

```bash
ssh wronguser@localhost
