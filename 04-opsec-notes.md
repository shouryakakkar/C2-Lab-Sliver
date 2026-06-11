# OPSEC Notes

This is what separates a professional red team 
report from a basic tool demo.

## What We Did That's Detectable
| Action | Detection Method |
|--------|-----------------|
| Python HTTP server on 8080 | Network traffic analysis |
| beacon.exe dropped to C:\Tools | EDR file monitoring |
| SmartScreen warning triggered | Windows event logs |
| HTTP beacon every 60 seconds | Periodic connection pattern |
| Sliver default certificate | TLS fingerprinting |

## How a Blue Team Would Catch This
- **SIEM alert:** Periodic outbound HTTP to 
  unknown IP every ~60 seconds
- **EDR:** unsigned executable dropped and run 
  from C:\Tools
- **Event ID 4688:** New process created 
  (beacon.exe)
- **Network:** Unusual HTTP POST requests to 
  non-standard port 6789

## How to Improve OPSEC in Real Engagement
- Use HTTPS instead of HTTP
- Use domain fronting to hide C2 traffic
- Migrate beacon to a legitimate process 
  (explorer.exe, svchost.exe)
- Use longer beacon intervals (4-8 hours)
- Sign the beacon binary
- Use named pipe communication instead of HTTP