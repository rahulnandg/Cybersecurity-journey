# 🧠 DNS in Detail – TryHackMe Walkthrough & Concepts

Welcome to my documentation of the **DNS in Detail** room from [TryHackMe](https://tryhackme.com). This room is part of the Pre-Security Path and focuses on mastering the fundamentals of **Domain Name System (DNS)** — a critical skill for cybersecurity and networking.

---

## 🧩 What I Learned

### 📌 1. What is DNS?
- DNS (Domain Name System) is the **"phonebook of the internet"**.
- It translates **domain names** (like `example.com`) into **IP addresses** that computers use to locate each other.

### 📌 2. Domain Hierarchy
- Structure of domain names:
- Hierarchy:
- Root (`.`)
- TLD (.com, .net, .org)
- Second-level (example)
- Subdomains (www, blog, mail, etc.)

### 📌 3. DNS Record Types
| Record Type | Purpose |
|-------------|---------|
| **A**       | Maps a domain to an IPv4 address |
| **AAAA**    | Maps a domain to an IPv6 address |
| **CNAME**   | Canonical name (alias for another domain) |
| **MX**      | Mail exchange (email routing) |
| **NS**      | Name server for a domain |
| **TXT**     | Arbitrary text; often used for verification and SPF |


### 📌 4. How DNS Requests Work
1. User types a domain into the browser.
2. Request goes to **recursive resolver**.
3. Resolver queries **root server**, **TLD server**, and **authoritative server** in sequence.
4. Once IP is found, it's returned to the browser.
5. The browser contacts the web server using the IP and loads the site.

---

## 🛠️ Skills Gained
- Deep understanding of DNS lookup flow
- Analyzing and identifying DNS record types
- Networking fundamentals from a cybersecurity perspective

---

## 🚀 Why This Matters in Cybersecurity

- Attackers often use **DNS tunneling**, **phishing domains**, and **subdomain takeovers**.
- Misconfigured DNS can lead to **data leaks**, **downtime**, or **email spoofing**.
- Understanding DNS is critical in **reconnaissance**, **threat hunting**, and **incident response**.

---


---

## 🔗 TryHackMe Room
🔗 [DNS in Detail – TryHackMe](https://tryhackme.com/room/dnsindetail)

---

## 📫 Connect With Me

🔒 I’m actively learning and documenting my cybersecurity journey.  
If you're looking for someone passionate about security, learning, and teaching — let’s connect.

- 🔗 [LinkedIn](https://www.linkedin.com/in/rahul-nandagopal/)
- 🛠️ 

---



