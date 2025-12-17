## Wazuh Rule Mapping - SSH Brute Force

This section maps the SSH brute-force detection logic to a Wazuh-style rule.

### Rule Description
Detect multiple failed SSH login attempts from the same source IP.

### Relevant Log Field
- Program: sshd
- Message: "Failed password"
- Source IP address

### Example Wazuh Rule (Conceptual)

<rule id="100001" level="8">
  <if_matched_sid>5710</if_matched_sid>
  <same_source_ip />
  <description>SSH brute-force attack detected from same IP</description>
  <frequency>5</frequency>
  <timeframe>60</timeframe>
</rule>

### Alert Severity
High

### SOC Response
- Investigate source IP
- Check for successful login attempts
- Block IP if malicious
