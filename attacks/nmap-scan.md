# Nmap Network Scanning

## Objective
My goal with this phase was to perform network reconnaissance on the Ubuntu Server target machine. I wanted to identify open ports, discover running services, and understand potential vulnerabilities that might exist.

---

## What is Nmap?
Nmap (Network Mapper) is a powerful open-source tool that I used for several purposes:
- Network discovery and mapping
- Port scanning to find open services
- Service version detection
- Operating system fingerprinting
- Basic vulnerability assessment

---

## Scanning Commands I Used

### 1. Basic Scan
```bash
nmap <target-ip>
```
This quick scan checks the most common 1000 ports to get a fast overview of the target.

### 2. Full Port Scan
```bash
nmap -p- <target-ip>
```
I ran this to scan all 65535 ports thoroughly, ensuring I didn't miss anything.

### 3. Service Version Detection
```bash
nmap -sV <target-ip>
```
This helped me identify exactly which versions of services were running on open ports.

### 4. Operating System Detection
```bash
sudo nmap -O <target-ip>
```
Using this command, I could detect what operating system the target was running.

### 5. Aggressive Scan
```bash
sudo nmap -A <target-ip>
```
This comprehensive scan combines OS detection, version detection, script scanning, and traceroute.

### 6. Specific Port Scan
```bash
nmap -p 22,80,443 <target-ip>
```
When I wanted to focus on specific ports, I used this targeted approach.

---

## What I Discovered

### Open Ports Identified
| Port | Service | Version | Purpose |
|------|---------|---------|--------|
| 22 | SSH | OpenSSH 8.x | Remote access |
| 80 | HTTP | Apache 2.4.x | Web server |
| 3306 | MySQL | 8.0.x | Database server |

### Service Details
Here's what I found running:
- SSH: Secure Shell for remote administration
- Apache: Web server hosting DVWA
- MySQL: Database backend supporting the web applications

---

## What I Learned

Through this scanning exercise, I developed several important skills:

Technical Skills:
- How to properly conduct network scanning
- Port identification and analysis techniques
- Service enumeration methods
- Interpreting and understanding Nmap output

Security Insights:
- How to identify an attack surface
- Recognizing potential entry points
- Understanding the risks of service exposure
- Planning next steps in penetration testing

---

## Security Implications

Findings:
- Each open port represents a potential attack vector
- Service versions might have known vulnerabilities
- Running unnecessary services increases risk
- Proper port management is crucial for security

Recommendations:
- Close unused ports
- Keep all services updated
- Implement firewall rules
- Regularly monitor access logs

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

After completing this reconnaissance:
- Network mapping is complete
- Attack surface has been identified
- Services have been enumerated
- Ready to proceed with vulnerability testing

Next, I'll move on to testing the DVWA web application.

---

## Ethical Considerations

Important reminders:
- I only scanned systems that I own and have permission to test
- Unauthorized scanning is illegal and unethical
- All scanning activities were documented
- This work was performed in a controlled lab environment

---

## Additional Resources

Resources I found helpful:
- [Nmap Official Documentation](https://nmap.org/docs.html)
- [Nmap Port Scanning Basics](https://nmap.org/book/man-port-scanning-basics.html)
- [Common Nmap Commands Cheat Sheet](https://www.stationx.net/nmap-cheat-sheet/)
