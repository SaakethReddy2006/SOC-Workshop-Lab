# 📋 Demonstration Guide – Suspicious File Analysis Using VirusTotal

This guide demonstrates how to analyze a Windows executable using VirusTotal to determine its reputation, antivirus detections, and threat intelligence.

---

# 🎯 Objective

The objective of this demonstration is to analyze a Windows executable using VirusTotal and understand how cloud-based threat intelligence assists in malware detection and incident response.

> **Note:** This lab uses **PuTTY (`putty.exe`)**, a legitimate and digitally signed SSH client, for educational purposes. The goal is to learn how VirusTotal presents analysis results for Windows executables.

---

# Step 1 – Open VirusTotal

## Instructions

1. Open your preferred web browser.
2. Navigate to:

```
https://www.virustotal.com
```

3. Log in to your VirusTotal account.

<img width="959" height="439" alt="image" src="https://github.com/user-attachments/assets/7d7e9763-f86a-4ab7-a944-3ae32f289a6e" />



### Explanation

VirusTotal is a cloud-based malware analysis platform that scans files using multiple antivirus engines and threat intelligence sources.

### Expected Result

The VirusTotal dashboard opens successfully.

---

# Step 2 – Upload the Executable

## Instructions

1. Click **Upload File**.
2. Browse to the location of the **putty.exe**.
3. Select the file.
4. Wait for the upload to complete.

<img width="785" height="399" alt="image" src="https://github.com/user-attachments/assets/0796dfa9-88dc-489c-9def-424be96d4b3a" />



### Explanation

VirusTotal calculates the cryptographic hash of the executable and checks whether it has been previously analyzed. If a report already exists, it is displayed immediately.

### Expected Result

The analysis report begins loading.

---

# Step 3 – Review the Detection Summary

## Instructions

Observe the overall detection result displayed at the top of the report.

Review:

- Detection Ratio
- Community Score
- File Type
- SHA-256 Hash

<img width="790" height="353" alt="Screenshot 2026-08-03 162230" src="https://github.com/user-attachments/assets/b2ba9327-6e7e-4d28-84c4-5d7652310bc8" />



### Explanation

The detection summary provides a quick overview of how many security vendors flagged the file. Since PuTTY is a legitimate application, it is expected to have little or no antivirus detections.

### Expected Result

The report displays the file's detection summary and basic information.

---

# Step 4 – Review File Details

## Instructions

Open the **Details** tab.

Review:

- File Name
- File Size
- SHA-256
- MD5
- File Type
- Digital Signature
- Creation Time (if available)

<img width="789" height="356" alt="image" src="https://github.com/user-attachments/assets/63a2d5ed-4077-4eb3-9133-24294577435b" />


### Explanation

The Details section provides metadata that can be used to uniquely identify the file during forensic investigations.

### Expected Result

The file metadata is displayed successfully.

---

# Step 5 – Review Behavior (If Available)

## Instructions

Open the **Behavior** tab.

Review any available information regarding:

- Process Activity
- Registry Activity
- File Activity
- Network Activity

<img width="790" height="357" alt="image" src="https://github.com/user-attachments/assets/9a774eef-65a4-462d-9d97-5b9d847b5192" />


### Explanation

Behavioral analysis is only available if VirusTotal has executed the sample in a sandbox environment. Not every file will include this information.

### Expected Result

Behavioral information is displayed if available.

---

# Step 6 – Review Relations

## Instructions

Open the **Relations** tab.

Review any related files, contacted domains, IP addresses, or URLs.

<img width="790" height="359" alt="image" src="https://github.com/user-attachments/assets/0a5f44df-2130-47a7-b93c-fe31fb44a61e" />


### Explanation

Relations help analysts understand connections between the analyzed file and other artifacts within VirusTotal's threat intelligence database.

### Expected Result

Related artifacts are displayed (if available).

---

# Step 7 – Review Community Information

## Instructions

Open the **Community** tab.

Check whether security researchers have commented on or classified the file.

<img width="788" height="356" alt="image" src="https://github.com/user-attachments/assets/41a73d03-adfd-4252-9724-1ec6bb076bc8" />


### Explanation

Community contributions often provide additional context that may assist analysts during investigations.

### Expected Result

Community information is displayed if available.

---

# 📝 Summary

In this demonstration, you successfully:

- Uploaded a Windows executable
- Reviewed antivirus detections
- Examined file metadata
- Explored behavioral analysis
- Investigated related artifacts
- Learned how VirusTotal assists in threat intelligence

---

# 🎓 Learning Outcome

After completing this demonstration, participants should be able to:

- Upload suspicious files safely to VirusTotal
- Interpret detection results
- Analyze file metadata
- Understand cloud-based threat intelligence
- Perform reputation-based malware analysis
