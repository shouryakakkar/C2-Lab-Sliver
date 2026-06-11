# Listener Configuration

**MITRE ATT&CK:** T1071.001 — Application Layer 
Protocol: Web Protocols

## Starting HTTP Listener
Port 80 was in use so used port 6789:
http --lport 6789

<img width="591" height="123" alt="image" src="https://github.com/user-attachments/assets/331dd1bc-f061-4577-a309-5f01cac7abc7" />


## Why HTTP C2?
- Blends with normal web traffic
- Less likely to trigger firewall rules than 
  raw TCP
- Harder to distinguish from legitimate browsing
  in basic network monitoring
