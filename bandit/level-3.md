🕵️‍♂️ OverTheWire Bandit – Level 3 Walkthrough
Goal:
Find the password for the next level, hidden somewhere inside a folder.

✅ Level Summary
Current Level: Bandit Level 3

Next Level: Bandit Level 4

Challenge: A hidden file inside a hidden directory contains the password. We need to find and read it.

🛠️ Commands Used
Command	Purpose
"ls -a"	List all files, including hidden ones (those starting with a dot .)
"cd"	Change directory (move into a folder)
"cat"	Display the contents of a file

🧭 Step-by-Step Solution
🔹 Step 1: List everything in the current directory
"ls -a"
The "-a" option shows all files — even hidden ones. This revealed a hidden directory called:

".inhere"
🔹 Step 2: Go inside the .inhere directory
"cd inhere"
Now we are inside the hidden folder where the password might be stored.

🔹 Step 3: List contents of .inhere
"ls -a"
Again, ls -a helps us discover all files, even hidden ones inside this hidden folder.
I found an interesting file named:
...Hiding-From-You
Yes, the file name starts with three dots, which makes it a bit tricky to spot or work with.

🔹 Step 4: Read the content of the file
cat ...Hiding-From-You
The cat command displays the content of the file.
💡 This file contained the password for the next level.

🎯 Key Takeaways
Always use ls -a when exploring — hidden files can contain crucial data.

File and folder names can start with multiple dots — don’t ignore them!

Knowing how to navigate and inspect the file system is a core Linux skill.

🧑‍💻 Why This Matters
This challenge tested my ability to:

Work in the Linux command-line environment

Think critically and pay attention to hidden details

Document steps clearly for repeatability

I’m committed to learning in public, and cybersecurity challenges like this help sharpen both my technical and analytical thinking.

📌 About the Bandit Wargame
OverTheWire Bandit is a popular set of hands-on CTF challenges designed to teach Linux and cybersecurity fundamentals.

🔗 Let’s Connect
If you’re a recruiter or hiring manager looking for someone who’s consistent, coachable, and passionate about learning cybersecurity — I’d love to connect on LinkedIn.
