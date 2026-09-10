# Wazuh SIEM Architecture

## Overview

This project implements a cloud-based Security Information and Event Management (SIEM) lab using Wazuh deployed on AWS EC2.

The environment consists of a centralized Wazuh Manager and an Ubuntu endpoint agent. The agent forwards security events to the Wazuh Manager for monitoring, detection, investigation, and alert analysis.

## Architecture

```text
                    AWS Cloud
                        │
                        │
              ┌─────────▼─────────┐
              │   Wazuh Manager   │
              │     AWS EC2       │
              │                   │
              │ Private IP:       │
              │ 172.31.29.139     │
              │                   │
              │ Wazuh 4.13.1      │
              └─────────┬─────────┘
                        │
                  TCP 1514 / 1515
                        │
              ┌─────────▼─────────┐
              │   Ubuntu Agent    │
              │     AWS EC2       │
              │                   │
              │ Agent ID: 002     │
              │ Private IP:       │
              │ 172.31.81.68      │
              └───────────────────┘
              