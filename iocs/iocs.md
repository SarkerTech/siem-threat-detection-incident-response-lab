# Indicators of Compromise (IOCs)

## Observed Indicators

| Indicator | Value | Context |
|---|---|---|
| Source IP | `127.0.0.1` | SSH authentication attempt |
| Username | `wronguser` | Invalid login identity |
| Service | `sshd` | SSH authentication |
| Rule ID | `5710` | Authentication failure |

## File Integrity Monitoring

| Indicator | Value |
|---|---|
| File | `/etc/wazuh-test.txt` |
| Rule ID | `554` |
| Rule Level | `5` |
| Event | File added |

## MITRE ATT&CK

| ID | Technique |
|---|---|
| `T1110.001` | Password Guessing |
| `T1021.004` | SSH |

## Note

These indicators were generated inside a controlled AWS lab environment and do not represent a real-world compromise.
