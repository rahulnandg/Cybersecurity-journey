# 🔍 TryHackMe - Investigating Windows (CTF Writeup)

This is my personal writeup for the **"Investigating Windows"** room on TryHackMe. It focuses on practical Windows forensics using PowerShell, covering log analysis, user behavior, and network connections.

All answers below were found using native Windows tools — mainly **PowerShell** and **Event Viewer**.

---

## ✅ Question 1: What’s the version and year of the Windows machine?

**🔍 Objective:** Identify the OS version and its release year.

**🛠️ Method:**
I used `Get-ComputerInfo to fetch the Windows version.

**📄 PowerShell Command:**
Get-ComputerInfo

📌 Answer:
Windows datacenter 2016

✅ Question 2: Which user logged in last?
🔍 Objective: Find the last successfully logged-in user.



🛠️ Method:
Queried the Security Event Log for Event ID 4624 (successful logon) and reviewed the user account in the message.

📄 PowerShell Command: Get-LocalUser

 Answer: Administrator

✅ Question 3: When did John log onto the system last?


🔍 Objective: Extract the timestamp of John’s latest login.

🛠️ Method:
Filtered Event ID 4624 logs for John and pulled the TimeCreated field.

Powershell Command: net user john |findstr "Last"

Answer:03/02/2019 5:48:32 pm

✅ Question 4: What IP does the system connect to when it first starts?
🔍 Objective: Identify the first outbound connection IP after system startup.

🛠️ Method:
regedit > HKEY_LOCAL_MACHINE > software > Microsoft > Windows > RUN > updatesvc, the IP address was 10.34.2.3.

RUN is where all the files both malicious and legitimate ones automatically run when the windows is booted. We check for "updatesvc" because that is how malware hides itself as. 

✍️ Notes
All investigation was done inside a virtualized Windows environment provided by TryHackMe.

I documented this as part of my learning and public portfolio-building process.

PowerShell was used exclusively to simulate realistic analyst workflows.

🧠 Why This Matters
This challenge helped me build practical skills in:

Windows log analysis

Using PowerShell for investigation

Understanding login events and user activity






