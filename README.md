# Security Log Analyzer (Mini SOC Project)

A simple Python program that simulates **SOC (Security Operations Center) log analysis** by detecting suspicious failed login attempts in Linux-style authentication logs.  

This project is beginner-friendly, uses standard Python, and demonstrates real-world defensive security concepts.

---

## 🛠️ Features

- Reads a log file (`auth.log` or any log you provide)
- Detects **failed SSH login attempts**
- Extracts attacker **IP addresses**
- Counts repeated attempts using Python's `Counter`
- Prints a **ranked list of top suspicious IPs**
- Gracefully handles missing log files or empty logs

---

## 📂 Example Log File (`auth.log`)

```text
Dec 1 10:01:23 server sshd[1234]: Failed password for root from 45.33.12.90 port 44522 ssh2
Dec 1 10:01:30 server sshd[1234]: Failed password for root from 45.33.12.90 port 44522 ssh2
Dec 1 10:01:35 server sshd[1234]: Failed password for root from 192.168.1.10 port 33445 ssh2

How to Run
run python log_analyzer.py using python 3
If no failed attempts are found:
Top suspicious IPs:
No suspicious login attempts found.

if there is any suspicious login in:

Top suspicious IPs:
45.33.12.90: 2 attempts
192.168.1.10: 1 attempts
