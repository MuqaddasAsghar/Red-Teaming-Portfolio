# Nmap Network Scanning Basics

## Project Overview

This project demonstrates the basic usage of Nmap for network reconnaissance in a controlled lab environment using Kali Linux.

The project covers:

- Verifying the Nmap installation
- Basic port scanning
- Service version detection
- Operating system detection
- Aggressive scanning

The target used in this project is the local machine (127.0.0.1).

---

# Objectives

- Learn how to use Nmap.
- Understand basic network reconnaissance.
- Identify open ports.
- Detect running services.
- Identify service versions.
- Detect the operating system.
- Perform an aggressive scan.

---

# Lab Environment

| Component | Details |
|----------|---------|
| Operating System | Kali Linux 2025.1c |
| Tool | Nmap 7.95 |
| Platform | Oracle VirtualBox |
| Target | 127.0.0.1 |

---

# Project Structure

```
01-Nmap-Network-Scanning-Basics
│
├── README.md
├── CHANGELOG.md
├── screenshots/
├── commands/
├── notes/
└── report/
```

---

# Commands Covered

## Check Nmap Version

```bash
nmap --version
```

---

## Basic Scan

```bash
nmap 127.0.0.1
```

---

## Service Version Detection

```bash
nmap -sV 127.0.0.1
```

---

## Operating System Detection

```bash
nmap -O 127.0.0.1
```

---

## Aggressive Scan

```bash
nmap -A 127.0.0.1
```

---

# Screenshots

The screenshots folder contains the outputs of every command executed during this lab.

- Nmap Version
- Basic Scan
- Service Version Detection
- Operating System Detection
- Aggressive Scan

---

# Learning Outcomes

After completing this project, I learned:

- How Nmap discovers hosts.
- How to identify open ports.
- How to identify running services.
- How to detect service versions.
- How operating system detection works.
- How aggressive scanning combines multiple reconnaissance techniques.

---

# Disclaimer

This project was performed only inside a personal virtual lab environment for educational and authorized cybersecurity practice.

Never scan systems without proper authorization.