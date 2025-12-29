# 🐻 Kali Linux Setup (via WSL)

## Overview
This document outlines the setup and configuration of **Kali Linux** running on **Windows Subsystem for Linux (WSL)** as the attacker machine in the cybersecurity homelab.

---

## Installation Steps

### 1. Enable WSL on Windows
```powershell
wsl --install
```

### 2. Install Kali Linux from Microsoft Store
- Open Microsoft Store
- Search for "Kali Linux"
- Click Install
- Launch and create user account

### 3. Update System
```bash
sudo apt update && sudo apt upgrade -y
```

---

## Essential Tools Installation

### Network Scanning Tools
```bash
# Nmap - Network scanner
sudo apt install nmap -y

# Netcat - Network utility
sudo apt install netcat -y
```

### Web Application Testing
```bash
# Burp Suite (Community Edition)
sudo apt install burpsuite -y

# Nikto - Web server scanner
sudo apt install nikto -y

# SQLMap - SQL injection tool
sudo apt install sqlmap -y
```

### Exploitation Framework
```bash
# Metasploit Framework
sudo apt install metasploit-framework -y
```

### Network Analysis
```bash
# Wireshark
sudo apt install wireshark -y
```

---

## Tool Purposes

| Tool | Purpose | Use Case |
|------|---------|----------|
| **Nmap** | Network scanning | Port discovery, service identification |
| **Metasploit** | Exploitation framework | Testing vulnerabilities |
| **Burp Suite** | Web proxy | HTTP request interception |
| **Wireshark** | Packet analyzer | Network traffic analysis |
| **Nikto** | Web scanner | Server vulnerability detection |
| **SQLMap** | SQL injection | Database exploitation testing |

---

## Basic Commands Used

### Nmap Scanning
```bash
# Basic scan
nmap <target-ip>

# Detailed scan with version detection
nmap -sV -O <target-ip>

# Scan all ports
nmap -p- <target-ip>
```

### Metasploit
```bash
# Start Metasploit
msfconsole

# Search for exploits
search <vulnerability-name>
```

### Burp Suite
```bash
# Launch Burp Suite
burpsuite
```

---

## Network Configuration

### Check IP Address
```bash
ip addr show
```

### Test Connectivity
```bash
ping <target-ip>
```

---

## Security Notes

⚠️ **Important:**
- Only use these tools in controlled lab environments
- Never test on systems without authorization
- Keep tools updated regularly
- Document all testing activities

---

## Learning Resources

- [Kali Linux Documentation](https://www.kali.org/docs/)
- [Nmap Reference Guide](https://nmap.org/book/)
- [Metasploit Unleashed](https://www.offensive-security.com/metasploit-unleashed/)
- [Burp Suite Documentation](https://portswigger.net/burp/documentation)

---

## Next Steps

✅ Kali Linux is configured and ready
✅ Essential tools are installed
✅ Ready to perform security testing

➡️ Proceed to [Ubuntu Server Setup](ubuntu-setup.md)
