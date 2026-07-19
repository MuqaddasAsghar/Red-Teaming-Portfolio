# Nmap Commands

This file contains all Nmap commands executed during the **Nmap Network Scanning Basics** project.

---

# 1. Verify Nmap Installation

## Command

```bash
nmap --version
```

## Purpose

Verify that Nmap is installed correctly and display the installed version.

## Important Option

| Option | Description |
|---------|-------------|
| `--version` | Displays the installed Nmap version and build information. |

## Expected Outcome

- Confirms Nmap is installed.
- Displays version information.
- Shows supported libraries and platform details.

---

# 2. Basic Port Scan

## Command

```bash
nmap 127.0.0.1
```

## Purpose

Perform a basic scan of the localhost to identify open TCP ports.

## Target

127.0.0.1 (Localhost)

## Expected Outcome

- Checks whether the host is online.
- Scans the default top 1000 TCP ports.
- Displays open ports and associated services.

Example Result:

- Port 22 → SSH

---

# 3. Service Version Detection

## Command

```bash
nmap -sV 127.0.0.1
```

## Purpose

Detect the exact version of services running on open ports.

## Important Option

| Option | Description |
|---------|-------------|
| `-sV` | Enables Service Version Detection. |

## Expected Outcome

- Detects running services.
- Displays software versions.

Example:

OpenSSH 9.9p1 Debian 3

---

# 4. Operating System Detection

## Command

```bash
nmap -O 127.0.0.1
```

## Purpose

Attempt to identify the operating system of the target.

## Important Option

| Option | Description |
|---------|-------------|
| `-O` | Enables Operating System Detection using TCP/IP fingerprinting. |

## Expected Outcome

- Identifies the operating system.
- Displays device type.
- Displays network distance.

Example:

- Linux
- General Purpose Device

---

# 5. Aggressive Scan

## Command

```bash
nmap -A 127.0.0.1
```

## Purpose

Perform a comprehensive scan using multiple advanced detection techniques.

## Important Option

| Option | Description |
|---------|-------------|
| `-A` | Enables Aggressive Scan. |

## Features Included

The `-A` option performs:

- Service Version Detection (`-sV`)
- Operating System Detection (`-O`)
- Default NSE Script Scanning
- Traceroute (when applicable)

## Expected Outcome

- Detect running services.
- Detect service versions.
- Detect operating system.
- Collect SSH host key fingerprints.
- Provide additional reconnaissance information.

---

# Summary

During this project, the following Nmap commands were successfully executed:

| Command | Purpose |
|----------|---------|
| `nmap --version` | Verify Nmap installation |
| `nmap 127.0.0.1` | Basic port scan |
| `nmap -sV 127.0.0.1` | Service version detection |
| `nmap -O 127.0.0.1` | Operating system detection |
| `nmap -A 127.0.0.1` | Aggressive scan |

---

# Notes

- All scans were performed against **127.0.0.1 (localhost)**.
- Testing was conducted inside a **Kali Linux Virtual Machine**.
- The project was completed in a controlled lab environment.
- These techniques should only be used on systems for which explicit authorization has been granted.