# 📋 Demonstration Guide – Velociraptor Offline Evidence Collection

This guide demonstrates how to generate an Offline Collector, collect forensic artifacts from a Windows endpoint, and preserve the collected evidence for later investigation.

---

# 🎯 Objective

The objective of this demonstration is to perform offline forensic evidence collection using Velociraptor without installing a permanent endpoint agent.

---

# Step 1 – Launch the Velociraptor Server

## Instructions

1. Open Command Prompt.
2. Navigate to the Velociraptor folder.
3. Start the server by running:

```cmd
velociraptor.exe gui
```

4. Wait until the server starts successfully.



### Explanation

This command starts the Velociraptor Server and launches the web interface used for forensic investigations.

### Expected Result

The server starts successfully without errors.

---

# Step 2 – Open the Velociraptor Dashboard

## Instructions

1. Open your preferred web browser.
2. Visit:

```
https://127.0.0.1:8889
```

3. Log in using your administrator credentials.

<img width="788" height="356" alt="dashboard" src="https://github.com/user-attachments/assets/4cbf3057-cdee-4a2c-8d66-883038484070" />


### Explanation

The dashboard is the central interface for creating collectors, managing endpoints, and analyzing collected forensic artifacts.

### Expected Result

The Velociraptor Dashboard should load successfully.

---

# Step 3 – Create a New Offline Collector

## Instructions

1. Navigate to **Collector**.
2. Click the **+** button.
3. Search for:

```
Server.Utils.CreateCollector
```

4. Select the artifact.

<img width="713" height="327" alt="image" src="https://github.com/user-attachments/assets/bb002707-18de-494a-b5b6-e537d6ae3df6" />


### Explanation

The Offline Collector generates a standalone executable that can acquire forensic evidence from Windows systems.

### Expected Result

The Collector Configuration window opens.

---

# Step 4 – Configure Artifact Collection

## Instructions

Select the following configuration.

Operating System:

```
Windows
```

Artifacts:

- Generic.Client.Info
- Generic.System.Pstree
- Windows.Network.Netstat
- Windows.System.Services
- Windows.EventLogs.Evtx

Leave the remaining options at their default values.

<img width="704" height="327" alt="configuration" src="https://github.com/user-attachments/assets/88088c14-0bc5-4546-808b-f9b3f36db6d8" />

### Explanation

These artifacts collect important forensic information including:

- System information
- Running processes
- Active network connections
- Installed Windows services
- Windows Event Logs

### Expected Result

The collector is configured successfully.

---

# Step 5 – Generate the Offline Collector

## Instructions

1. Click **Launch** in the Offline Collector configuration.
2. Wait for Velociraptor to build the collector.
3. Confirm that `Server.Utils.CreateCollector` shows **State: Completed**.
4. Open the **Uploaded Files** tab.
5. Locate the generated **collector `.exe`** file.
6. Select the `.exe` and click **Download**.
7. Save the downloaded executable to your desired location.

> **Note:** The generated `.exe` under **Uploaded Files** is the Offline Collector. Do not confuse it with the `velociraptor.exe` used to run the Velociraptor server.

### Explanation

Velociraptor packages the selected artifacts into a standalone Windows executable.

### Expected Result

The collector executable is generated successfully.

---

# Step 6 – Execute the Collector

## Instructions

1. Copy the generated collector to the target Windows machine.
2. Right-click the executable.
3. Select:

```
Run as Administrator
```

4. Wait for the collection process to complete.

<img width="481" height="239" alt="running" src="https://github.com/user-attachments/assets/669b951f-d478-4b54-ac95-4639658927b9" />


### Explanation

The collector gathers all selected forensic artifacts and packages them into a compressed archive.

### Expected Result

The collection completes successfully.

---

# Step 7 – Review the Collected Evidence

## Instructions

After execution completes, locate the generated ZIP archive.

Example:

```
Collection-DESKTOP-XXXX.zip
```

<img width="640" height="260" alt="executed" src="https://github.com/user-attachments/assets/3c9d3cd7-b902-4f37-9dce-77241c1fde94" />


### Explanation

The ZIP archive contains the forensic artifacts collected from the endpoint and can be preserved for later analysis.

### Expected Result

A forensic evidence archive is successfully created.

---

# 📝 Summary

In this demonstration, you successfully:

- Started the Velociraptor Server
- Accessed the Web Dashboard
- Created an Offline Collector
- Configured artifact collection
- Executed the collector
- Collected forensic evidence
- Generated a forensic evidence ZIP archive

The collected evidence can now be analyzed using Velociraptor or other DFIR tools.

---

# 🎓 Learning Outcome

After completing this demonstration, participants should be able to:

- Generate Offline Collectors
- Perform endpoint forensic evidence collection
- Configure artifact selection
- Preserve digital evidence
- Understand the offline DFIR workflow
