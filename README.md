# 🛡️ Atomic Red Team Detection Lab

## Overview

The objective of this lab is to simulate real-world attack techniques, collect endpoint telemetry, and build detections mapped to the **MITRE ATT&CK framework**.

This project focuses on:

- Cross-platform persistence techniques
- Command execution monitoring
- Host-based detection engineering
- Alert triage using authentication and system logs
- MITRE ATT&CK mapping

---

## Lab Architecture

**Attack Simulation**
- Atomic Red Team (Linux & Windows endpoints)

**Telemetry Collection**
- Wazuh Agent
- Splunk Universal Forwarder

**Detection Platforms**
- Wazuh (custom rules)
- Splunk (SPL alerts)

---

## 🧰 Brief Setup

### 1️⃣ Infrastructure
- Ubuntu Linux VM
- Windows  VM
- Splunk Enterprise (Docker container)
- Wazuh 

### 2️⃣ Endpoint Configuration
- Installed Wazuh Agent on Linux and Windows
- Installed Splunk Universal Forwarder on both systems
- Configured log forwarding to Splunk index
- Enabled required log sources

### 3️⃣ Log Sources

**Linux**
- `/var/log/syslog`
- `/var/log/auth.log`
- `/var/log/audit/audit.log`

**Windows**
- Security Event Log
- PowerShell Operational Log
- Sysmon (optional)

### 4️⃣ Attack Simulation
- Installed Atomic Red Team
- Executed selected MITRE ATT&CK techniques
- Validated telemetry in Wazuh and Splunk
- Built detection rules and alerts

---

## Techniques Covered

### 🐧 Linux
- T1053.003 – Cron Persistence
- T1059.004 – Unix Shell Execution
- T1547 – Boot or Logon Autostart Execution

➡️ See full Linux implementation: [`/linux`](./linux)

### 🪟 Windows
- T1053.005 – Scheduled Task Persistence
- T1059.001 – PowerShell Execution
- T1547.001 – Registry Run Key Persistence

➡️ See full Windows implementation: [`/windows`](./windows)

---
<!---
## Screenshots

### Architecture
_Add architecture diagram here_

### Wazuh Alerts
_Add Wazuh detection screenshots here_

### Splunk Detections
_Add Splunk search/alert screenshots here_

### Atomic Red Team Execution
_Add Atomic execution screenshots here_

---

## Repository Structure

