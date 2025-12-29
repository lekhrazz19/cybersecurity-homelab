# Cybersecurity Homelab - Kali Linux Attacker & Ubuntu Server Target

## Project Overview

This project is a hands-on cybersecurity homelab I built to learn and practice penetration testing, vulnerability assessment, and Linux security fundamentals. The lab simulates real-world attack scenarios in a safe, controlled, and ethical environment.

### Lab Architecture
- Attacker Machine: Kali Linux (via WSL)
- Target Machine: Ubuntu Server
- Environment: Isolated local network

---

## Objective

I created this lab to achieve several goals:
- Gain practical experience in ethical hacking
- Understand network reconnaissance and vulnerability scanning techniques
- Practice web application security testing
- Develop skills in Linux system administration
- Learn how to document cybersecurity findings professionally

---

## Tools Used

### Kali Linux Tools:
| Tool | Purpose |
|------|--------|
| Nmap | Network scanning and port discovery |
| Metasploit | Exploitation framework for testing |
| Burp Suite | Web application security testing |
| Wireshark | Network traffic analysis |
| Nikto | Web server vulnerability scanning |

### Target Environment:
- Ubuntu Server - Running Apache, SSH, and vulnerable web applications
- DVWA (Damn Vulnerable Web Application) - For practicing common web exploits

---

## Repository Structure

```
cybersecurity-homelab/
│
├── README.md                    # Main project documentation
├── screenshots/                 # Lab screenshots and visual documentation
├── lab-setup/
│   ├── kali-setup.md           # Kali Linux installation & configuration
│   └── ubuntu-setup.md         # Ubuntu Server setup
├── attacks/
│   ├── nmap-scan.md            # Network reconnaissance documentation
│   ├── dvwa-testing.md         # Web vulnerability testing
│   └── burpsuite-notes.md      # HTTP interception notes
├── learning-outcomes.md         # Skills and knowledge I gained
└── disclaimer.md                # Legal and ethical disclaimer
```

---

## What I Tested

### Network Reconnaissance
- Performed Nmap scans to identify open ports and running services
- Discovered potential entry points and mapped the network topology
- Documented findings to understand the attack surface

### Web Application Security
- Tested DVWA for common vulnerabilities including:
  - SQL Injection attacks
  - Cross-Site Scripting (XSS)
  - Command Injection
  - File Upload vulnerabilities

### Traffic Interception
- Used Burp Suite to intercept and analyze HTTP requests
- Modified requests to test application security controls
- Learned how client-server communication works

---

## Key Learnings

Through this project, I developed several important skills:

Technical Skills:
- Proficiency with Linux command-line tools
- Network scanning and enumeration techniques
- Web application vulnerability testing
- Security tool configuration and usage

Security Concepts:
- Understanding of the CIA Triad (Confidentiality, Integrity, Availability)
- Knowledge of OWASP Top 10 vulnerabilities
- Ethical hacking methodology and approach
- Defense-in-depth security principles

Professional Development:
- Technical documentation and reporting skills
- Lab environment setup and management
- Understanding of various attack vectors
- Security assessment workflows and methodologies

---

## Future Improvements

I plan to expand this homelab in several ways:

- Add more vulnerable machines (Metasploitable, HackTheBox)
- Implement network segmentation for realistic environments
- Test wireless security (if applicable)
- Create automated security scanning scripts
- Document advanced exploitation techniques
- Set up a SIEM (Security Information and Event Management) solution

---

## Disclaimer

This project was created strictly for educational purposes in a controlled lab environment.

- All testing was performed on personally owned equipment
- No unauthorized testing was conducted on any external systems
- This project demonstrates ethical security research practices
- Always obtain proper authorization before testing any system

---

## About This Project

This homelab showcases:
- Practical cybersecurity skills developed through hands-on practice
- A methodical approach to learning security concepts
- Professional documentation of technical work
- Ethical security research principles

Created by: Lekhraj Singh  
Purpose: Educational & Skill Development  
Status: Active Learning Project

---

## Connect

If you're interested in cybersecurity and ethical hacking, feel free to connect with me:

- LinkedIn: [lekhrazz19](https://www.linkedin.com/in/lekhrazz19)
- Email: singhlekhraj497@gmail.com

---

## License

This project is for educational purposes only. Please use the techniques and knowledge shared here responsibly and ethically.

---

Remember: With great power comes great responsibility. Always practice ethical hacking and respect legal boundaries.
