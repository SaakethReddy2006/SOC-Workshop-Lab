# 🛡️ SOC Workshop Lab

![Windows](https://img.shields.io/badge/OS-Windows%2010-blue)
![SOC](https://img.shields.io/badge/Domain-SOC-green)
![DFIR](https://img.shields.io/badge/DFIR-Enabled-brightgreen)
![Malware Analysis](https://img.shields.io/badge/Malware-Analysis-red)
![License](https://img.shields.io/badge/License-MIT-yellow)

A hands-on **Security Operations Center (SOC)** laboratory built for learning and demonstrating Digital Forensics, Incident Response (DFIR), Malware Analysis, Endpoint Investigation, and Windows Security using industry-standard tools.

---

# 📌 Project Overview

This repository documents the setup of a complete SOC laboratory environment used to perform endpoint investigations, collect forensic evidence, analyze malware, inspect Windows artifacts, and understand incident response workflows.

The lab combines multiple open-source security tools to simulate real-world SOC analyst activities and build practical cybersecurity skills.

---

# 🎯 Objectives

- Build a practical Security Operations Center (SOC) lab
- Learn Digital Forensics and Incident Response (DFIR)
- Perform Windows endpoint investigations
- Analyze malware using static analysis tools
- Collect forensic evidence using Velociraptor
- Investigate Windows processes, services, event logs, and network activity
- Document investigation workflows
- Develop practical SOC analyst skills

---

# 🛠 Technologies Used

- Windows 10
- VMware Workstation Pro
- Velociraptor
- PEStudio
- VirusTotal
- System Informer
- DVWA
- Git
- GitHub
- Markdown

---

# 🏗 Lab Architecture

```text
                 VMware Workstation
                        │
        ┌───────────────┴───────────────┐
        │                               │
   Windows 10 VM                 Kali Linux VM
        │
        │
 ┌──────┴───────────────────────────────────┐
 │                                          │
 │  Velociraptor                            │
 │  PEStudio                                │
 │  VirusTotal                              │
 │  System Informer                         │
 │  DVWA                                    │
 └──────────────────────────────────────────┘
```

---

# 📂 Repository Structure

```text
SOC-Workshop-Lab/
│
├── README.md
├── LICENSE
│
├── screenshots/
│
├── docs/
│
├── DFIR/
│
├── Malware-Analysis/
│
├── Endpoint-Analysis/
│
├── Web-Security/
│
└── Resources/
```

---

# 🔬 DFIR

The DFIR section focuses on collecting and analyzing Windows forensic artifacts.

Topics include:

- Velociraptor Offline Collector
- Windows Event Logs
- Windows Services
- Process Tree Analysis
- Network Connections
- Endpoint Investigation

---

# 🦠 Malware Analysis

This section demonstrates static malware analysis using:

- PEStudio
- VirusTotal
- Windows executable inspection
- PE header analysis
- Indicators of Compromise (IOCs)

---

# 💻 Endpoint Analysis

Endpoint investigation using:

- System Informer
- Running Processes
- Services
- Threads
- Handles
- Resource Usage

---

# 🌐 Web Security

Practical web application security testing using:

- Damn Vulnerable Web Application (DVWA)
- Vulnerability discovery
- Web attack concepts

---

# 🚀 Workflow

```text
SOC Lab Setup
        │
        ▼
Deploy Windows Environment
        │
        ▼
Install Security Tools
        │
        ▼
Collect Windows Artifacts
        │
        ▼
Analyze Malware
        │
        ▼
Investigate Endpoint
        │
        ▼
Generate Findings
```

---

# 📸 Screenshots

## Velociraptor Dashboard

<img width="788" height="356" alt="dashboard" src="https://github.com/user-attachments/assets/cd5d68ee-52be-48fc-9942-afb23105793a" />

---

## Offline Collector Configuration

<img width="704" height="327" alt="configuration" src="https://github.com/user-attachments/assets/bdaeaea9-0ee2-4cf6-9216-30d29da54726" />


---

## Collector Execution

<img width="481" height="239" alt="running" src="https://github.com/user-attachments/assets/7dbdf194-5b16-4d33-8077-d9ec61d286cc" />

---

## Collection Results

<img width="640" height="260" alt="executed" src="https://github.com/user-attachments/assets/865356e1-6943-40e8-81b1-66f0686656e1" />


---

## PEStudio Analysis

![PEStudio](screenshots/pestudio.png)

---

## VirusTotal Scan

![VirusTotal](screenshots/virustotal.png)

---

## System Informer

![System Informer](screenshots/system-informer.png)

---

## DVWA

![DVWA](screenshots/dvwa.png)

---

# 📊 Skills Demonstrated

- Security Operations Center (SOC)
- Digital Forensics & Incident Response (DFIR)
- Endpoint Investigation
- Windows Artifact Collection
- Malware Analysis
- Static Analysis
- Evidence Collection
- Process Investigation
- Service Analysis
- Windows Event Log Analysis
- Network Connection Analysis
- Documentation & Reporting

---

# 🎓 Learning Outcomes

Through this project I learned:

- Building a complete SOC lab
- Endpoint forensic evidence collection
- Windows investigation techniques
- Malware static analysis
- Windows artifact analysis
- Security investigation workflow
- Practical DFIR methodologies
- Documentation of security investigations

---

# 🚧 Future Improvements

Planned additions to this repository:

- Wazuh SIEM
- Sysmon
- Sigma Rules
- YARA
- Splunk
- ELK Stack
- Microsoft Sentinel
- Zeek
- Suricata
- TheHive
- Cortex

---

# 📚 References

- Velociraptor Documentation  
  https://docs.velociraptor.app/

- Microsoft Learn  
  https://learn.microsoft.com/

- VirusTotal  
  https://www.virustotal.com/

- MITRE ATT&CK  
  https://attack.mitre.org/

- PEStudio  
  https://www.winitor.com/

---

# ⚠ Disclaimer

This repository was created for **educational and research purposes only**.

All tools were used inside an isolated laboratory environment.

---

# 📄 License

This project is licensed under the **MIT License**.

---

⭐ If you found this repository useful, consider giving it a star.
