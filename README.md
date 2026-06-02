# SOC Home Lab – Security Operations Center Simulation

## Overview

This project demonstrates the design, deployment, and operation of a Security Operations Center (SOC) Home Lab using Splunk Enterprise, Windows 10, Kali Linux, and Ubuntu. The objective was to simulate a real-world SOC environment for log collection, threat detection, alerting, and incident investigation.

The lab was built entirely in a controlled virtual environment using Oracle VirtualBox and was designed to replicate common SOC analyst workflows, including monitoring security events, detecting malicious activity, and investigating alerts.

---

## Objectives

* Build a functional SOC environment using free and open-source tools.
* Configure centralized log collection and analysis.
* Simulate realistic cyber attacks in a safe lab environment.
* Create detection rules and alerts in Splunk.
* Practice incident investigation and response workflows.

---

## Lab Architecture

### Machines Used

| Machine          | Role                | IP Address    |
| ---------------- | ------------------- | ------------- |
| Splunk-SIEM      | SIEM & Log Server   | 192.168.56.10 |
| Windows10-Victim | Target & Log Source | 192.168.56.20 |
| Kali-Attacker    | Attack Simulation   | 192.168.56.30 |

### Technologies

* Splunk Enterprise
* Splunk Universal Forwarder
* Ubuntu 22.04 LTS
* Windows 10 Pro
* Kali Linux
* Oracle VirtualBox
* Windows Event Logs

---

## Project Workflow

1. Configure an isolated VirtualBox network.
2. Deploy Ubuntu, Windows, and Kali virtual machines.
3. Install and configure Splunk Enterprise.
4. Configure Splunk Universal Forwarder on Windows.
5. Forward Windows Event Logs to Splunk.
6. Simulate attacks from Kali Linux.
7. Create detection queries and alerts.
8. Investigate security events using Splunk.

---

## Simulated Attacks

### Nmap Service Scan

Performed network reconnaissance and service enumeration against the target system.

**Detection Method**

* Network activity monitoring
* Windows Firewall event analysis
* Splunk search queries

### Hydra RDP Brute Force Attack

Simulated password guessing attempts against the Windows RDP service.

**Detection Method**

* Windows Event ID 4625
* Failed authentication monitoring
* Automated Splunk alert generation

---

## Detection Engineering

Custom SPL queries were developed to identify:

* Port scanning activity
* Multiple failed login attempts
* Potential brute-force attacks
* Suspicious authentication behavior

Alerts were configured to automatically notify the analyst when predefined thresholds were exceeded.

---

## Incident Investigation

For each detected attack:

* Alert validation was performed.
* Source IP addresses were identified.
* Authentication logs were reviewed.
* Attack timelines were reconstructed.
* Appropriate response actions were documented.

---

## Skills Demonstrated

* SIEM Operations
* Splunk Administration
* Log Management
* Threat Detection
* Security Monitoring
* Alert Tuning
* Incident Response
* Network Security
* Windows Event Analysis
* SOC Analyst Workflows

---

## Key Learning Outcomes

* Understanding of SOC operations and monitoring processes.
* Hands-on experience with Splunk SIEM.
* Real-time log collection and analysis.
* Detection engineering using SPL queries.
* Investigation of simulated cyber attacks.
* Practical exposure to incident response procedures.

---

## Disclaimer

All activities documented in this project were conducted within a controlled and isolated laboratory environment for educational purposes only. No third-party systems, production environments, or external networks were targeted.

