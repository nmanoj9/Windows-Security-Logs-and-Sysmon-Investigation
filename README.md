# Windows Security Logs and Sysmon Investigation

## Project Overview

This project demonstrates a SOC Analyst investigation using Windows Security Logs and Sysmon logs. The objective was to analyze authentication activity, detect failed login attempts, investigate process creation and termination events, review network connections, and perform event correlation.

---

## Objectives

- Investigate Windows Security Event ID 4624 (Successful Logon)
- Investigate Windows Security Event ID 4625 (Failed Logon)
- Detect potential brute-force authentication activity
- Analyze Sysmon Event ID 1 (Process Creation)
- Analyze Sysmon Event ID 3 (Network Connection)
- Analyze Sysmon Event ID 5 (Process Termination)
- Perform event correlation and investigation
- Document findings using SOC analyst methodology

---

## Tools Used

- Windows Event Viewer
- Sysmon
- Windows Security Logs
- Notepad
- GitHub

---

## Log Sources

### Windows Security Logs

- Event ID 4624 – Successful Logon
- Event ID 4625 – Failed Logon

### Sysmon Logs

- Event ID 1 – Process Creation
- Event ID 3 – Network Connection
- Event ID 5 – Process Termination

---

## Investigation Workflow

1. Reviewed Windows Security Logs.
2. Identified successful authentication events (4624).
3. Investigated failed authentication events (4625).
4. Performed brute-force activity analysis.
5. Reviewed Sysmon process creation events.
6. Investigated Sysmon network connection events.
7. Analyzed Sysmon process termination events.
8. Correlated authentication and Sysmon activity.
9. Documented findings and conclusions.

---

## Key Findings

### Event ID 4625 – Failed Logons

- Multiple failed login attempts were observed.
- Activity resembled password-guessing or brute-force behavior.
- No confirmed account compromise was identified.

### Event ID 4624 – Successful Logons

- Successful authentication events were observed.
- No direct correlation with failed login activity was confirmed.

### Sysmon Event ID 1

- Process creation activity was captured successfully.
- Notepad.exe execution was identified and analyzed.

### Sysmon Event ID 3

- Outbound HTTPS network communication was detected.
- OneDrive.exe generated a legitimate network connection.

### Sysmon Event ID 5

- Process termination activity was captured successfully.
- Process termination visibility was validated.

---

## MITRE ATT&CK Mapping

| Technique ID | Technique Name | Evidence |
|-------------|---------------|----------|
| T1110 | Brute Force | Multiple failed logon attempts (Event ID 4625) |
| T1078 | Valid Accounts | Successful authentication activity (Event ID 4624) |
| T1071 | Application Layer Protocol | HTTPS network communication observed in Sysmon Event ID 3 |

---

## Skills Demonstrated

- Security Monitoring
- Log Analysis
- Event Investigation
- Event Correlation
- Authentication Analysis
- Windows Security Logging
- Sysmon Analysis
- SOC Analyst Methodology
- Incident Investigation Documentation

---

## Repository Structure

```text
Investigation_Notes/
├── Windows Security Log Investigation Notes
├── Brute Force Detection Notes
├── Event Analysis Notes
├── Correlation Analysis
└── Final Investigation Report

Screenshots/
├── Event Viewer Evidence
├── Sysmon Evidence
├── Detection Screenshots
└── Investigation Screenshots
```

---

## Conclusion

This project demonstrates practical SOC Analyst skills through Windows Security Log analysis and Sysmon investigation. Multiple authentication events, process executions, network connections, and process termination events were analyzed and correlated. No confirmed malicious activity was identified during the investigation, and observed activity remained consistent with expected system and user behavior.

---
