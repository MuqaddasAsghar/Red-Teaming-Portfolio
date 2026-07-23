# Project Report – Information Gathering

## Project Name
Information Gathering using WHOIS, DIG, HOST, NSLOOKUP, CURL and TRACEROUTE

## Objective

The objective of this project was to perform passive information gathering on a public domain using common Linux reconnaissance tools. The goal was to understand how attackers and penetration testers collect publicly available information before starting any security assessment.

---

## Environment

- Operating System: Kali Linux 2025.1c
- Platform: VirtualBox
- Tools Used:
  - whois
  - dig
  - host
  - nslookup
  - curl
  - traceroute

---

## Activities Performed

### 1. Verified Tool Installation

Verified that all required reconnaissance tools were installed successfully.

---

### 2. WHOIS Enumeration

Collected domain registration information including:

- Registrar
- Creation Date
- Expiration Date
- Name Servers
- DNSSEC Status

---

### 3. DNS Lookup using DIG

Retrieved DNS A records of the target domain.

Observed multiple IPv4 addresses returned by the DNS server.

---

### 4. DNS Lookup using HOST

Retrieved:

- IPv4 addresses
- IPv6 addresses
- Mail exchange information

---

### 5. DNS Lookup using NSLOOKUP

Verified domain resolution using the configured DNS server.

---

### 6. HTTP Header Inspection

Used curl to retrieve HTTP response headers.

Observed:

- HTTP Status Code
- Content Type
- Server Headers
- Security Headers

---

### 7. Network Route Discovery

Used traceroute to observe the routing path from the local machine towards the target.

Only the first hop responded while later hops were filtered, which is common on modern networks.

---

## Findings

- Public domain information can be collected without authentication.
- DNS records reveal important infrastructure information.
- WHOIS provides ownership and registration details.
- HTTP headers reveal server configuration and security mechanisms.
- Traceroute demonstrates how packets travel through the network.

---

## Conclusion

This project demonstrated the fundamentals of passive reconnaissance using standard Linux networking tools. These techniques are commonly used during the information gathering phase of penetration testing and provide valuable insight into publicly accessible infrastructure before active testing begins.