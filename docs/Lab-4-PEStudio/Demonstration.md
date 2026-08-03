# 📋 Demonstration Guide – Static Malware Analysis Using PEStudio

This guide demonstrates how to perform static analysis on a Windows Portable Executable (PE) file using PEStudio without executing the file.

---

# 🎯 Objective

The objective of this demonstration is to safely inspect a suspicious executable, identify potential Indicators of Compromise (IOCs), and understand its characteristics using static analysis techniques.

---

# Step 1 – Launch PEStudio

## Instructions

1. Open the folder where PEStudio was extracted.
2. Double-click **PEStudio.exe**.
<img width="586" height="286" alt="image" src="https://github.com/user-attachments/assets/6c48004d-d0ef-43df-ab9f-3c687cd045db" />



### Explanation

PEStudio is a portable application and does not require installation. Launching the executable opens the analysis dashboard.

### Expected Result

The PEStudio dashboard should open successfully.

---

# Step 2 – Load the Suspicious File

## Instructions

1. Click **File** or drag and drop the suspicious executable into PEStudio.
2. Select the file for analysis.

<img width="584" height="285" alt="image" src="https://github.com/user-attachments/assets/60fb3681-7893-496c-989f-8f5ec2d13c9f" />


### Explanation

PEStudio reads the executable without running it, making the analysis safe.

### Expected Result

The selected file is loaded and analyzed.

---

# Step 3 – Review File Information

## Instructions

Navigate to the **Information** section.

Observe details such as:

- File Name
- File Size
- Compile Time
- Architecture (32-bit / 64-bit)
- Hash Values

<img width="789" height="400" alt="image" src="https://github.com/user-attachments/assets/9a7c0da9-36d4-4d21-8d24-97e1d31113c4" />


### Explanation

This section provides basic metadata about the executable and helps identify suspicious timestamps or unusual file properties.

### Expected Result

General information about the executable is displayed.

---

# Step 4 – Analyze Imported Libraries

## Instructions

Open the **Imports** section.

Review the imported DLLs and Windows API functions.

<img width="790" height="401" alt="image" src="https://github.com/user-attachments/assets/58d93586-5197-4dd4-b9f3-95ba27b74879" />


### Explanation

Imported APIs indicate what capabilities the executable may have, such as network communication, file operations, registry access, or process manipulation.

### Expected Result

A list of imported DLLs and API functions is displayed.

---

# Step 5 – Examine Embedded Strings

## Instructions

Navigate to the **Strings** section.

Review readable strings present within the executable.

<img width="789" height="401" alt="image" src="https://github.com/user-attachments/assets/67389838-4630-4b76-acad-de4a890d2891" />


### Explanation

Embedded strings may reveal URLs, IP addresses, file paths, registry keys, commands, or other useful forensic artifacts.

### Expected Result

Readable strings extracted from the executable are displayed.

---

# Step 6 – Review Indicators

## Instructions

Select the **Indicators** section.

Review any highlighted warnings or suspicious findings.

<img width="790" height="400" alt="image" src="https://github.com/user-attachments/assets/21d03304-c3d7-409a-9c47-df2da3f43d22" />


### Explanation

PEStudio automatically evaluates the executable and highlights potentially suspicious characteristics that may require further investigation.

### Expected Result

The Indicators section displays any detected warnings.

---

# Step 7 – Review VirusTotal Information (Optional)

## Instructions

If available, open the **VirusTotal** section.

Review the detection results.

<img width="788" height="398" alt="image" src="https://github.com/user-attachments/assets/f40c7b13-78ee-446a-ae02-647594157dca" />


### Explanation

PEStudio can display VirusTotal reputation data if the file has previously been analyzed.

### Expected Result

VirusTotal detection information is displayed (if available).

---

# 📝 Summary

In this demonstration, you successfully:

- Loaded a PE file into PEStudio
- Examined executable metadata
- Reviewed imported DLLs and APIs
- Analyzed embedded strings
- Identified suspicious indicators
- Performed safe static malware analysis

---

# 🎓 Learning Outcome

After completing this demonstration, participants should be able to:

- Perform static malware analysis
- Interpret PE file metadata
- Identify suspicious imports and strings
- Recognize Indicators of Compromise (IOCs)
- Safely inspect suspicious executables without execution
