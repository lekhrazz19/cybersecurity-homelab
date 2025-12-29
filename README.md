# 🛡️ Cybersecurity Homelab – Kali Linux Attacker & Ubuntu Server Target

## 📌 Project Overview

This project demonstrates a **hands-on cybersecurity homelab** created for learning **penetration testing**, **vulnerability assessment**, and **Linux security**. The lab simulates real-world attack scenarios in a safe, controlled, and ethical environment.

### 🎯 Lab Architecture
- **Attacker Machine**: Kali Linux (via WSL)
- **Target Machine**: Ubuntu Server
- **Environment**: Isolated local network

---

## 🚀 Objective

The primary goal of this project is to:
- Gain practical experience in **ethical hacking**
- Understand **network reconnaissance** and **vulnerability scanning**
- Practice **web application security testing**
- Develop skills in **Linux system administration**
- Learn to **document cybersecurity findings** professionally

---

## 🛠️ Tools Used

### Kali Linux Tools:
| Tool | Purpose |
|------|--------|
| **Nmap** | Network scanning and port discovery |
| **Metasploit** | Exploitation framework |
| **Burp Suite** | Web application security testing |
| **Wireshark** | Network traffic analysis |
| **Nikto** | Web server vulnerability scanner |

### Target Environment:
- **Ubuntu Server** – Running Apache, SSH, and vulnerable web apps
- **DVWA (Damn Vulnerable Web Application)** – For practicing web exploits

---

## 📂 Repository Structure

```
cybersecurity-homelab/
│
├── README.md                    # Main project documentation
├── screenshots/                 # Lab screenshots
├── lab-setup/
│   ├── kali-setup.md           # Kali Linux installation & configuration
│   └── ubuntu-setup.md         # Ubuntu Server setup
├── attacks/
│   ├── nmap-scan.md            # Network reconnaissance documentation
│   ├── dvwa-testing.md         # Web vulnerability testing
│   └── burpsuite-notes.md      # HTTP interception notes
├── learning-outcomes.md         # Skills and knowledge gained
└── disclaimer.md                # Legal and ethical disclaimer
```

---

## 🔬 What Was Tested

### 1. **Network Reconnaissance**
- Performed **Nmap scans** to identify open ports and services
- Discovered running services and potential entry points
- Documented findings for security assessment

### 2. **Web Application Security**
- Tested **DVWA** for common vulnerabilities:
  - SQL Injection
  - Cross-Site Scripting (XSS)
  - Command Injection
  - File Upload vulnerabilities

### 3. **Traffic Interception**
- Used **Burp Suite** to intercept and analyze HTTP requests
- Modified requests to test application security
- Understood client-server communication

---

## 📚 Key Learnings

✅ **Technical Skills:**
- Linux command-line proficiency
- Network scanning and enumeration
- Web application vulnerability testing
- Security tool utilization

✅ **Security Concepts:**
- CIA Triad (Confidentiality, Integrity, Availability)
- OWASP Top 10 vulnerabilities
- Ethical hacking methodology
- Defense in depth

✅ **Professional Development:**
- Documentation and reporting skills
- Lab environment setup and management
- Understanding of attack vectors
- Security assessment workflows

---

## 🔮 Future Improvements

- [ ] Add more vulnerable machines (Metasploitable, HackTheBox)
- [ ] Implement network segmentation
- [ ] Test wireless security (if applicable)
- [ ] Create automated security scanning scripts
- [ ] Document advanced exploitation techniques
- [ ] Set up a SIEM (Security Information and Event Management) solution

---

## ⚠️ Disclaimer

**This project was created strictly for educational purposes in a controlled lab environment.**

- No unauthorized testing was performed
- All activities were conducted on personally owned machines
- This project demonstrates ethical security research
- Always obtain proper authorization before testing any system

---

## 👨‍💻 About the Project

This homelab project showcases:
- Practical cybersecurity skills
- Hands-on learning approach
- Professional documentation
- Ethical security research

**Created by:** Lekhraj Singh  
**Purpose:** Educational & Skill Development  
**Status:** Active Learning Project

---

## 📞 Connect

Interested in cybersecurity and ethical hacking? Let's connect!

- **LinkedIn**: [lekhrazz19](https://www.linkedin.com/in/lekhrazz19)
- **Email**: singhlekhraj497@gmail.com

---

## 📄 License

This project is for educational purposes only. Please use responsibly and ethically.

---

*🔐 Remember: With great power comes great responsibility. Always practice ethical hacking.*
