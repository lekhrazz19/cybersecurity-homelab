# 🐧 Ubuntu Server Setup

## Overview
This document outlines the configuration of **Ubuntu Server** as the **target machine** in the cybersecurity homelab environment.

---

## Installation

### System Requirements
- Ubuntu Server 20.04 LTS or later
- Minimum 2GB RAM
- 20GB disk space
- Network connectivity

### Installation Steps
1. Download Ubuntu Server ISO from [official website](https://ubuntu.com/download/server)
2. Create bootable USB or virtual machine
3. Follow installation wizard
4. Configure network settings
5. Create user account

---

## Initial Configuration

### Update System
```bash
sudo apt update && sudo apt upgrade -y
```

### Check IP Address
```bash
ip addr show
# or
ifconfig
```

### Enable SSH (if not already enabled)
```bash
sudo apt install openssh-server -y
sudo systemctl enable ssh
sudo systemctl start ssh
```

---

## Services Installation

### Apache Web Server
```bash
# Install Apache
sudo apt install apache2 -y

# Start and enable Apache
sudo systemctl start apache2
sudo systemctl enable apache2

# Check status
sudo systemctl status apache2
```

### PHP (for vulnerable web applications)
```bash
sudo apt install php libapache2-mod-php php-mysql -y
```

### MySQL Database
```bash
sudo apt install mysql-server -y
sudo mysql_secure_installation
```

---

## DVWA Installation

### Download and Setup DVWA
```bash
# Navigate to web directory
cd /var/www/html

# Clone DVWA repository
sudo git clone https://github.com/digininja/DVWA.git

# Set permissions
sudo chown -R www-data:www-data DVWA
sudo chmod -R 755 DVWA
```

### Configure DVWA
```bash
# Copy configuration file
cd DVWA/config
sudo cp config.inc.php.dist config.inc.php

# Edit configuration (set database credentials)
sudo nano config.inc.php
```

### Setup Database
1. Access DVWA: `http://<server-ip>/DVWA/setup.php`
2. Click "Create / Reset Database"
3. Login with default credentials:
   - Username: `admin`
   - Password: `password`

---

## Network Configuration

### Check Listening Ports
```bash
sudo netstat -tulpn
# or
sudo ss -tulpn
```

### Firewall Configuration (Optional)
```bash
# Check firewall status
sudo ufw status

# Allow Apache
sudo ufw allow 'Apache Full'

# Allow SSH
sudo ufw allow 22/tcp
```

---

## Purpose as Target Machine

### Services Exposed
| Service | Port | Purpose |
|---------|------|--------|
| **SSH** | 22 | Remote access testing |
| **HTTP** | 80 | Web application testing |
| **MySQL** | 3306 | Database security testing |

### Vulnerabilities for Testing
- Web application vulnerabilities (DVWA)
- Service version detection
- Port scanning practice
- Authentication testing

---

## Security Notes

⚠️ **Important:**
- This is a **vulnerable** system by design
- Only use in **isolated** lab environment
- **Never expose** to public internet
- Keep snapshots for easy restoration
- Monitor all testing activities

---

## Testing Scenarios

### Network Scanning
- Target for Nmap reconnaissance
- Service enumeration practice
- Port detection exercises

### Web Application Testing
- SQL injection practice (DVWA)
- XSS vulnerability testing
- File upload exploits
- Authentication bypass attempts

### SSH Testing
- Connection testing
- Brute force prevention (fail2ban)
- Key-based authentication

---

## Maintenance

### Regular Tasks
```bash
# Check running services
sudo systemctl status apache2
sudo systemctl status mysql
sudo systemctl status ssh

# View logs
sudo tail -f /var/log/apache2/access.log
sudo tail -f /var/log/apache2/error.log

# Restart services if needed
sudo systemctl restart apache2
```

### Reset Environment
```bash
# Reset DVWA database
# Access: http://<server-ip>/DVWA/setup.php
# Click "Create / Reset Database"

# Restore from snapshot (if using VM)
```

---

## Verification Checklist

✅ Ubuntu Server installed and updated
✅ Apache web server running
✅ SSH service enabled
✅ DVWA installed and accessible
✅ Network connectivity verified
✅ IP address documented
✅ Services responding to requests

---

## Next Steps

➡️ Server is ready for security testing
➡️ Proceed to [Nmap Scanning](../attacks/nmap-scan.md)

---

## Useful Commands Reference

```bash
# Check Ubuntu version
lsb_release -a

# Check system resources
free -h
df -h

# View network connections
sudo netstat -tuln

# Check Apache configuration
apachectl -t

# View installed packages
dpkg -l | grep apache
```
