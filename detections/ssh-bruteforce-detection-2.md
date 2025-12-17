## Detection Logic (Conceptual)

title: SSH Brute Force Attempt
id: ssh-bruteforce-linux-001
status: experimental
description: Detects multiple failed SSH login attempts from a single IP address within a short time window.
author: Muhammad Nabilfikri bin Abdul Rahman
logsource:
  product: linux
  service: ssh

detection:
  selection:
    message|contains: "Failed password"
  condition: selection | count(source.ip) > 5 within 1 minute

falsepositives:
  - User repeatedly entering wrong password
  - Misconfigured automation scripts

level: medium
