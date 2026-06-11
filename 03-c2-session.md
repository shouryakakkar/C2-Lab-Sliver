# C2 Session — Post Exploitation

**MITRE ATT&CK:** T1033, T1057, T1082

## Beacon Check-In
[INSERT SCREENSHOT → PDF showing beacons table:
"INADEQUATE_CONSONANT - DESKTOP-0CLPOBP - 
LAB\jsmith - windows/amd64 - Next Check-In: 1m7s"]

Two beacons visible — showing persistent access 
established on the target machine.

## Selecting the Beacon
use 5f670cb2

## Post-Exploitation Commands

### Identity Confirmation
whoami
→ Logon ID: LAB\jsmith
[INSERT SCREENSHOT → PDF showing:
"whoami → Logon ID: LAB\jsmith"]

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
[INSERT SCREENSHOT → PDF showing ps, getuid, 
pwd commands being tasked]

## Session Summary
Full C2 access established over HTTP to domain 
machine DESKTOP-0CLPOBP as LAB\jsmith with 
1 minute beacon interval and 30 second jitter.