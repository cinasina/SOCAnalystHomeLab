# Splunk Deployment & First Log Ingestion

This module focused on deploying Splunk Enterprise and validating the first Windows Event Log ingestion pipeline.

## What I Learned

- The basic role of Splunk Enterprise.
- What the Splunk Universal Forwarder does on a Windows endpoint.
- How forwarded events reach Splunk over TCP/9997.
- What an index is and why I created a dedicated `windows` index.
- The basic meaning of:
  - `host`
  - `source`
  - `sourcetype`
  - `EventCode`
  - `_time`
- How to verify that Windows Event Logs are actually reaching Splunk.

## Lab

I installed Splunk Enterprise on an Ubuntu Server virtual machine and installed Splunk Universal Forwarder on my Windows system.

For this first ingestion test, I collected only the Windows **System** Event Log to keep the lab simple and avoid collecting unnecessary personal security data.

The data flow used in this lab was:

`Windows System Event Log → Splunk Universal Forwarder → TCP/9997 → Splunk Enterprise → index=windows → Search`

I verified the ingestion with:

```spl
index=windows
```

The returned events showed `WinEventLog:System` as the source/sourcetype, confirming that the forwarding pipeline was working.

## Evidence

- `screenshots/07-windows-system-events-ingested.png`

## Setup & Troubleshooting Notes

A detailed reproduction and troubleshooting guide is available here:

- `docs/splunk-enterprise-windows-forwarder-lab-guide.txt`

This guide contains the setup steps and issues I encountered while building the lab.
