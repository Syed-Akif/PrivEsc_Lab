# Incident Report: Privilege Escalation Detected

## Summary
A privilege escalation attempt was detected on an Ubuntu endpoint monitored by Wazuh SIEM.  
The activity involved creation of a new user and abuse of sudo privileges.

## Timeline
- User account created on the system
- User added to sudo group
- Passwordless sudo access configured
- Successful sudo execution detected

## Detection
- Linux auditd captured privilege-related events
- Wazuh correlated logs and raised alerts
- MITRE ATT&CK techniques identified

## MITRE ATT&CK Mapping
- T1136 – Create Account
- T1548.003 – Abuse Elevation Control Mechanism

## Impact
Unauthorized root-level access could allow full system compromise.

## Mitigation
- Remove unauthorized user
- Audit sudoers files
- Review access control policies
- Enable continuous monitoring

## Status
Incident contained and documented.
