# C2 Lab — Sliver Command & Control Framework

## Overview
A home lab simulating real-world red team C2 operations 
using Sliver framework against a domain-joined Windows 11 
target. All activity performed in an isolated VMware lab 
environment.

## Lab Architecture
- **C2 Server:** Kali Linux (Sliver v1.7.3)
- **Target:** Windows 11 Enterprise (DESKTOP-0CLPOBP)
- **Domain:** lab.local
- **Compromised User:** LAB\jsmith
- **C2 Channel:** HTTP beacon

## Attack Summary
| Phase | Detail | Status |
|-------|--------|--------|
| Listener Setup | HTTP on port 6789 | ✅ |
| Beacon Generation | windows/amd64 implant | ✅ |
| Beacon Delivery | Python HTTP server | ✅ |
| C2 Session | LAB\jsmith checked in | ✅ |
| Post-Exploitation | whoami, info, pwd, ps | ✅ |
| AV Evasion | SmartScreen bypassed | ✅ |

## MITRE ATT&CK Mapping
| TTP | ID | Detail |
|-----|----|--------|
| Command and Control | T1071.001 | HTTP C2 channel |
| Ingress Tool Transfer | T1105 | beacon.exe delivery |
| Native API | T1106 | Sliver beacon execution |
| System Owner Discovery | T1033 | whoami → LAB\jsmith |
| Process Discovery | T1057 | ps command |

<img width="1370" height="713" alt="image" src="https://github.com/user-attachments/assets/33d5c1a8-f21b-47b0-9e50-a68ef576a553" />
<img width="1001" height="806" alt="image" src="https://github.com/user-attachments/assets/8d74208a-51fa-4fc2-8d6b-fed7b97cbb8a" />
