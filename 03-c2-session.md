# C2 Session — Post Exploitation

**MITRE ATT&CK:** T1033, T1057, T1082

## Beacon Check-In
<img width="1703" height="312" alt="image" src="https://github.com/user-attachments/assets/e4dbe5a1-aa89-48aa-ae59-dbdcfbfa3375" />


Two beacons visible — showing persistent access 
established on the target machine.

## Selecting the Beacon
use 5f670cb2

## Post-Exploitation Commands

### Identity Confirmation
whoami
→ Logon ID: LAB\jsmith


<img width="671" height="131" alt="image" src="https://github.com/user-attachments/assets/c510568d-507e-4a11-9f6d-243e35908d19" />


### System Information
info
[INSERT SCREENSHOT → PDF showing full info output:
- Beacon ID: 5f670cb2
- Hostname: DESKTOP-0CLPOBP
- Username: LAB\jsmith
- OS: windows 10 build 26200 x86_64
- Arch: amd64
- Active C2: https://192.168.30.138:6789
- Interval: 1m0s
- First Contact: Thu Jun 11 09:01:42 IST 2026
- Last Checkin: Thu Jun 11 09:01:43 IST 2026]

### Process Discovery
ps
getuid
pwd


<img width="715" height="782" alt="image" src="https://github.com/user-attachments/assets/6c8080b6-a63e-4651-9781-66c5cc4ca458" />

## Session Summary
Full C2 access established over HTTP to domain 
machine DESKTOP-0CLPOBP as LAB\jsmith with 
1 minute beacon interval and 30 second jitter.
