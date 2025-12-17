## Lateral Movement Detection Signals

### Attacker Behavior Observed
- Authentication attempts across multiple systems
- Repeated access attempts using same credentials
- Movement follows initial access attempts

### Log Evidence
SSH logs combined with authentication timestamps can indicate potential lateral movement attempts.

### Detection Opportunities
- Monitor same user logging into multiple hosts rapidly
- Alert on authentication spread patterns
- Correlate source IPs across hosts

### Blue Team Insight
Early detection of lateral movement reduces blast radius and limits attacker persistence.

### Mitigation Strategies
- Network segmentation
- Centralized logging
- Alerting on abnormal authentication patterns
