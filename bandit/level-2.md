 OverTheWire: Bandit - Level 2 Walkthrough
 Goal:
The password for the next level is stored in a file called --spaces in this filename--.

 Step-by-Step Solution
 1. SSH into the Bandit server
ssh bandit2@bandit.labs.overthewire.org -p 2220
ssh: Securely connects you to a remote server.

bandit2@...: You're logging in as user bandit2.

-p 2220: The Bandit game uses port 2220 instead of the default SSH port (22).

 You'll be asked for the password you got from Level 1.

 2. List all files in the current directory
"ls -a"
ls: Lists files and directories.

-a: Shows all files, including hidden ones (starting with a dot .).

You should see a file named: --spaces in this filename--
This filename includes spaces and starts with double dashes, which makes it tricky to handle.

 **Why cat --spaces in this filename-- doesn't work**
This will NOT work: cat --spaces in this filename--
Because: The --spaces part is interpreted as a command-line option (not a filename).

The spaces break the input into multiple arguments, which is not what we want.

3. Proper way to read the file
cat ./"--spaces in this filename--"
cat: Displays file contents.

./: Refers to the current directory.

Wrapping the filename in quotes ensures it’s treated as a single string, even with spaces and dashes.

This command will print the password for Level 3 

 Final Thoughts
This level teaches an important lesson:

Filenames with special characters (like spaces or --) need to be handled with care in the shell.

**Commands Used Recap**
Command	Description
ssh user@host -p port	Connects to a remote server via SSH
ls -a	Lists all files, including hidden ones
cat ./"filename with spaces"	Reads a file with a tricky name

 What I Learned
How to SSH into a server on a custom port

How to list hidden files with ls -a

How to handle filenames with spaces and special characters using quotes

That -- at the start of a filename can act like a command-line flag and break your command

This solution is part of my ongoing journey through OverTheWire: Bandit.
Follow me on GitHub and LinkedIn to see how I solve each level and explain it step-by-step for beginners!
