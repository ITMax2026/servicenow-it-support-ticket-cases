# Case Study: Wi-Fi Connection Dropping in Conference Room B

## Incident Summary
**User Report:** User reports that their Wi-Fi connection consistently drops when working in Conference Room B, while the connection remains stable in all other areas of the building.

---

## Environment
* OS: Windows 10/11 Laptop
* Network: Corporate Wi-Fi (SSID)
* Location: Conference Room B

## Symptoms
* Wi-Fi disconnects repeatedly and specifically within Conference Room B.
* The device reconnects normally immediately upon leaving the room.
* No connectivity issues reported by the user in other parts of the office.

## Troubleshooting Steps
1. **Initial Verification:** Confirmed with the user that the drops are location-specific. Verified that the device maintains a stable connection in the main workspace.
2. **Network Health Check:** Reviewed the network monitoring dashboard and ServiceNow outage board; confirmed no known wide-scale wireless outages or scheduled maintenance.
3. **Local Device Reset:** Reset the wireless adapter on the user's device to rule out a hung driver or local hardware state issue.
4. **Profile Refresh:** Had the user "Forget" the corporate SSID and reconnect to establish a fresh lease and profile.
5. **Physical Testing:** Tested the connection inside Conference Room B (issue reproduced) and then moved immediately outside the room (connection stabilized). 
6. **Diagnostic:** Confirmed that the issue is isolated to the specific physical location, pointing to a localized infrastructure fault.

## Root Cause
**Wireless Access Point (AP) coverage issue or malfunction.** The behavior indicates either a "dead zone" caused by physical interference in the room or a hardware malfunction of the specific Access Point serving that area.

## Resolution
* **Action:** Documented all troubleshooting steps and findings. Escalated the incident to the Network Infrastructure Team.
* **Result:** Requested a physical inspection and signal strength analysis (Heat Map) for Conference Room B to determine if the AP requires replacement or reconfiguration.
* **Interim:** Advised user of the escalation and suggested alternative workspaces until the network team confirms a fix.

---

## Skills Demonstrated
* Network Troubleshooting
* Isolation by Location
* Wireless Diagnostics
* Proper Escalation Procedures
* ServiceNow Documentation
* User Communication
