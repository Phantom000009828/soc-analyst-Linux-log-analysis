# SOC Analyst L1 Project – Linux Log Analysis (SSH Brute Force Detection)

## 📌 Project Overview
This project focuses on analyzing Linux authentication logs to detect
suspicious SSH login attempts and identify potential brute-force attacks.
The analysis was performed on a systemd-based Linux system using journalctl.

## 🎯 Objective
- Detect failed SSH login attempts
- Identify suspicious IP addresses
- Understand SOC Analyst L1 investigation workflow

## 🛠️ Tools & Technologies Used
- Kali Linux
- systemd journal logs
- journalctl
- grep, awk, wc

## 🔍 Methodology
1. Accessed authentication logs using journalctl
2. Filtered failed SSH login attempts
3. Counted repeated login failures
4. Extracted attacker IP addresses
5. Analyzed brute-force patterns

## 🧪 Commands Used
sudo journalctl | grep "Failed password"
sudo journalctl | grep "Failed password" | wc -l
sudo journalctl | grep "Failed password" | awk '{print $(NF-3)}'

## 📊 Findings
Multiple failed SSH login attempts were detected from the same IP address,
indicating a possible brute-force attack.

## 🧠 SOC Analyst Conclusion
Repeated failed authentication attempts from a single source IP
suggest brute-force behavior and should be escalated for further investigation.

## 📈 Learning Outcome
- Hands-on experience with Linux log analysis
- Practical SOC L1 investigation workflow
- Understanding of authentication-based attacks

