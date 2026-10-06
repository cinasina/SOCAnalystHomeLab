# SOC Analyst Home Lab

This repository documents my hands-on SOC learning journey.

The goal of this project is to build practical SOC analyst skills through endpoint telemetry, SIEM labs, log analysis, network visibility, investigation, and detection exercises.

## Current Progress

So far, I have worked on:

- Building an evidence-based SOC investigation mindset.
- Investigating unknown processes and activity without relying on assumptions.
- Deploying my first SIEM lab with Wazuh.
- Connecting Windows and Linux endpoints using Wazuh agents.
- Learning where Windows Event Logs come from and using Sysmon for additional endpoint telemetry.
- Getting familiar with Wireshark and inspecting sample DNS, TCP, and HTTP packet captures.
- Deploying Splunk Enterprise on an Ubuntu Server.
- Connecting a Windows endpoint using Splunk Universal Forwarder.
- Ingesting Windows System Event Logs into a dedicated Splunk index.
- Practicing basic SPL searches and exploring Windows event fields.

## Current Lab Architecture

Windows Endpoint  
↓  
Splunk Universal Forwarder  
↓  
TCP/9997  
↓  
Splunk Enterprise  
↓  
Windows Index  
↓  
SPL Search

## Next Steps

The next stages of the project will focus on:

- Windows Security Logs and Sysmon in Splunk.
- Authentication and process investigations.
- Attack simulation and log analysis.
- Detection engineering and false-positive tuning.
- Splunk BOTS investigation datasets.
- Incident triage, correlation, and reporting.

## Project Status

**In Progress**