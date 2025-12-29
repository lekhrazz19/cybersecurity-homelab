# Kali Linux Setup (via WSL)

## Overview
Setting up Kali Linux was the first step in building my cybersecurity homelab. I chose to run it on Windows Subsystem for Linux (WSL) because it provides a convenient way to have a Linux environment on my Windows machine without needing dual boot or a separate virtual machine.

---

## Installation Steps

### 1. Enable WSL on Windows
First, I opened PowerShell as administrator and ran:
```powershell
wsl --install
```

This command enabled WSL and set up the necessary components on my Windows system.

### 2. Install Kali Linux from Microsoft Store
The installation process was straightforward:
- Opened the Microsoft Store
- Searched for "Kali Linux"
- Clicked Install
- Launched Kali and created my user account

### 3. Update the System
Once Kali was running, my first task was updating everything:
```bash
sudo apt update && sudo apt upgrade -y
```

I learned it's crucial to keep the system updated to have the latest tools and security patches.

---

## Essential Tools Installation

After the base installation, I installed the security tools I needed for my testing.

### Network Scanning Tools
```bash
# Nmap - My go-to network scanner
sudo apt install nmap -y

# Netcat - Useful network utility
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
# Wireshark - For packet analysis
sudo apt install wireshark -y
```

---

## Tool Purposes

Here's why I chose each tool and what I used them for:

| Tool | Purpose | How I Used It |
|------|---------|---------------|
| Nmap | Network scanning | Discovering open ports and identifying services |
| Metasploit | Exploitation framework | Testing known vulnerabilities |
| Burp Suite | Web proxy | Intercepting and modifying HTTP requests |
| Wireshark | Packet analyzer | Analyzing network traffic patterns |
| Nikto | Web scanner | Finding server vulnerabilities |
| SQLMap | SQL injection | Testing database security |

---

## Basic Commands I Used

### Nmap Scanning
These are the Nmap commands I used most frequently:
```bash
# Basic scan
nmap <target-ip>

# Detailed scan with version detection
nmap -sV -O <target-ip>

# Scan all ports
nmap -p- <target-ip>
```

### Metasploit
Getting started with Metasploit:
```bash
# Start Metasploit console
msfconsole

# Search for exploits
search <vulnerability-name>
```

### Burp Suite
Launching Burp Suite:
```bash
burpsuite
```

---

## Network Configuration

### Checking My IP Address
To find my Kali Linux IP:
```bash
ip addr show
```

### Testing Connectivity
Before starting any tests, I always verified connectivity:
```bash
ping <target-ip>
```

---

## Security Notes

Important lessons I learned about using these tools:

- Only use these tools in controlled lab environments
- Never test on systems without proper authorization
- Keep all tools updated regularly
- Document everything you do
- Understand what each command does before running it

---

## Learning Resources

These resources helped me learn how to use Kali Linux effectively:

- [Kali Linux Documentation](https://www.kali.org/docs/)
- [Nmap Reference Guide](https://nmap.org/book/)
- [Metasploit Unleashed](https://www.offensive-security.com/metasploit-unleashed/)
- [Burp Suite Documentation](https://portswigger.net/burp/documentation)

---

## Next Steps

After completing the Kali Linux setup:
- My attacker machine is configured and ready
- All essential security tools are installed
- I'm ready to start performing security testing

The next step is setting up the Ubuntu Server as my target machine.

---

## Tips and Tricks

### Things I Learned Along the Way:

1. **WSL Integration**: Kali on WSL integrates well with Windows, making file sharing easy
2. **Resource Management**: WSL is lighter than a full VM, which helped with system performance
3. **Tool Updates**: I created a habit of updating tools before each testing session
4. **Documentation**: I kept notes of useful commands and configurations

### Common Issues I Encountered:

- **Network Connectivity**: Sometimes WSL networking can be tricky; restarting WSL usually helped
- **Permission Issues**: Many tools need sudo privileges
- **Tool Conflicts**: Some tools work better when run individually rather than simultaneously

---

## Conclusion

Setting up Kali Linux on WSL gave me a powerful, flexible platform for learning cybersecurity. The installation was straightforward, and having it integrated with my Windows environment made the workflow smooth.

This setup became the foundation for all my penetration testing exercises in the homelab.
