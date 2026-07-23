# Project Report

# Project Information

**Project Number:** 03

**Project Title:** Wireshark Packet Analysis

**Tool Used:** Wireshark 4.4.4

**Operating System:** Kali Linux

---

# Objective

The objective of this project was to analyze live network traffic using Wireshark and gain practical experience with common network protocols.

The project focused on capturing, filtering, and analyzing packets generated during normal network communication.

---

# Activities Performed

The following practical tasks were completed during this project:

- Verified Wireshark installation
- Started live packet capture
- Captured network traffic
- Analyzed TCP packets
- Generated and analyzed DNS traffic
- Generated and analyzed ARP traffic
- Observed ICMPv6 packets
- Generated HTTPS traffic using curl
- Analyzed TLS communication
- Saved packet capture for future analysis

---

# Protocols Analyzed

## TCP

Observed TCP communication between local and remote hosts.

Key observations:

- Source Port
- Destination Port
- Reliable communication

---

## DNS

Generated DNS traffic using:

```bash
nslookup google.com
```

Observed:

- DNS Query
- DNS Response
- Domain name resolution

---

## ARP

Generated ARP traffic using:

```bash
ping -c 2 10.0.3.3
```

Observed:

- ARP Request
- ARP Reply

---

## ICMPv6

Observed IPv6 Neighbor Discovery packets using the `icmpv6` display filter.

These packets demonstrated IPv6 network communication and address resolution.

---

## HTTPS / TLS

Generated encrypted traffic using:

```bash
curl https://example.com
```

Observed:

- TLS Handshake
- Server Hello
- Application Data

This demonstrated secure encrypted communication over HTTPS.

---

# Files Produced

- Wireshark screenshots
- Packet capture (.pcapng)
- Commands documentation
- Learning notes
- README
- Project report

---

# Skills Developed

- Packet Analysis
- Wireshark
- TCP/IP Networking
- DNS Analysis
- ARP Analysis
- ICMPv6 Analysis
- HTTPS/TLS Analysis
- Network Troubleshooting

---

# Conclusion

This project provided practical experience in capturing and analyzing live network traffic using Wireshark.

Through hands-on analysis of TCP, DNS, ARP, ICMPv6, and HTTPS/TLS traffic, I developed a stronger understanding of how common network protocols operate and how Wireshark can be used for troubleshooting and cybersecurity investigations.