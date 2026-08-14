# ⚙️ Installation Guide – Velociraptor

---

# 📋 Requirements

- Windows 10 Virtual Machine
- Administrator Privileges
- VMware Workstation Pro
- Internet Connection

---

# Step 1 – Download Velociraptor

Visit:

https://docs.velociraptor.app/downloads/

Download the latest Windows executable.

<img width="680" height="113" alt="Screenshot 2026-08-03 132614" src="https://github.com/user-attachments/assets/a0365cc8-4ae6-4a98-ae21-ef5e9c37f4d4" />


---

# Step 2 – Create a Working Folder

Create a folder named:

```
Velociraptor
```

Move the downloaded executable into this folder.



---

# Step 3 – Open Command Prompt

Press:

```
Windows + R
```

Type:

```
cmd
```

Navigate to the folder:

```cmd
cd C:\Users\<username>\Downloads\Velociraptor
```



---

# Step 4 – Generate Configuration

Run:

```cmd
velociraptor.exe config generate -i
```

Answer the setup prompts.



---

# Step 5 – Start Server

Run:

```cmd
velociraptor.exe gui
```



---

# Step 6 – Open Dashboard

Visit:

```
https://127.0.0.1:8889
```

Ignore the browser certificate warning and log in using the generated credentials.

<img width="788" height="359" alt="Screenshot 2026-08-03 132927" src="https://github.com/user-attachments/assets/b17adf71-1a01-46d0-9012-3ec3c697daf6" />


---

# ✅ Installation Complete

Velociraptor Server is now ready.
