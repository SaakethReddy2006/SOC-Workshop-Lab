# 🛡️ SOC Workshop Lab

![Windows](https://img.shields.io/badge/OS-Windows%2010-blue)
![SOC](https://img.shields.io/badge/Domain-Security%20Operations%20Center-success)
![DFIR](https://img.shields.io/badge/DFIR-Digital%20Forensics-red)
![Cybersecurity](https://img.shields.io/badge/Cybersecurity-Workshop-orange)
![License](https://img.shields.io/badge/License-MIT-green)

---

# 📌 Project Overview

This repository serves as the official documentation for the **Security Operations Center (SOC) Workshop**. It provides setup guides, lab manuals, and demonstrations for each hands-on exercise conducted during the workshop.

The objective of this repository is to help participants recreate the laboratory environment, understand the tools used during the workshop, and revisit each practical exercise independently.

---

> 💡 **Workshop Guide**
>
> Every lab contains:
>
> - 📖 Overview
> - ⚙️ Installation
> - 🔧 Configuration
> - 🎥 Demonstration
> - 🎓 Learning Outcomes
>
> Click on any lab below to open its complete guide.

---

# 🎯 Workshop Objectives

By completing this workshop, participants will learn how to:

- Build a practical Security Operations Center (SOC) lab
- Investigate web application security incidents
- Perform Digital Forensics & Incident Response (DFIR)
- Analyze Windows memory for suspicious activities
- Perform static malware analysis
- Analyze suspicious files using online threat intelligence
- Perform dynamic malware analysis
- Understand Windows internals and forensic artifacts

---

# 📚 Workshop Labs

| Lab | Laboratory Exercise | Documentation |
|------|---------------------|---------------|
| **Lab 1** | Forensic Investigation of Application Security Incidents: SQL Injection Attack | 📖 [Open Guide](docs/Lab-1-SQL-Injection) |
| **Lab 2** | Forensic Investigation of a Compromised System Incident Using Velociraptor | 📖 [Open Guide](docs/Lab-2-Velociraptor) |
| **Lab 3** | Analyzing RAM for Suspicious Activities Using Redline | 📖 [Open Guide](docs/Lab-3-Redline) |
| **Lab 4** | Perform Static Analysis on a Suspicious File Using PEStudio | 📖 [Open Guide](docs/Lab-4-PEStudio) |
| **Lab 5** | Examine a Suspicious File Using VirusTotal | 📖 [Open Guide](docs/Lab-5-VirusTotal) |
| **Lab 6** | Perform Dynamic Malware Analysis in Windows using Process Hacker | 📖 [Open Guide](docs/Lab-6-Process-Hacker) |

---

# 💻 Lab Environment

| Component | Details |
|-----------|---------|
| Host Operating System | Windows 10 |
| Virtualization Platform | VMware Workstation Pro |
| Virtual Machines | Windows 10, Kali Linux |
| Version Control | Git & GitHub |

---

# 🛠️ Tools Used

- Velociraptor
- Redline
- PEStudio
- VirusTotal
- Process Hacker
- DVWA
- VMware Workstation Pro
- Git
- GitHub

---

# 🏗️ Lab Architecture

```text
                     VMware Workstation
                             │
           ┌─────────────────┴─────────────────┐
           │                                   │
      Windows 10 VM                     Kali Linux VM
           │
           │
    ┌──────┴────────────────────────────────────────┐
    │                                               │
    │  DVWA                                          │
    │  Velociraptor                                 │
    │  Redline                                      │
    │  PEStudio                                     │
    │  VirusTotal                                   │
    │  Process Hacker                               │
    └───────────────────────────────────────────────┘
```

---

# 🏆 Skills Gained

Participants will gain practical experience in:

- Security Operations Center (SOC)
- Digital Forensics & Incident Response (DFIR)
- Web Application Security
- Memory Forensics
- Static Malware Analysis
- Dynamic Malware Analysis
- Windows Internals
- Windows Artifact Collection
- Threat Intelligence
- Security Investigation Workflow
- Documentation & Reporting

---

# 📂 Repository Structure

```text
SOC-Workshop-Lab/
│
├── README.md
├── LICENSE
│
├── Labs/
│   ├── Lab-1-SQL-Injection.md
│   ├── Lab-2-Velociraptor.md
│   ├── Lab-3-Redline.md
│   ├── Lab-4-PEStudio.md
│   ├── Lab-5-VirusTotal.md
│   └── Lab-6-ProcessHacker.md
│
└── screenshots/
```

---

# 🚀 Future Enhancements

Future additions planned for this workshop include:

- Wazuh SIEM
- Sysmon
- Sigma Rules
- YARA
- Splunk
- ELK Stack
- Microsoft Sentinel
- Zeek
- Suricata

---

# 📚 References

- Velociraptor Documentation — https://docs.velociraptor.app/
- Microsoft Learn — https://learn.microsoft.com/
- VirusTotal — https://www.virustotal.com/
- MITRE ATT&CK Framework — https://attack.mitre.org/
- PEStudio — https://www.winitor.com/

---

# ⚠️ Disclaimer

This repository is intended **solely for educational and research purposes**.

All demonstrations were performed in isolated virtual laboratory environments. Do not use these techniques on systems without proper authorization.

---

# 📄 License

This project is licensed under the **MIT License**.
