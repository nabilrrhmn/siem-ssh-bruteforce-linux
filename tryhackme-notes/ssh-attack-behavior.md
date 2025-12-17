## TryHackMe-Inspired SSH Attack Behavior Analysis

### Objective
This document summarizes SSH brute-force attacker behavior observed during hands-on security labs and translates it into blue team detection and response insights.

### Attacker Behavior Observed
- Multiple SSH login attempts in rapid succession
- Use of common usernames such as root, admin, test
- Repeated authentication failures from the same source IP
- Automated tools rather than manual login attempts

### Log Evidence
These behaviors generate repeated "Failed password" entries in Linux authentication logs (auth.log), which can be correlated by source IP and time window.

### Detection Opportunities
- Count failed login attempts per source IP
- Identify short timeframes between attempts
- Alert when thresholds are exceeded

### Blue Team Perspective
Rather than focusing on exploitation success, defenders prioritize early detection, alerting, and prevention before account compromise occurs.

### Mitigation Strategies
- Enforce SSH key-based authentication
- Disable root login over SSH
- Implement rate limiting (e.g., fail2ban)
- Monitor and alert on repeated failures
