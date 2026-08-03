# 📋 Demonstration Guide – Dynamic Process Analysis Using Process Hacker

This guide demonstrates how to monitor the runtime behavior of a Windows executable using Process Hacker. Participants will launch a legitimate application (PuTTY) and observe its processes, threads, handles, and resource usage.

---

# 🎯 Objective

The objective of this demonstration is to understand how Process Hacker can be used to inspect running processes, analyze process information, and monitor system activity in real time.

> **Note:** This lab uses **PuTTY (`putty.exe`)**, a legitimate and digitally signed SSH client, for educational purposes. The techniques demonstrated in this lab are commonly used during malware investigations and incident response.

---

# Step 1 – Launch Process Hacker

## Instructions

1. Open the **Start Menu**.
2. Search for **Process Hacker**.
3. Right-click **Process Hacker**.
4. Select **Run as administrator**.

<img width="551" height="403" alt="image" src="https://github.com/user-attachments/assets/a808eb84-c7e2-4524-a600-95c725c59ea7" />


### Explanation

Launching Process Hacker with administrative privileges allows access to detailed information about running processes and system resources.

### Expected Result

The Process Hacker dashboard opens successfully and displays the list of active processes.

---

# Step 2 – Execute PuTTY

## Instructions

1. Navigate to the location of **putty.exe**.
2. Double-click the executable.
3. Keep the PuTTY window open.

<img width="304" height="251" alt="image" src="https://github.com/user-attachments/assets/5df2681e-8a60-414d-ba32-1094a95dd757" />


### Explanation

PuTTY is executed to generate a live process that can be monitored using Process Hacker.

### Expected Result

The PuTTY application launches successfully.

---

# Step 3 – Locate the PuTTY Process

## Instructions

1. Return to **Process Hacker**.
2. Locate **putty.exe** in the process list.
3. Observe its **Process ID (PID)** and parent process.

<img width="388" height="50" alt="image" src="https://github.com/user-attachments/assets/5c82e1e8-a593-47e2-bb4a-3aa318f8d721" />

### Explanation

Each running application appears as a separate process with a unique Process ID (PID). The parent process indicates which application started it.

### Expected Result

The running PuTTY process is visible in the process list.

---

# Step 4 – View Process Properties

## Instructions

1. Right-click **putty.exe**.
2. Select **Properties**.

Review:

- Executable Path
- Command Line
- Integrity Level
- Digital Signature

<img width="557" height="400" alt="image" src="https://github.com/user-attachments/assets/a67569a4-a0f0-4113-9ae3-da56fe6823d5" />

### Explanation

The Properties window provides detailed information about the executable and confirms that it is a legitimate digitally signed application.

### Expected Result

The process properties are displayed successfully.

---

# Step 5 – Analyze Threads

## Instructions

1. Open the **Threads** tab.
2. Review the active threads associated with the process.

<img width="498" height="398" alt="image" src="https://github.com/user-attachments/assets/e67b6c88-6f39-4344-8981-572710fa8590" />


### Explanation

Threads are the smallest units of execution within a process. Monitoring threads helps analysts understand how an application performs its tasks.

### Expected Result

The Threads tab displays all active threads for PuTTY.

---

# Step 6 – Analyze Handles

## Instructions

1. Open the **Handles** tab.
2. Review the handles opened by the process.

<img width="788" height="399" alt="image" src="https://github.com/user-attachments/assets/9913e410-f4a7-430f-95f3-dbbcd9e84a00" />

### Explanation

Handles represent resources currently being used by the application, such as files, registry keys, events, mutexes, and other system objects.

### Expected Result

The Handles tab displays the resources accessed by PuTTY.

---

# Step 7 – Monitor Resource Usage

## Instructions

Observe the following process statistics:

- CPU Usage
- Memory Usage
- Private Bytes
- Working Set

<img width="790" height="399" alt="image" src="https://github.com/user-attachments/assets/31bcb575-799d-4f8a-9ae4-0b934e9d98f3" />


### Explanation

Monitoring resource usage helps analysts identify abnormal behavior such as excessive memory consumption or unusually high CPU utilization.

### Expected Result

Current resource utilization for PuTTY is displayed.

---

# Step 8 – Terminate the Process

## Instructions

1. Right-click **putty.exe**.
2. Select **Terminate**.
3. Confirm the action if prompted.

<img width="789" height="399" alt="image" src="https://github.com/user-attachments/assets/96019f63-ab24-4dd4-a6ac-f20288df6a61" />

### Explanation

Terminating the process immediately stops its execution. This action is commonly performed during malware containment or when ending an unresponsive application.

### Expected Result

The PuTTY process disappears from the process list.

---

# 📝 Summary

In this demonstration, you successfully:

- Launched Process Hacker
- Executed PuTTY
- Identified the running process
- Examined process properties
- Reviewed threads and handles
- Monitored resource usage
- Terminated the process

---

# 🎓 Learning Outcome

After completing this demonstration, participants should be able to:

- Monitor running Windows processes
- Interpret Process IDs (PIDs)
- Analyze process properties
- Understand threads and handles
- Monitor CPU and memory usage
- Safely terminate running processes during an investigation
