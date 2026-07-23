# Commands Used – Project 03

This document contains all commands used during the Wireshark Packet Analysis lab.

---

# 1. Verify Wireshark Installation

```bash
wireshark --version
```

Purpose:
- Verify that Wireshark is installed correctly.
- Display the installed version.

---

# 2. Start Live Packet Capture

Wireshark was launched and live packet capture was started using the available network interface.

Purpose:
- Capture real-time network traffic.

---

# 3. TCP Packet Analysis

Display Filter:

```text
tcp
```

Purpose:
- Display only TCP packets.

---

# 4. DNS Packet Analysis

Terminal Command:

```bash
nslookup google.com
```

Display Filter:

```text
dns
```

Purpose:
- Generate DNS traffic.
- Observe DNS query and response packets.

---

# 5. ARP Packet Analysis

Terminal Command:

```bash
ping -c 2 10.0.3.3
```

Display Filter:

```text
arp
```

Purpose:
- Generate ARP traffic.
- Observe ARP Request and ARP Reply packets.

---

# 6. ICMPv6 Packet Analysis

Display Filter:

```text
icmpv6
```

Purpose:
- Analyze IPv6 Neighbor Discovery and ICMPv6 traffic.

---

# 7. HTTPS / TLS Packet Analysis

Terminal Command:

```bash
curl https://example.com
```

Display Filter:

```text
tls
```

Purpose:
- Generate HTTPS traffic.
- Observe encrypted TLS communication.

---

# 8. Save Packet Capture

File → Save As

Filename:

```text
project03_capture.pcapng
```

Purpose:
- Save captured packets for future analysis.

---

# Summary

The following protocols were successfully analyzed:

- TCP
- DNS
- ARP
- ICMPv6
- HTTPS/TLS