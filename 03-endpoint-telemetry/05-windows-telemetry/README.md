# Windows Endpoint Telemetry

This module focused on understanding where Windows security telemetry comes from.

## What I Learned

- The main Windows Event Viewer areas:
  - Security
  - System
  - Application
  - Applications and Services Logs
- The difference between native Windows Event Logs and Sysmon telemetry.
- Why Sysmon can provide additional visibility into endpoint activity.
- How to find Sysmon events in Windows Event Viewer.
- How to inspect a Sysmon Process Create event.
- Important process fields such as:
  - Image
  - Parent process
  - Command line
  - User
  - Process ID
  - Time

## Lab

I installed Sysmon on Windows and inspected process creation activity in:

`Applications and Services Logs → Microsoft → Windows → Sysmon → Operational`

This helped me understand how endpoint activity is recorded locally before it is sent to a SIEM.

## Evidence

- `evidence/05-sysmon-process-create.png`