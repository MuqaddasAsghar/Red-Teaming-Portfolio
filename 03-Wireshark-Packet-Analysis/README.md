# Project 03 – Wireshark Packet Analysis

## 📌 Overview

This project demonstrates the fundamentals of network traffic analysis using **Wireshark**, one of the most widely used network protocol analyzers.

The objective of this lab was to capture and inspect different types of network traffic generated during normal network communication and understand how various protocols operate in real-world environments.

---

## 🎯 Objectives

- Install and verify Wireshark
- Capture live network traffic
- Analyze TCP packets
- Analyze DNS queries and responses
- Analyze ARP packets
- Analyze ICMPv6 packets
- Analyze HTTPS/TLS traffic
- Save packet captures for future analysis

---

## 🛠️ Tools Used

- Kali Linux
- Wireshark 4.4.4
- Terminal
- Ping
- NSLookup
- Curl

---

## 📂 Project Structure

```
03-Wireshark-Packet-Analysis/
│
├── README.md
├── CHANGELOG.md
├── commands/
│   └── commands.md
├── notes/
│   └── learning_notes.md
├── report/
│   └── report.md
├── capture/
│   └── project03_capture.pcapng
└── screenshots/
    ├── 00_wireshark_version.png
    ├── 01_capture_started.png
    ├── 02_live_capture.png
    ├── 03_tcp_filter.png
    ├── 04_dns_filter.png
    ├── 05_arp_filter.png
    ├── 06_icmpv6_filter.png
    └── 07_https_tls_capture.png
```

---

## 📷 Screenshots

| Screenshot | Description |
|------------|-------------|
| 00_wireshark_version.png | Wireshark version verification |
| 01_capture_started.png | Live packet capture started |
| 02_live_capture.png | Capturing network traffic |
| 03_tcp_filter.png | TCP traffic analysis |
| 04_dns_filter.png | DNS query and response analysis |
| 05_arp_filter.png | ARP request and reply analysis |
| 06_icmpv6_filter.png | ICMPv6 packet analysis |
| 07_https_tls_capture.png | HTTPS/TLS packet analysis |

---

## 📖 Key Concepts Learned

- Packet Capture
- TCP Communication
- DNS Resolution
- ARP Protocol
- ICMPv6
- HTTPS Communication
- TLS Encryption
- Packet Filtering
- Network Troubleshooting

---

## 📁 Capture File

The complete packet capture is included in:

```
capture/project03_capture.pcapng
```

---

## 🎓 Learning Outcomes

After completing this project, I learned how to:

- Capture live network traffic
- Apply protocol-based filters
- Identify TCP sessions
- Inspect DNS lookups
- Understand ARP communication
- Observe ICMPv6 traffic
- Analyze encrypted HTTPS/TLS communication
- Save and review packet captures for further investigation

---

## ⚠️ Disclaimer

This project was performed in an authorized lab environment for educational purposes only.

No unauthorized systems were scanned, attacked, or accessed.

---

## 🏁 Conclusion

This project strengthened my understanding of packet analysis and network protocols using Wireshark. The practical experience gained through capturing and analyzing live traffic provides a strong foundation for future studies in network security, incident response, threat hunting, and Red Teaming.