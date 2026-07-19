# Nmap Advanced Scanning Commands

This document contains all Nmap commands executed during Project 02.

---

# 1. Scan Without Host Discovery

## Command

```bash
nmap -Pn 127.0.0.1
```

### Purpose

Skip host discovery and assume the target host is online before scanning.

---

# 2. Scan a Specific Port

## Command

```bash
nmap -p 22 127.0.0.1
```

### Purpose

Scan only TCP port 22 to verify whether the SSH service is running.

---

# 3. Scan Multiple Ports

## Command

```bash
nmap -p 22,80,443 127.0.0.1
```

### Purpose

Scan multiple selected ports (SSH, HTTP, and HTTPS).

---

# 4. Fast Scan

## Command

```bash
nmap -F 127.0.0.1
```

### Purpose

Perform a Fast Scan of the top 100 most common TCP ports.

---

# 5. Aggressive Timing Template

## Command

```bash
nmap -T4 127.0.0.1
```

### Purpose

Increase scanning speed using the Aggressive timing template.

---

# 6. UDP Scan

## Command

```bash
sudo nmap -sU 127.0.0.1
```

### Purpose

Scan UDP ports to identify UDP-based services.

---

# 7. Run Default NSE Scripts

## Command

```bash
nmap --script default 127.0.0.1
```

### Purpose

Execute Nmap's default scripting engine for additional service enumeration.

---

# 8. Save Scan Results

## Command

```bash
nmap -oN scan_results.txt 127.0.0.1
```

### Purpose

Save the scan results in normal text format.

---

# 9. Display Saved Results

## Command

```bash
cat scan_results.txt
```

### Purpose

Verify that the scan results were successfully saved.

---

# Commands Summary

| No. | Command | Description |
|-----|---------|-------------|
| 1 | `nmap -Pn 127.0.0.1` | Skip host discovery |
| 2 | `nmap -p 22 127.0.0.1` | Scan a specific port |
| 3 | `nmap -p 22,80,443 127.0.0.1` | Scan multiple ports |
| 4 | `nmap -F 127.0.0.1` | Fast scan |
| 5 | `nmap -T4 127.0.0.1` | Aggressive timing template |
| 6 | `sudo nmap -sU 127.0.0.1` | UDP scan |
| 7 | `nmap --script default 127.0.0.1` | Run default NSE scripts |
| 8 | `nmap -oN scan_results.txt 127.0.0.1` | Save scan output |
| 9 | `cat scan_results.txt` | Display saved scan results |