# Nmap Advanced Scanning

## Objective

Learn advanced Nmap scanning techniques including host discovery, targeted port scanning, fast scanning, timing templates, UDP scanning, Nmap Scripting Engine (NSE), and saving scan results in a controlled Kali Linux lab environment.

---

## Environment

- Operating System: Kali Linux 2025.1c
- Tool: Nmap 7.95
- Virtualization Platform: Oracle VirtualBox
- Target: Localhost (127.0.0.1)

---

# Host Discovery with -Pn

## Command

```bash
nmap -Pn 127.0.0.1
```

## Purpose

Skip host discovery (ping) and assume the target is online before starting the scan.

## Observation

- Host was reachable.
- Port 22 (SSH) was open.
- 999 TCP ports were closed.

## Learning

Normally, Nmap performs host discovery before scanning. The `-Pn` option disables this step and is useful when ICMP or ping requests are blocked by a firewall.

---

# Scan a Specific Port

## Command

```bash
nmap -p 22 127.0.0.1
```

## Purpose

Scan only a specific TCP port.

## Observation

- Port 22 was open.
- SSH service was detected.

## Learning

The `-p` option allows targeted scanning of one or more ports instead of scanning the default top 1000 TCP ports.

---

# Scan Multiple Ports

## Command

```bash
nmap -p 22,80,443 127.0.0.1
```

## Purpose

Scan multiple selected ports.

## Observation

- Port 22: Open (SSH)
- Port 80: Closed (HTTP)
- Port 443: Closed (HTTPS)

## Learning

Scanning selected ports is faster and useful when only specific services need to be checked.

---

# Fast Scan

## Command

```bash
nmap -F 127.0.0.1
```

## Purpose

Perform a fast scan of the top 100 most common TCP ports.

## Observation

- Port 22 was open.
- 99 TCP ports were closed.

## Learning

The `-F` option reduces scan time by scanning fewer ports than the default scan.

---

# Timing Template (-T4)

## Command

```bash
nmap -T4 127.0.0.1
```

## Purpose

Increase scan speed using the Aggressive timing template.

## Observation

- Host detected successfully.
- Port 22 remained open.
- Scan completed successfully.

## Learning

The `-T4` timing template performs faster scans and is commonly used during authorized penetration testing.

---

# UDP Scan

## Command

```bash
sudo nmap -sU 127.0.0.1
```

## Purpose

Scan UDP ports on the target.

## Observation

- All scanned UDP ports were closed.
- No common UDP services were running.

## Learning

UDP scanning is important because services such as DNS, DHCP, NTP, and SNMP commonly use UDP instead of TCP.

---

# Nmap Scripting Engine (NSE)

## Command

```bash
nmap --script default 127.0.0.1
```

## Purpose

Run Nmap's default NSE scripts.

## Observation

- SSH service detected.
- SSH host keys (ECDSA and ED25519) were identified.

## Learning

NSE scripts provide additional service information beyond basic port scanning and assist in enumeration during reconnaissance.

---

# Saving Scan Results

## Command

```bash
nmap -oN scan_results.txt 127.0.0.1
```

## Verify Saved Output

```bash
cat scan_results.txt
```

## Purpose

Save scan results to a text file for later analysis and reporting.

## Observation

- Scan results were successfully saved.
- File contents matched the terminal output.

## Learning

Saving scan results is a standard practice during penetration testing and security assessments because it simplifies documentation and report writing.

---

# Summary

During this project, the following Nmap features were practiced:

- Host Discovery Control (`-Pn`)
- Targeted Port Scanning (`-p`)
- Multiple Port Scanning
- Fast Scanning (`-F`)
- Timing Templates (`-T4`)
- UDP Scanning (`-sU`)
- Nmap Scripting Engine (`--script default`)
- Saving Scan Results (`-oN`)