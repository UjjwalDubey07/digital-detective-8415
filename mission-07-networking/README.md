# Mission 7: How Computers Communicate

## 1. Task / Objective
Explain network concepts (LAN, MAN, WAN, DNS, Router, Protocol, Packet Switching, Client-Server), observe connectivity and DNS lookup, and describe the website request flow.

## 2. Work Completed
- Completed network concepts table with explanations and examples.
- Ran connectivity test (`ping`) and DNS lookup (`dig`) against `tiktok.com`.
- Documented 7-step website request flow using client, server, DNS, and protocol terminology.

## 3. Commands / Tools Used
| Command | Purpose |
| :--- | :--- |
| `ping -c 4 tiktok.com` | Test reachability and measure latency to a public host (ICMP echo). |
| `dig tiktok.com +short` | Perform DNS lookup to retrieve IP address(es) for a domain. |

## 4. My Understanding

### Network Concepts
| Concept | Explanation | Example |
| :--- | :--- | :--- |
| **LAN** | Small-area network (home, office) connecting devices via Ethernet/Wi-Fi. | Home Wi-Fi connecting laptop, phone, printer. |
| **MAN** | City/campus-wide network linking multiple LANs. | University campus network. |
| **WAN** | Large geographical network connecting many LANs/MANs; the Internet is the largest. | The Internet; corporate multi-site network. |
| **DNS** | Distributed directory translating domain names to IP addresses. | `google.com` → `142.250.190.46` |
| **Router** | Device connecting networks and forwarding packets by destination IP. | Home router linking LAN to ISP. |
| **Protocol** | Rules defining how devices format, transmit, and interpret data. | HTTP, TCP/IP, DNS, DHCP. |
| **Packet Switching** | Data split into packets, routed independently, reassembled at destination. | Email split into packets, reassembled at recipient. |
| **Client-Server** | Client requests services; server provides responses. | Browser (client) ↔ Web server (server). |

### Connectivity & DNS Observation
**Command output (redacted):**
```text
$ ping -c 4 tiktok.com
PING tiktok.com (23.11.215.138): 56 data bytes
64 bytes from 23.11.215.138: icmp_seq=0 ttl=57 time=5.207 ms
64 bytes from 23.11.215.138: icmp_seq=1 ttl=57 time=10.035 ms
64 bytes from 23.11.215.138: icmp_seq=2 ttl=57 time=4.538 ms
64 bytes from 23.11.215.138: icmp_seq=3 ttl=57 time=36.983 ms

...
--- tiktok.com ping statistics ---
4 packets transmitted, 4 packets received, 0.0% packet loss
round-trip min/avg/max/stddev = 4.538/14.191/36.983/13.329 ms

$ dig tiktok.com +short
23.62.20.77
23.62.20.78
23.53.3.175
23.62.20.79
23.62.20.85
23.53.3.172
23.53.3.168

Answers:
1. Connectivity test: Checks if target host is reachable via ICMP; confirms network path, routing, and measures latency.
2. DNS lookup: Displays the IP address(es) (A/AAAA records) for a domain — the address browsers connect to.
3. DNS role: Translates human-readable domain names to numeric IPs so clients can establish TCP connections to servers.

Website Request Flow (7 Steps)

1. User enters URL — Browser (client) receives https://example.com.
2. DNS Resolution — Client queries DNS resolver → root → .com TLD → authoritative server → returns IP (93.184.216.34).
3. TCP Handshake — Client initiates TCP 3-way handshake (SYN, SYN-ACK, ACK) with server on port 443.
4. TLS Handshake — Client and server negotiate encryption, verify certificate, establish session keys.
5. HTTP Request — Client sends GET / HTTP/1.1 (or HTTP/2) over encrypted TLS tunnel.
6. Server Response — Server returns 200 OK with headers and HTML body.
7. Render Page — Browser parses HTML, fetches sub-resources (CSS, JS, images), executes scripts, displays page.

5. Difficulties Faced

["Initially confused TCP vs TLS handshake order; clarified by reading about HTTPS stack."]

6. How I Resolved Them

["Reviewed that TLS runs on top of TCP."]

7. Evidence / Files

- This README with tables and command output.
- No screenshots (privacy-safe text output only).
