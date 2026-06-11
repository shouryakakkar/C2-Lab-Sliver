# Listener Configuration

**MITRE ATT&CK:** T1071.001 — Application Layer 
Protocol: Web Protocols

## Starting HTTP Listener
Port 80 was in use so used port 6789:
http --lport 6789

[INSERT SCREENSHOT → PDF showing:
"[+] Starting HTTP :6789 listener"
"[+] Successfully started job #3"]

## Why HTTP C2?
- Blends with normal web traffic
- Less likely to trigger firewall rules than 
  raw TCP
- Harder to distinguish from legitimate browsing
  in basic network monitoring