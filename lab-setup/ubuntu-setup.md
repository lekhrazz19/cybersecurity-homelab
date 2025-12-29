# Ubuntu Server Setup

## Overview

For the target machine in my cybersecurity homelab, I chose Ubuntu Server. It's a common choice for servers and represents the kind of system you would find in many real-world environments. Running it as the target gave me a safe system to practice penetration testing techniques without breaking anything important.

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

Once Ubuntu Server was installed, I started with some basic configuration steps to prepare it for testing.

### Update System

The first thing I did was update all packages to make sure the system was current:

```bash
sudo apt update && sudo apt upgrade -y
```

### Check IP Address

I needed to know the IP address so I could connect from Kali. I used:

```bash
ip addr show
# or
ifconfig
```

### Enable SSH (if not already enabled)

SSH lets me access the server remotely, which is essential for many attacks:

```bash
sudo apt install openssh-server -y
sudo systemctl enable ssh
sudo systemctl start ssh
```

---

## Services Installation

To make the lab more realistic, I installed several services that are commonly found on real servers. This gave me various targets to practice different attack techniques.

### Apache Web Server

```bash
# Install Apache
sudo apt install apache2 -y

# Start and enable Apache
sudo systemctl start apache2
sudo systemctl enable apache2

# Verify it's running
sudo systemctl status apache2
```

### MySQL Database

```bash
# Install MySQL
sudo apt install mysql-server -y

# Run security script
sudo mysql_secure_installation
```

### FTP Server (vsftpd)

```bash
# Install vsftpd
sudo apt install vsftpd -y

# Configure and start
sudo systemctl enable vsftpd
sudo systemctl start vsftpd
```

---

## Security Configurations

### Firewall Setup

I configured the firewall to allow the services I wanted to test:

```bash
# Enable UFW firewall
sudo ufw enable

# Allow SSH (important - don't lock yourself out)
sudo ufw allow ssh

# Allow HTTP and HTTPS
sudo ufw allow http
sudo ufw allow https

# Allow FTP
sudo ufw allow ftp

# Check status
sudo ufw status
```

### Creating Test Users

I created some test user accounts with weak passwords on purpose, so I could practice password cracking:

```bash
sudo adduser testuser1
sudo adduser testuser2
```

---

## Network Configuration

### Static IP (Optional)

To keep things consistent, I set a static IP address. This meant I wouldn't have to check the IP every time I wanted to connect from Kali.

Edit the network configuration file:

```bash
sudo nano /etc/netplan/00-installer-config.yaml
```

Example configuration:

```yaml
network:
  version: 2
  ethernets:
    eth0:
      addresses:
        - 192.168.1.100/24
      gateway4: 192.168.1.1
      nameservers:
        addresses: [8.8.8.8, 8.8.4.4]
```

Apply the changes:

```bash
sudo netplan apply
```

---

## Verification

After everything was set up, I verified that all services were running:

```bash
# Check running services
sudo systemctl list-units --type=service --state=running

# Check open ports
sudo netstat -tulpn
```

---

## What I Learned

Setting up Ubuntu Server taught me several important things:

1. **Service Management**: I learned how to install, configure, and manage services using systemctl
2. **Firewall Configuration**: Understanding UFW helped me see how firewalls protect systems
3. **Network Basics**: Setting up static IPs and understanding network configuration was valuable
4. **Linux Administration**: Managing users, permissions, and system updates gave me practical Linux experience

---

With the Ubuntu Server configured, I had a realistic target environment ready for penetration testing. The next step was setting up the Ubuntu Server as my target machine.
