# 🛡️ OverTheWire Bandit — Level 1 Walkthrough

## 🎯 Objective

SSH into the remote machine as `bandit1` and retrieve the password for `bandit2`. The password is stored in a file named `-` located in the home directory.

---

## 🖥️ Level Details

- **Username:** `bandit1`
- **Host:** `bandit.labs.overthewire.org`
- **Port:** `2220`
- **Password from Level 0:** `boJ9jbbUNNfktd78OOpsqOltutMc3MY1`

---

## 🛠️ Step-by-Step Solution

### 🔹 Step 1: SSH into the server

```bash
ssh bandit1@bandit.labs.overthewire.org -p 2220
🔍 This command connects to the remote server using SSH on port 2220 as user bandit1.

🔹 Step 2: List all files in the home directory
ls
🔍 Lists all files in the current directory. You’ll see a file named:
(-)
The dash (-) is tricky because it's usually used as an option flag in Linux commands.

🔹 Step 3: View the contents of the file named -
cat ./-
🔍 ./ tells the system to look for the file named - in the current directory, avoiding the confusion with command flags.

📥 This reveals the password for the next level.

🔑 Password for Level 2
CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9

✅ What I Learned

How to SSH into a remote server using a custom port.

How to handle tricky filenames like (-) in Linux.

How to read file contents using cat.

The importance of relative paths (./) to avoid command conflicts.

🧠 Why It Matters
This level builds practical knowledge of:

Linux command-line fundamentals

Remote connections

Navigating and managing files in tricky scenarios

🚀 About OverTheWire Bandit
OverTheWire: Bandit is a free wargame that helps users learn Linux commands and security basics through hands-on levels.
