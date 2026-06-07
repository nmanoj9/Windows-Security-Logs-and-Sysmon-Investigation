# Windows Security Logs and Sysmon Investigation

## Project Overview

This project demonstrates a SOC Analyst investigation using Windows Security Logs and Sysmon logs. The objective was to analyze authentication activity, detect failed login attempts, investigate process creation and termination events, review network connections, and perform event correlation.

---

## Objectives

* Investigate Windows Security Event ID 4624 (Successful Logon)
* Investigate Windows Security Event ID 4625 (Failed Logon)
* Detect potential brute-force authentication activity
* Analyze Sysmon Event ID 1 (Process Creation)
* Analyze Sysmon Event ID 3 (Network Connection)
* Analyze Sysmon Event ID 5 (Process Termination)
* Perform event correlation and investigation
* Document findings using SOC Analyst methodology

---

## Tools Used

* Microsoft Windows 11
* Windows Event Viewer
* Sysmon

---

## Log Sources

### Windows Security Logs

* Event ID 4624 – Successful Logon
* Event ID 4625 – Failed Logon

### Sysmon Logs

* Event ID 1 – Process Creation
* Event ID 3 – Network Connection
* Event ID 5 – Process Termination

---

## Investigation Workflow

1. Reviewed Windows Security Logs.
2. Identified successful authentication events (Event ID 4624).
3. Investigated failed authentication events (Event ID 4625).
4. Performed brute-force activity analysis.
5. Reviewed Sysmon process creation events.
6. Investigated Sysmon network connection events.
7. Analyzed Sysmon process termination events.
8. Correlated authentication and Sysmon activity.
9. Documented findings and conclusions.

---

## Key Findings

### Event ID 4625 – Failed Logons

* Multiple failed login attempts were observed.
* Activity resembled password-guessing or brute-force behavior.
* No confirmed account compromise was identified.

### Event ID 4624 – Successful Logons

* Successful authentication events were observed.
* No confirmed account compromise or malicious authentication activity was identified.

### Sysmon Event ID 1 – Process Creation

* Process creation activity was captured successfully.
* Notepad.exe execution was identified and analyzed.
* Sysmon logging functionality was validated.

### Sysmon Event ID 3 – Network Connection

* Outbound HTTPS network communication was detected.
* OneDrive.exe generated a legitimate network connection.
* Network visibility through Sysmon was successfully validated.

### Sysmon Event ID 5 – Process Termination

* Process termination activity was captured successfully.
* Process lifecycle visibility was validated.
* Sysmon successfully recorded process termination events.

---

## MITRE ATT&CK Mapping

| Technique ID | Technique Name             | Evidence                                                  |
| ------------ | -------------------------- | --------------------------------------------------------- |
| T1110        | Brute Force                | Multiple failed logon attempts (Event ID 4625)            |
| T1078        | Valid Accounts             | Successful authentication activity (Event ID 4624)        |
| T1071        | Application Layer Protocol | HTTPS network communication observed in Sysmon Event ID 3 |

### MITRE ATT&CK Analysis

* **T1110 (Brute Force):** Multiple failed authentication attempts were identified during Windows Security Log analysis.
* **T1078 (Valid Accounts):** Successful authentication activity was observed through Event ID 4624 investigations.
* **T1071 (Application Layer Protocol):** HTTPS communication activity was observed through Sysmon Event ID 3 network connection monitoring.

---

## Skills Demonstrated

* Security Monitoring
* Windows Event Log Analysis
* Sysmon Analysis
* Authentication Investigation
* Event Correlation
* Threat Detection
* Incident Investigation
* SOC Analyst Methodology
* Security Documentation
* Windows Security Monitoring

---

## Conclusion

This project demonstrates practical SOC Analyst skills through Windows Security Log analysis and Sysmon investigation. Authentication events, process executions, network connections, and process termination activities were analyzed and correlated to understand system behavior. No confirmed malicious activity was identified during the investigation, and the observed events were consistent with expected system and user activity. The project successfully validated visibility across multiple Windows log sources and demonstrated a structured SOC investigation workflow.

---

## Project Status

**Completed**
