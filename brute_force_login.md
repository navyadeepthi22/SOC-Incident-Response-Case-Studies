# Multiple Failed Login Attempts Detected

## Incident Type
Brute Force / Unauthorized Login Attempts

## Alert Description
The SOC alert was triggered when multiple failed login attempts were detected on a user account within a short time period. The source IP was unfamiliar and attempts occurred during off-hours.

## Assets Involved
- User Account: J. Doe
- Source IP: 203.0.113.45
- Host / Device: LPT-HR-042
- Network Segment: VPN / Remote Access

## Initial Assessment
The activity originated from an external IP address not previously observed in login history. Login attempts occurred between 2:00 AM and 3:00 AM, increasing suspicion. The user belongs to the HR department, which handles sensitive data.

## Evidence Observed
- 7 failed login attempts within 10 minutes
- No successful login from the source IP
- Source IP not recognized in previous login records

## MITRE ATT&CK Mapping
- Tactic: Credential Access
- Technique: Brute Force (T1110)

## Decision
True Positive – Escalate to Tier-2

## Recommended Actions
- Escalate the incident to a Tier-2 SOC analyst
- Temporarily lock the affected user account
- Review VPN and firewall logs for additional suspicious activity
- Notify the user and IT security team