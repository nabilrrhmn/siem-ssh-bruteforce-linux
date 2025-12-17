# SIEM SSH Brute Force Detection Lab (Linux)

## Overview
This project demonstrates a blue team SIEM lab focused on detecting and responding to SSH brute-force attacks on a Linux system. The lab simulates attacker behavior, detection logic, and incident response from a SOC analyst perspective.

## Tools and Technologies
- Linux (Ubuntu)
- SSH authentication logs (auth.log)
- SIEM detection logic (Wazuh-style)
- Incident response documentation

## Attack Scenario
An attacker attempts multiple SSH login attempts using different usernames from a single IP address in a short time period.

## What This Project Demonstrates
- Understanding of Linux authentication logs
- SSH brute-force detection logic
- Alert triage and investigation
- Incident response reporting
- Blue team and SOC fundamentals
- Translation of attacker behavior into detection logic
- Mapping of detections to Wazuh SIEM rules
- SOC-level alert investigation and response workflow


## Repository Structure
- log-sources: Linux authentication logs
- detections: Detection logic and alert conditions
- incident-response: SOC-style incident report
- screenshots: Example alert evidence
