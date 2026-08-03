# ⚙️ Installation Guide – SQL Injection Lab

This guide explains how to set up the environment required for performing a SQL Injection demonstration.

---

# 📋 Requirements

- Windows 10/11
- VMware Workstation Pro or VirtualBox
- XAMPP
- DVWA (Damn Vulnerable Web Application)
- Web Browser (Google Chrome or Microsoft Edge)

---

# Step 1 – Download XAMPP

1. Open your web browser.
2. Visit the official website:

https://www.apachefriends.org/

3. Download the latest version of XAMPP for Windows.

<img width="812" height="392" alt="Screenshot 2026-08-03 131419" src="https://github.com/user-attachments/assets/7396fe1b-f5e9-450a-a136-a5e6aeb47ad2" />


**Explanation**

XAMPP installs Apache, PHP, and MySQL, which are required to host DVWA locally.

---

# Step 2 – Install XAMPP

1. Run the downloaded installer.
2. Click **Next** through the installation wizard.
3. Keep the default components selected.
4. Finish the installation.

---

# Step 3 – Start Apache and MySQL

1. Open **XAMPP Control Panel**.
2. Click **Start** for:
   - Apache
   - MySQL

The status indicators should turn green.

<img width="449" height="261" alt="Screenshot 2026-08-03 131744" src="https://github.com/user-attachments/assets/11cf1b83-b274-465c-be8d-14b8bfb55b2f" />


---

# Step 4 – Download DVWA

1. Visit:

https://github.com/digininja/DVWA

2. Download the ZIP file.
3. Extract it.

---

# Step 5 – Move DVWA

Copy the extracted folder into:

```
C:\xampp\htdocs\

```

Rename it to:

```
dvwa

```

# Step 6 – Configure DVWA

Open:

```
config/config.inc.php
```

Rename:

```
config.inc.php.dist
```

to

```
config.inc.php

---

# Step 7 – Open DVWA

Open your browser.

Visit:

```
http://localhost/dvwa
```

Follow the setup instructions and create the database.

<img width="788" height="398" alt="Screenshot 2026-08-03 131935" src="https://github.com/user-attachments/assets/1fc4b9dc-2633-4ebc-9fa5-c5448f13d04e" />


---

# ✅ Installation Complete

DVWA is now ready for the SQL Injection lab.
