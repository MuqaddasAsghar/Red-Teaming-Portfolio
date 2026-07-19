# Nmap Network Scanning Basics

---

# Objective

The objective of this lab is to learn the basic functionality of Nmap by performing different types of scans on the localhost. During this project, I learned how to identify open ports, detect running services, determine service versions, identify the operating system, and perform an aggressive scan.

---

# Lab Environment

| Item | Value |
|------|-------|
| Operating System | Kali Linux 2025.1c |
| Tool | Nmap 7.95 |
| Platform | Oracle VirtualBox |
| Target | 127.0.0.1 (Localhost) |

---

# What is Nmap?

Nmap (Network Mapper) is one of the most widely used open-source tools in cybersecurity. It is mainly used for:

- Network Discovery
- Port Scanning
- Service Enumeration
- Operating System Detection
- Security Auditing
- Reconnaissance during Penetration Testing
- Red Team Assessments

Nmap is included by default in Kali Linux.

---

# Practical Exercise 1 — Verify Nmap Installation

## Command

```bash
nmap --version
```

## Why did we use this command?

Before using any security tool, we should verify that it is installed correctly and check its version.

## Syntax Breakdown

- `nmap` → Launches the Nmap tool.
- `--version` → Displays version information.

## Output Summary

The command displayed:

- Nmap Version: 7.95
- Supported libraries
- Platform information

## What did I learn?

- Nmap is already installed in Kali Linux.
- Version information is useful because different versions support different features.

## Real-World Usage

Security professionals always verify tool versions before beginning an assessment.

---

# Practical Exercise 2 — Basic Port Scan

## Command

```bash
nmap 127.0.0.1
```

## Why did we use this command?

To identify which TCP ports are open on the localhost.

## Syntax Breakdown

- `nmap` → Starts Nmap.
- `127.0.0.1` → The localhost IP address.

## Output Summary

The scan showed:

- Host is up.
- 999 ports are closed.
- Port 22 is open.

Open Port:

| Port | Service |
|------|----------|
|22|SSH|

## Detailed Explanation

Nmap scanned the default top 1000 TCP ports.

Only one port was open:

Port 22 → SSH (Secure Shell)

This indicates that the SSH service is currently running.

## What did I learn?

- Nmap checks network ports.
- Open ports indicate active services.
- SSH commonly uses Port 22.

## Real-World Usage

Basic scans are usually the first step during reconnaissance.

---

# Practical Exercise 3 — Service Version Detection

## Command

```bash
nmap -sV 127.0.0.1
```

## Why did we use this command?

To identify the exact version of the running service.

## Syntax Breakdown

- `-sV` → Enables Service Version Detection.

## Output Summary

Nmap identified:

- Service: SSH
- Version:

OpenSSH 9.9p1 Debian 3

## Detailed Explanation

Knowing that SSH is running is useful.

Knowing the exact software version is much more useful because vulnerability databases (CVE, NVD, Exploit-DB) search by software version.

## What did I learn?

- Version detection provides detailed information.
- Service versions help identify known vulnerabilities.

## Real-World Usage

Red Teamers perform service version detection before searching for exploits.

---

# Practical Exercise 4 — Operating System Detection

## Command

```bash
nmap -O 127.0.0.1
```

## Why did we use this command?

To identify the operating system running on the target.

## Syntax Breakdown

- `-O` → Enables Operating System Detection.

## Output Summary

Nmap detected:

Device Type:

General Purpose

Operating System:

Linux

Network Distance:

0 hops

## Detailed Explanation

Nmap analyzes TCP/IP characteristics to estimate the operating system.

Although it may not always be 100% accurate, it often provides valuable information.

## What did I learn?

- Nmap can estimate operating systems.
- OS detection is useful during reconnaissance.
- The detected OS helps determine possible attack paths.

## Real-World Usage

Attackers and Red Teams identify operating systems before selecting exploitation techniques.

---

# Practical Exercise 5 — Aggressive Scan

## Command

```bash
nmap -A 127.0.0.1
```

## Why did we use this command?

To perform multiple advanced detection techniques using a single command.

## Syntax Breakdown

- `-A` → Enables Aggressive Scan.

This option combines:

- Service Version Detection
- Operating System Detection
- NSE Script Scanning
- Traceroute

## Output Summary

The scan identified:

- SSH Service
- OpenSSH 9.9p1 Debian 3
- Linux Operating System
- SSH Host Key Fingerprints

## Detailed Explanation

This scan produced much more information than the previous scans because several detection techniques were executed together.

The SSH host key fingerprints were also displayed.

These fingerprints uniquely identify the SSH server.

## What did I learn?

- The `-A` option provides comprehensive reconnaissance information.
- It combines multiple Nmap features into one scan.
- It saves time during authorized security assessments.

## Real-World Usage

Aggressive scanning is commonly used during penetration testing after obtaining proper authorization.

---

# Key Takeaways

During this project I learned:

- How to verify Nmap installation.
- How to perform a basic port scan.
- How to identify running services.
- How to detect service versions.
- How to detect operating systems.
- How to perform aggressive scans.
- Why reconnaissance is the first phase of penetration testing and red teaming.

---

# Ethical Consideration

All scans performed in this project targeted only my own Kali Linux localhost (127.0.0.1) inside a controlled virtual lab environment.

These techniques should only be used on systems where explicit authorization has been granted.