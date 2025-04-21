# 🌐 Computer Networks Viva Preparation Guide - Answers

## 🔹 Introduction to Computer Networks

### Q: What is a Computer Network?
**A:** A computer network is a collection of interconnected devices that share resources and data using communication channels.

### Q: Types of Networks
- **LAN**: Limited area like home, school
- **MAN**: Covers a city or campus
- **WAN**: Large area like countries (e.g., Internet)
- **PAN**: Personal devices within a few meters

### Q: Topologies
- **Star**: Central hub (robust, expensive)
- **Ring**: Circular data path
- **Bus**: Single cable (cheap, less secure)
- **Mesh**: Every device connected to all others
- **Hybrid**: Combination of topologies

### Q: OSI vs TCP/IP Models
- **OSI**: 7 layers, theoretical model
- **TCP/IP**: 4 layers, practical implementation

---

## 🔹 OSI Model (7 Layers)
1. **Physical** – Transmits bits via cables
2. **Data Link** – Framing, MAC address, error detection
3. **Network** – Routing, logical addressing (IP)
4. **Transport** – End-to-end connection, TCP/UDP
5. **Session** – Session control and synchronization
6. **Presentation** – Data translation, encryption, compression
7. **Application** – User interaction, protocols like HTTP, FTP

---

## 🔹 TCP/IP Model (4 Layers)
- **Application** – User-facing protocols (HTTP, FTP)
- **Transport** – TCP/UDP, port numbers
- **Internet** – IP addressing, routing
- **Network Access** – Physical transmission, MAC

---

## 🔹 Transmission Media

### Guided:
- **Twisted Pair**: Cheap, used in LANs
- **Coaxial**: TV cables, better shielding
- **Fiber Optics**: High speed, long distance, expensive

### Unguided:
- **Radio Waves**: Wi-Fi, long-range
- **Microwaves**: Point-to-point, satellite
- **Infrared**: Short-range, line-of-sight

---

## 🔹 Switching Techniques
- **Circuit Switching**: Dedicated path (e.g., telephone)
- **Packet Switching**: Data split into packets (e.g., Internet)
- **Message Switching**: Whole message stored & forwarded

---

## 🔹 IP Addressing
- **IPv4**: 32-bit, e.g., 192.168.1.1
- **IPv6**: 128-bit, supports more devices
- **Classes**:
  - A (1–126)
  - B (128–191)
  - C (192–223)
  - D (224–239 - Multicast)
  - E (240–255 - Reserved)
- **Subnetting**: Dividing network into smaller parts
- **Supernetting**: Combining networks
- **Public vs Private**: Private used in LAN, not routable on Internet
- **Loopback**: 127.0.0.1 for self-testing

---

## 🔹 Protocols and Ports
- **HTTP**: 80
- **HTTPS**: 443
- **FTP**: 21
- **SFTP/SSH**: 22
- **SMTP**: 25
- **POP3**: 110
- **IMAP**: 143
- **DNS**: 53
- **DHCP**: 67 (server), 68 (client)
- **TELNET**: 23

---

## 🔹 Routing and Switching
- **Static Routing**: Manual route configuration
- **Dynamic Routing**: Routes learned via protocols
- **RIP**: Distance-vector
- **OSPF**: Link-state, faster
- **BGP**: Between ISPs

### Devices:
- **Hub**: Broadcasts to all
- **Switch**: Forwards based on MAC
- **Router**: Routes based on IP

### MAC vs IP
- **MAC**: Physical address, fixed
- **IP**: Logical address, can change

---

## 🔹 Transport Layer

### TCP vs UDP
- **TCP**: Reliable, connection-oriented (e.g., HTTP)
- **UDP**: Faster, no guarantee (e.g., streaming)

### TCP Three-way Handshake
1. SYN
2. SYN-ACK
3. ACK

### Flow Control
- **Sliding Window**: Efficient, uses window size
- **Stop-and-Wait**: Simple, slow
- **Go-Back-N**: Retransmits from error

### Congestion Control
- **Slow Start**
- **AIMD**: Additive Increase, Multiplicative Decrease

---

## 🔹 Application Layer Protocols
- **HTTP**: Web pages
- **FTP**: File transfer
- **SMTP**: Email sending
- **DNS**: Name to IP
- **DHCP**: Assigns IP dynamically

### Architectures
- **Client-Server**: Centralized control
- **P2P**: Equal peers, decentralized

---

## 🔹 Network Devices
- **Repeater**: Signal booster
- **Hub**: Broadcast device
- **Switch**: Smart hub, MAC-based
- **Router**: Connects networks
- **Bridge**: Connects LANs
- **Gateway**: Protocol converter
- **Modem**: Modulates/demodulates signals

---

## 🔹 Network Security
- **Firewall**: Filters traffic
- **Encryption**:
  - Symmetric (same key)
  - Asymmetric (public/private key)
- **VPN**: Secure tunnel over Internet
- **SSL/TLS**: Web security

### Attacks:
- **DoS/DDoS**: Overloads server
- **MITM**: Eavesdropping
- **Phishing**: Fake links/forms

---

## 🔹 Miscellaneous Topics
- **DNS**: Resolves domain names to IPs
- **ARP**: Maps IP to MAC
- **ICMP**: Sends error/control messages (e.g., Ping)
- **NAT**: Translates private IPs to public
- **DHCP**: Assigns IPs automatically
- **URL vs IP**: URL is human-friendly, IP is computer-readable
- **Proxy Server**: Intermediary for requests

---

## 🔹 Common Viva Questions

### Q: Difference between TCP and UDP?
- **TCP**: Reliable, ordered, slower
- **UDP**: Fast, no guarantee

### Q: What is an IP address vs MAC address?
- **IP**: Logical, for routing
- **MAC**: Physical, for local delivery

### Q: Explain OSI layers with functions
**A:** See OSI section above

### Q: Hub vs Switch vs Router
- **Hub**: Broadcasts
- **Switch**: MAC-based forwarding
- **Router**: IP-based routing

### Q: What is Subnetting?
**A:** Dividing IP network into subnets to improve management and efficiency

### Q: What is the use of DNS?
**A:** Resolves domain names to IP addresses

### Q: What happens when you type a URL?
1. DNS lookup
2. IP address found
3. TCP connection established
4. HTTP request sent
5. Webpage received and rendered

### Q: How does the Internet work?
**A:** Uses TCP/IP, routers, ISPs, DNS, and various protocols to deliver data between devices globally

---

> 💡 **Tip:** Use real-world analogies like postal system (IP = address, port = door number) to explain complex terms!

