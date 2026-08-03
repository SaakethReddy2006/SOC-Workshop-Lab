# 🦖 Velociraptor Offline Collector

## Overview

Velociraptor was used to build an Offline Collector capable of collecting forensic evidence from a Windows endpoint without installing a permanent agent.

The generated collector acquires system artifacts and packages them into a ZIP archive for offline forensic analysis.

---

# Architecture

```
Velociraptor Server
        │
        ▼
Generate Offline Collector
        │
        ▼
Run Collector on Windows
        │
        ▼
Collect Artifacts
        │
        ▼
Generate Evidence ZIP
```

---

# Artifacts Collected

- Generic.Client.Info
- Generic.System.Pstree
- Windows.Network.Netstat
- Windows.System.Services
- Windows.EventLogs.Evtx

---

# Demonstration

## 1. Velociraptor Dashboard

<img width="788" height="356" alt="dashboard" src="https://github.com/user-attachments/assets/65f451bd-c7b8-4024-81aa-3747c00600ba" />
The Velociraptor web interface provides centralized management for digital forensic and incident response (DFIR) activities. From this dashboard, investigators can create offline collectors, manage clients, launch artifact collections, and review forensic evidence collected from Windows endpoints.

---

## 2. Configure Offline Collector

<img width="704" height="327" alt="configuration" src="https://github.com/user-attachments/assets/40a836f5-89b5-4ac2-8307-d2f2610b0b1d" />
The Offline Collector was configured to acquire key Windows forensic artifacts without installing a permanent agent on the endpoint. The selected artifacts included client information, process hierarchy, network connections, installed services, and Windows Event Logs, providing a comprehensive snapshot of the system.

---

## 3. Review Request

<img width="709" height="333" alt="Screenshot 2026-08-03 120733" src="https://github.com/user-attachments/assets/7f86be01-9111-4848-abc4-f009dc3982f2" />
Before generating the collector, Velociraptor displays the complete collection request in JSON format. This verification step confirms that the selected artifacts and configuration parameters are correct before building the standalone executable.
Velociraptor generated a standalone Offline Collector executable based on the selected artifact configuration. This executable can be transferred to any Windows endpoint and executed locally to collect forensic evidence without requiring an active Velociraptor client installation.
---

## 4. Execute Collector

<img width="481" height="239" alt="running" src="https://github.com/user-attachments/assets/cc719cf8-3df3-41b1-8412-ac11cb0531e0" />
The Offline Collector was executed with administrative privileges on the target Windows system. During execution, the tool automatically collected the configured forensic artifacts, including system information, running processes, network connections, installed services, and Windows Event Logs.

---

## 5. Generated Evidence ZIP

<img width="640" height="260" alt="executed" src="https://github.com/user-attachments/assets/177da4c8-373f-430f-92b5-458104730f67" />
After successfully collecting the requested artifacts, the Offline Collector packaged all acquired evidence into a compressed ZIP archive. This archive preserves the collected data for offline forensic examination and incident response investigations.
The Velociraptor server confirms successful completion of the collection task and provides information about the generated evidence package, including uploaded files, collection statistics, and execution status.
The generated ZIP archive contains the collected forensic artifacts in their original format. Investigators can extract and analyze these artifacts using Velociraptor or other forensic analysis tools to reconstruct system activity and support incident investigations.

---

# Evidence Generated

The Offline Collector generated:

- ZIP archive containing forensic artifacts
- Windows Event Logs
- Running Processes
- Network Connections
- Installed Services
- System Information

---

# Learning Outcomes

- Deployment of Velociraptor Server
- Offline Evidence Acquisition
- Windows Artifact Collection
- DFIR Workflow
- Endpoint Investigation

---

# References

- https://docs.velociraptor.app/
- https://docs.velociraptor.app/artifact_references/
