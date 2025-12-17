## Detection Name
SSH Brute Force Attempt

## Log Source
Linux authentication log (auth.log)

## Detection Logic
Trigger an alert when more than 5 failed SSH login attempts from the same IP address occur within 1 minute.

## Detection Method
- Monitor "Failed password" events
- Group events by source IP
- Count attempts over a short time window

## Why This Is Suspicious
Normal users rarely fail authentication repeatedly within a short time frame. 
Multiple rapid failures typically indicate automated brute-force activity.

## Possible False Positives
- Misconfigured scripts
- User repeatedly typing incorrect credentials

## Severity
Medium
