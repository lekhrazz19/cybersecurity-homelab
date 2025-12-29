# 🔍 Nmap Network Scanning

## Objective
Perform network reconnaissance to identify open ports, running services, and potential vulnerabilities on the Ubuntu Server target machine.

---

## What is Nmap?
**Nmap (Network Mapper)** is a powerful open-source tool used for:
- Network discovery
- Port scanning
- Service version detection
- Operating system fingerprinting
- Vulnerability assessment

---
## Scanning Commands Used

### 1. Basic Scan
```bash
nmap <target-ip>
```
**Purpose**: Quick scan of most common 1000 ports

### 2. Full Port Scan
```bash
nmap -p- <target-ip>
```
**Purpose**: Scan all 65535 ports

### 3. Service Version Detection
```bash
nmap -sV <target-ip>
```
**Purpose**: Identify service versions running on open ports

### 4. Operating System Detection
```bash
sudo nmap -O <target-ip>
```
**Purpose**: Detect target operating system

### 5. Aggressive Scan
```bash
sudo nmap -A <target-ip>
```
**Purpose**: Comprehensive scan including OS detection, version detection, script scanning, and traceroute

### 6. Specific Port Scan
```bash
nmap -p 22,80,443 <target-ip>
```
**Purpose**: Scan specific ports only

---

## What Was Discovered

### Open Ports Identified
| Port | Service | Version | Purpose |
|------|---------|---------|--------|
| **22** | SSH | OpenSSH 8.x | Remote access |
| **80** | HTTP | Apache 2.4.x | Web server |
| **3306** | MySQL | 8.0.x | Database server |

### Service Details
- **SSH**: Secure Shell for remote administration
- **Apache**: Web server hosting DVWA
- **MySQL**: Database backend for web applications

---

## Learning Outcomes

✅ **Technical Skills:**
- Understanding of network scanning methodology
- Port identification and analysis
- Service enumeration techniques
- Interpreting Nmap output

✅ **Security Insights:**
- Identifying attack surface
- Recognizing potential entry points
- Understanding service exposure risks
- Planning further penetration testing steps

---

## Security Implications

⚠️ **Findings:**
- Open ports indicate potential attack vectors
- Service versions may have known vulnerabilities
- Unnecessary services increase risk
- Proper port management is crucial

✅ **Recommendations:**
- Close unused ports
- Keep services updated
- Implement firewall rules
- Monitor access logs

---

## Example Output

```
Starting Nmap scan...

PORT     STATE SERVICE VERSION
22/tcp   open  ssh     OpenSSH 8.2p1 Ubuntu
80/tcp   open  http    Apache httpd 2.4.41
3306/tcp open  mysql   MySQL 8.0.32

OS details: Linux 5.4
Network Distance: 1 hop

Nmap scan completed: 1 IP address scanned
```

---

## Next Steps

✅ Network reconnaissance completed
✅ Attack surface identified
✅ Services enumerated

➡️ Proceed to [DVWA Testing](dvwa-testing.md)

---

## Ethical Considerations

⚠️ **Important:**
- Only scan systems you own or have permission to test
- Unauthorized scanning is illegal
- Document all scanning activities
- This was performed in a controlled lab environment

---

## Additional Resources

- [Nmap Official Documentation](https://nmap.org/docs.html)
- [Nmap Port Scanning Basics](https://nmap.org/book/man-port-scanning-basics.html)
- [Common Nmap Commands Cheat Sheet](https://www.stationx.net/nmap-cheat-sheet/)
