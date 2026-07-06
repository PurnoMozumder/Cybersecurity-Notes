# 🌐 Networking Notes
 
A collection of notes covering core networking concepts every cybersecurity professional needs to know.
 
---
 
## 📖 Table of Contents
 
- [Basic Networking](#-basic-networking)
- [OSI Model](#-osi-model)
- [TCP/IP Model](#-tcpip-model)
- [Common Ports](#-common-ports)
- [DNS](#-dns)
- [HTTP & HTTPS](#-http--https)
- [Network Troubleshooting](#-network-troubleshooting)
---
 
## 🔌 Basic Networking
 
> Notes on fundamental networking concepts.
 
- **IP Address** — A unique identifier assigned to a device on a network.
- **Subnet Mask** — Defines the network and host portions of an IP address.
- **Gateway** — The device (usually a router) that connects a local network to other networks.
- **MAC Address** — A hardware-level address unique to a network interface.
**Key Commands:**
```bash
ipconfig        # Windows - view IP configuration
ifconfig        # Linux/macOS - view IP configuration
ping <host>     # Test connectivity to a host
tracert <host>  # Windows - trace the route to a host
traceroute <host> # Linux/macOS - trace the route to a host
```
 
---
 
## 🧱 OSI Model
 
The OSI (Open Systems Interconnection) model has **7 layers**:
 
| Layer | Name         | Function                                  | Example Protocols     |
|-------|--------------|--------------------------------------------|------------------------|
| 7     | Application  | User-facing services                       | HTTP, FTP, DNS         |
| 6     | Presentation | Data translation, encryption, compression  | SSL/TLS, JPEG          |
| 5     | Session      | Manages sessions between applications       | NetBIOS, RPC           |
| 4     | Transport    | End-to-end communication, reliability      | TCP, UDP               |
| 3     | Network      | Logical addressing & routing               | IP, ICMP               |
| 2     | Data Link    | Physical addressing, error detection       | Ethernet, ARP          |
| 1     | Physical     | Raw bit transmission over physical medium  | Cables, Hubs           |
 
> 🧠 **Mnemonic:** *"All People Seem To Need Data Processing"*
 
---
 
## 📡 TCP/IP Model
 
A simplified 4-layer model used in real-world networking:
 
| Layer          | Corresponds to OSI Layers | Protocols        |
|----------------|----------------------------|------------------|
| Application    | 5, 6, 7                    | HTTP, DNS, FTP   |
| Transport      | 4                           | TCP, UDP         |
| Internet       | 3                           | IP, ICMP         |
| Network Access | 1, 2                        | Ethernet, Wi-Fi  |
 
**TCP vs UDP:**
 
| Feature      | TCP                          | UDP                     |
|--------------|-------------------------------|--------------------------|
| Connection   | Connection-oriented            | Connectionless           |
| Reliability  | Reliable (acknowledgments)     | Unreliable (no ack)      |
| Speed        | Slower                          | Faster                   |
| Use Case     | Web, Email, File Transfer       | Streaming, Gaming, DNS   |
 
---
 
## 🚪 Common Ports
 
| Port | Protocol       | Service              |
|------|----------------|----------------------|
| 20/21| FTP            | File Transfer        |
| 22   | SSH            | Secure Shell         |
| 23   | Telnet         | Remote Login         |
| 25   | SMTP           | Email Sending        |
| 53   | DNS            | Domain Name Resolution |
| 80   | HTTP           | Web Traffic          |
| 110  | POP3           | Email Retrieval      |
| 143  | IMAP           | Email Retrieval      |
| 443  | HTTPS          | Secure Web Traffic   |
| 3389 | RDP            | Remote Desktop        |
 
---
 
## 🌍 DNS (Domain Name System)
 
DNS translates human-readable domain names (e.g. `example.com`) into IP addresses.
 
**DNS Record Types:**
 
| Record | Purpose                          |
|--------|-----------------------------------|
| A      | Maps domain to IPv4 address       |
| AAAA   | Maps domain to IPv6 address       |
| CNAME  | Alias for another domain          |
| MX     | Mail server for the domain        |
| TXT    | Text records (e.g. SPF, DKIM)     |
| NS     | Name server for the domain        |
 
**Useful Commands:**
```bash
nslookup example.com
dig example.com
```
 
---
 
## 🔐 HTTP & HTTPS
 
- **HTTP** — Hypertext Transfer Protocol, unencrypted, port 80.
- **HTTPS** — HTTP Secure, encrypted with SSL/TLS, port 443.
**Common HTTP Methods:**
 
| Method | Purpose                  |
|--------|----------------------------|
| GET    | Retrieve data              |
| POST   | Submit data                |
| PUT    | Update existing resource    |
| DELETE | Remove a resource           |
 
**Common HTTP Status Codes:**
 
| Code | Meaning               |
|------|------------------------|
| 200  | OK                     |
| 301  | Moved Permanently      |
| 403  | Forbidden              |
| 404  | Not Found              |
| 500  | Internal Server Error  |
 
---
 
## 🛠️ Network Troubleshooting
 
Common tools and steps to diagnose network issues:
 
```bash
ping <host>            # Check basic connectivity
tracert / traceroute   # Trace the network path
nslookup / dig         # Check DNS resolution
netstat -an            # View active connections
ipconfig /all          # View detailed network config (Windows)
```
 
**Troubleshooting Flow:**
1. Check physical connection (cables, Wi-Fi).
2. Verify IP configuration (`ipconfig` / `ifconfig`).
3. Test connectivity with `ping`.
4. Check DNS resolution with `nslookup`.
5. Trace the route with `tracert` / `traceroute`.
---
 
## 📌 Resources
 
- [Cisco Networking Basics](https://www.cisco.com/)
- [Professor Messer - Network+](https://www.professormesser.com/)
- [TryHackMe - Networking Modules](https://tryhackme.com/)
---
 
⬅️ [Back to Main README](../README.md)
 
