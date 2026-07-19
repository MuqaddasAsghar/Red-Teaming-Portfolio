# Project Report

# Project Title

Nmap Network Scanning Basics

---

# Objective

The objective of this project was to understand the basic functionality of Nmap by performing different types of scans on the localhost. The project focused on verifying the Nmap installation, identifying open ports, detecting service versions, identifying the operating system, and performing an aggressive scan.

---

# Lab Environment

| Item | Value |
|------|-------|
| Operating System | Kali Linux 2025.1c |
| Tool | Nmap 7.95 |
| Virtualization Platform | Oracle VirtualBox |
| Target | 127.0.0.1 (Localhost) |

---

# Task 1 – Verify Nmap Installation

## Command

```bash
nmap --version
```

## Purpose

Verify that Nmap is installed correctly and identify the installed version.

## Observation

- Nmap version 7.95 was successfully detected.
- The output displayed supported libraries and platform information.

## Conclusion

Nmap was successfully installed and ready for use.

---

# Task 2 – Basic Localhost Scan

## Command

```bash
nmap 127.0.0.1
```

## Purpose

Scan the localhost to identify open TCP ports.

## Observation

- Host was online.
- 999 TCP ports were closed.
- Port 22 (SSH) was open.

## Conclusion

The scan successfully identified the active SSH service running on the localhost.

---

# Task 3 – Service Version Detection

## Command

```bash
nmap -sV 127.0.0.1
```

## Purpose

Identify the exact version of services running on open ports.

## Observation

- SSH service detected.
- Service version identified as:

OpenSSH 9.9p1 Debian 3

- Service information indicated that the operating system was Linux.

## Conclusion

The `-sV` option provides detailed information about running services, which is useful during reconnaissance and vulnerability assessment.

---

# Task 4 – Operating System Detection

## Command

```bash
nmap -O 127.0.0.1
```

## Purpose

Attempt to identify the operating system of the target.

## Observation

- Device Type: General Purpose
- Operating System: Linux
- Network Distance: 0 hops

## Conclusion

Nmap successfully identified the target as a Linux-based operating system using TCP/IP fingerprinting.

---

# Task 5 – Aggressive Scan

## Command

```bash
nmap -A 127.0.0.1
```

## Purpose

Perform a comprehensive scan using multiple advanced detection techniques.

## Observation

The aggressive scan successfully identified:

- SSH service
- OpenSSH 9.9p1 Debian 3
- Linux operating system
- SSH host key fingerprints
- Additional service information

## Conclusion

The `-A` option combined multiple reconnaissance techniques into a single scan and provided significantly more information than the previous scans.

---

# Skills Demonstrated

During this project, the following skills were practiced:

- Verifying tool installation
- Basic TCP port scanning
- Service version detection
- Operating system detection
- Aggressive scanning
- Basic reconnaissance
- Security documentation

---

# Challenges Encountered

No major technical issues were encountered during the lab. All scans were successfully completed against the localhost in a controlled virtual environment.

---

# Overall Learning Outcome

This project provided practical experience with the basic capabilities of Nmap. It demonstrated how different scan types reveal increasing levels of information about a target system. The project also reinforced the importance of reconnaissance as the first phase of penetration testing and red teaming engagements.

---

# Ethical Consideration

All scans performed during this project targeted only my own Kali Linux localhost (127.0.0.1) inside a controlled Oracle VirtualBox lab environment.

These techniques should only be used on systems where explicit authorization has been granted.