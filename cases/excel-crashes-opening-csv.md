# Case Study: Excel Crashes When Opening CSV Files

## Incident Summary
**User Report:** User reported that Microsoft Excel crashes immediately whenever they attempt to open any .csv file. 

---

## Environment
* OS: Windows 10/11
* Software: Microsoft Excel (Microsoft 365 Desktop App)

## Symptoms
* Excel crashes immediately upon opening .csv files.
* The issue is consistent across multiple different CSV files.
* Web-based Office apps and other desktop Office apps (Word, Outlook) are unaffected.

## Troubleshooting Steps
1. **Initial Verification:** Contacted the user and screenshared to confirm the crash. Verified that the issue was isolated to the desktop version of Excel.
2. **Service Check:** Checked the ServiceNow outage board; confirmed no active Microsoft 365 service-wide issues.
3. **Safe Mode:** Launched Excel in Safe Mode (excel /safe) to rule out third-party add-ins. The issue persisted, suggesting a core application fault rather than a plugin conflict.
4. **Diagnostic:** Identified that the crash behavior pointed toward corrupted Office application components or DLLs.

## Root Cause
**Corrupted Microsoft Office application components.** A specific set of libraries used for file parsing was failing, causing the application to terminate unexpectedly during the file-open process.

## Resolution
* **Action:** Performed a Microsoft Office 365 Quick Repair via the Control Panel (Apps & Features).
* **Result:** After the repair finished, Excel was able to open the CSV files successfully without crashing.
* **Confirmation:** User tested several files and confirmed the application is functioning normally.

## Verification
- [x] CSV files open successfully.
- [x] Excel no longer crashes on launch.
- [x] User confirmed resolution.

---

## Skills Demonstrated
* Application Troubleshooting
* Microsoft Office 365 Support
* Isolation and Root Cause Analysis (RCA)
* User Communication
* Technical Documentation
