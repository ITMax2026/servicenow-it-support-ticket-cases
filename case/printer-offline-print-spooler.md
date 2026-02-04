# Case Study: Printer Showing "Offline" Due to Print Spooler Issue

## Incident Summary
**User Report:** User was unable to print critical financial reports to network printer PRN-ACC-01. The printer displayed as "Offline" on the user's Windows 11 workstation, despite other users in the department being able to print successfully.

---

## Environment
* OS: Windows 11 Workstation
* Hardware: Network Printer (PRN-ACC-01)
* Infrastructure: Corporate Print Server

## Symptoms
* Printer status consistently showed as "Offline" in the Windows Settings and Control Panel.
* New print jobs failed to send and remained in the queue.
* Network connectivity (Ping) to the printer’s IP address was stable.
* The issue was isolated to a single workstation; other users could print to PRN-ACC-01 without issue.

## Troubleshooting Steps
1. **Initial Verification:** Remoted into the user workstation and confirmed the "Offline" status. 
2. **Queue Analysis:** Checked the local print queue and identified a stuck 200MB PDF document that had been pending for several hours.
3. **Service Diagnostics:** Attempted to cancel the stuck document, but the print queue was unresponsive.
4. **Service Restart:** Opened `services.msc` and restarted the **Print Spooler** service to clear the application hang.
5. **Configuration Check:** Verified that the printer port was correctly configured to the standard TCP/IP address and had not reverted to a WSD port.
6. **Printer Re-installation:** Removed the local instance of the printer and re-added it from the corporate print server to ensure a fresh connection and driver initialization.

## Root Cause
**Unresponsive Print Spooler service.** A large, complex print job (200MB PDF) caused the local Print Spooler service to hang, preventing the workstation from communicating with the print server and resulting in an "Offline" status.

## Resolution
* **Action:** Restarted the Windows Print Spooler service, manually cleared the stuck print job from the spool folder, and re-added the printer from the print server.
* **Result:** The printer status immediately returned to "Ready." 
* **Confirmation:** Successfully printed a test page and verified the user could print their financial reports.

## Verification
- [x] Test page printed successfully.
- [x] Printer status returned to "Ready" on the workstation.
- [x] User confirmed the ability to print reports and resumed normal operations.

---

## Skills Demonstrated
* Windows Print Spooler Troubleshooting
* Print Queue Management
* Network Printer Configuration
* Remote Desktop Support
* ServiceNow Documentation
* Business Impact Awareness
