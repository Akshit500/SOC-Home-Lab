# Incident Report — INC-001

| Field | Details |
|-------|---------|
| Incident ID | INC-001 |
| Date | 20 May 2026 |
| Analyst | Akshit Rawat |
| Severity | High |
| Status | Resolved |
| Type | Brute Force Attack |

---

## Executive Summary
A brute force attack was detected against a Windows 10 endpoint.
The attack originated from an internal Kali Linux machine used for
simulation purposes. Wazuh SIEM successfully detected and alerted
on the activity within seconds of the attack beginning.

---

## Timeline of Events

| Time | Event |
|------|-------|
| 12:30:00 | Hydra brute force initiated from Kali Linux |
| 12:30:03 | First failed login recorded (Event ID 4625) |
| 12:30:05 | 20+ failed attempts detected by Wazuh |
| 12:30:06 | Wazuh Rule 5710 triggered — High severity alert |
| 12:31:00 | Attack simulation stopped |
| 12:32:00 | Alert reviewed and investigated on dashboard |

---

## Affected Systems
- **Hostname:** DESKTOP-WIN10
- **IP Address:** 192.168.x.x
- **OS:** Windows 10

---

## Attack Details
- **Attack Type:** RDP Brute Force
- **Source IP:** 192.168.x.x (Kali Linux)
- **Tool Used:** Hydra
- **Targeted Account:** Administrator
- **Total Failed Attempts:** 50+

---

## Detection
- **SIEM:** Wazuh
- **Rule Triggered:** 5710 — Multiple failed logins
- **Alert Level:** 10 (High)
- **Event IDs:** 4625 (Failed Logon)

---

## Response Actions
1. Identified source IP from Wazuh alert
2. Confirmed brute force pattern from login frequency
3. Reviewed Windows Security Event logs
4. Confirmed no successful login occurred
5. Documented findings in this report

---

## Recommendations
1. Enable account lockout policy (lock after 5 failed attempts)
2. Disable RDP if not required
3. Restrict RDP access to trusted IPs only
4. Enable MFA for remote access
5. Set up automated email alerting for Level 10+ Wazuh alerts

---

## Conclusion
The Wazuh SIEM successfully detected the brute force attack in real time.
No unauthorized access occurred. Preventive controls recommended above
should be implemented to reduce risk in a production environment.
