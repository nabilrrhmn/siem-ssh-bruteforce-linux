## Incident Summary
A brute-force SSH attack was detected based on multiple failed login attempts from a single IP address 
within a short time period.

## Timeline
- 10:01 Multiple failed SSH login attempts detected
- 10:02 SIEM alert triggered
- 10:05 SOC investigation initiated

## Indicators of Compromise
- Source IP: 192.168.1.50
- Target service: SSH
- Affected system: Linux server

## Impact Assessment
No successful unauthorized login was detected. The attack was limited to failed authentication attempts.

## Response Actions
- Blocked source IP at firewall level
- Increased monitoring for further attempts

## Recommendations
- Enforce SSH key-based authentication
- Disable root login via SSH
- Implement rate limiting using fail2ban
