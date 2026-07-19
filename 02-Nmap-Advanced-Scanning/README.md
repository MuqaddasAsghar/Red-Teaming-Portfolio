# Nmap Advanced Scanning

## Project Overview

This project demonstrates advanced Nmap scanning techniques used during the reconnaissance phase of an authorized penetration test. The lab was performed in a controlled Kali Linux environment using localhost (127.0.0.1) as the target.

---

## Objectives

- Learn advanced Nmap scanning options.
- Perform targeted port scanning.
- Perform UDP scanning.
- Explore Nmap Scripting Engine (NSE).
- Save scan results for documentation and reporting.

---

## Lab Environment

| Item | Details |
|------|---------|
| Operating System | Kali Linux 2025.1c |
| Tool | Nmap 7.95 |
| Platform | Oracle VirtualBox |
| Target | Localhost (127.0.0.1) |

---

# Techniques Covered

- Host Discovery Control (`-Pn`)
- Targeted Port Scanning (`-p`)
- Multiple Port Scanning
- Fast Scan (`-F`)
- Timing Template (`-T4`)
- UDP Scan (`-sU`)
- Nmap Scripting Engine (NSE)
- Saving Scan Results (`-oN`)

---

# Commands Used

```bash
nmap -Pn 127.0.0.1
nmap -p 22 127.0.0.1
nmap -p 22,80,443 127.0.0.1
nmap -F 127.0.0.1
nmap -T4 127.0.0.1
sudo nmap -sU 127.0.0.1
nmap --script default 127.0.0.1
nmap -oN scan_results.txt 127.0.0.1
cat scan_results.txt
```

---

# Project Structure

```
02-Nmap-Advanced-Scanning/
│
├── screenshots/
│   ├── 00_nmap_Pn_localhost.png
│   ├── 01_nmap_port22.png
│   ├── 02_nmap_multiple_ports.png
│   ├── 03_nmap_fast_scan.png
│   ├── 04_nmap_T4_scan.png
│   ├── 05_nmap_udp_scan.png
│   ├── 06_nmap_default_scripts.png
│   ├── 07_nmap_output_saved.png
│   └── 08_scan_results_file.png
│
├── commands/
│   └── commands.md
│
├── notes/
│   └── learning_notes.md
│
├── report/
│   └── report.md
│
├── README.md
└── CHANGELOG.md
```

---

# Skills Practiced

- Network Reconnaissance
- Port Scanning
- Service Enumeration
- UDP Scanning
- Nmap Scripting Engine (NSE)
- Scan Documentation
- Report Writing

---

# Learning Outcomes

After completing this project, I learned how to:

- Skip host discovery using `-Pn`.
- Scan individual and multiple ports.
- Perform fast scans.
- Use timing templates.
- Scan UDP services.
- Execute default NSE scripts.
- Save scan results for documentation.
- Verify saved scan reports.

---

# Screenshots

This project contains **9 screenshots** demonstrating each practical task performed during the lab.

---

# Disclaimer

This project was performed in a controlled lab environment for educational purposes only. No unauthorized systems were scanned.

---

**Author:** Muqaddas Asghar

BS Cyber Security Student

HITEC University, Taxila, Pakistan