# 🖥️ Windows Networking & System Commands Cheat Sheet

---

## 🔍 Find All MAC Addresses
```bash
arp -a
```

Displays all MAC addresses and corresponding IPs cached in the ARP table.

🎯 Find MAC Address of the Local System
```bash
getmac
```
Shows the MAC address of your network interfaces.

🌐 IP Address Information
```bash
ipconfig
```
```bash
ipconfig /all
```
Displays basic (or detailed with /all) IP configuration including IP address, subnet mask, gateway, and DNS servers.

🧠 System Information
```bash
systeminfo
```

Displays complete system info such as OS version, build, architecture, BIOS, and more.

🧹 Flush DNS Cache

```bash
ipconfig /flushdns
```
Clears the DNS resolver cache.

🔎 View DNS Cache
```bash
ipconfig /displaydns
```
Displays contents of the DNS resolver cache.

🌐 Find Domain IP, Website IP & MAC Address

```bash
nslookup google.com
```
Resolves the domain name to an IP address using DNS.

🛠️ Force Group Policy Update (Windows Server)

```bash
gpupdate /force
```
Forces an immediate update of Group Policy settings.

📦 DNS Record Lookup Types (Using NSLOOKUP)

Record Type	Command Example	Description
1. A	nslookup -type=a google.com	IPv4 address
2. AAAA	nslookup -type=aaaa google.com	IPv6 address
3. NS	nslookup -type=ns google.com	Name servers
4. MX	nslookup -type=mx google.com	Mail exchange servers
5. CNAME	nslookup -type=cname google.com	Canonical name
6. SOA	nslookup -type=soa google.com	Start of authority
7. PTR	nslookup -type=ptr [IP]	Reverse lookup for IP to domain
8. RV (N/A)	nslookup -type=rv google.com	⚠️ Likely a typo, not a valid type

📘 Common Windows Networking Commands
1. ipconfig
Displays IP configuration of the system.

```bash
ipconfig
```

2. nslookup
Queries DNS servers for domain details.

```bash
nslookup google.com
```

3. ping
Tests connectivity to a host.

```bash
ping www.example.com
```

4. tracert
Traces the route packets take to reach the destination.

```bash
tracert www.example.com
```

5. netstat
Displays all active network connections.

```bash
netstat
```

6. arp
Displays IP-to-MAC address mappings.

```bash
arp -a
```

7. nbtstat
Displays NetBIOS over TCP/IP statistics.

```bash
nbtstat -n
```

8. systeminfo
Shows detailed system hardware and software information.

```bash
systeminfo
```

9. pathping
Combines ping and tracert to show latency and packet loss over time.

```bash
pathping www.example.com
```

10. getmac
Displays MAC addresses for local network interfaces.

```bash
getmac
```

✅ Notes
Use cmd as Administrator for many of these commands to avoid permission issues.

Replace domain names and IPs with your target as needed.

Keep your system and DNS settings up to date for accurate results.
