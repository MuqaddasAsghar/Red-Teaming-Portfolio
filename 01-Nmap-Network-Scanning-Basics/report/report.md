# Project Report

# Project Title

Nmap Network Scanning Basics

## Environment

- Operating System: Kali Linux 2025.1c
- Tool: Nmap 7.95
- Platform: Oracle VirtualBox

---

## Task 1 – Verify Nmap Installation

### Command

```bash
nmap --version
```

### Observation

Nmap version 7.95 was successfully detected.

### Conclusion

Nmap is installed and ready for use.

---

## Task 2 – Basic Localhost Scan

### Command

```bash
nmap 127.0.0.1
```

### Observation

- Host is online.
- Port 22 (SSH) is open.
- 999 TCP ports are closed.

### Conclusion

The localhost scan successfully identified the active SSH service.

---

## Task 3 – Service Version Detection

### Command

```bash
nmap -sV 127.0.0.1
```

### Observation

- SSH service detected.
- Version identified as OpenSSH 9.9p1 Debian 3.

### Conclusion

The `-sV` option provides additional information about service versions, which is useful during reconnaissance.

---

## Task 4 – Operating System Detection

### Command

```bash
nmap -O 127.0.0.1
```

### Observation

- Device Type: General Purpose
- Operating System: Linux
- Network Distance: 0 hops

### Conclusion

Nmap successfully identified the target as a Linux-based operating system using OS fingerprinting.
---

## Task 5 – Aggressive Scan

### Command

```bash
nmap -A 127.0.0.1
```

### Observation

- SSH service detected.
- OpenSSH version identified.
- Linux operating system detected.
- SSH host key fingerprints collected.
- Scan completed successfully.

### Conclusion

The aggressive scan combined multiple detection techniques and produced a more comprehensive view of the target than previous scans.
