# Ubuntu Server Lab

## Overview
Deployed Ubuntu Server 22.04 LTS in VirtualBox as the foundation 
of a self-built home lab environment. This project simulates a 
basic enterprise Linux server setup covering web services, remote 
administration, and firewall security.

## Environment
- **OS:** Ubuntu Server 22.04 LTS
- **Hypervisor:** VirtualBox (Windows host, 32GB RAM)
- **Network:** NAT with port forwarding

## Steps Completed

### 1. Installation & Initial Setup
- Downloaded Ubuntu Server 22.04 LTS ISO and created a VM in VirtualBox
- Allocated 2GB RAM, 2 CPUs, 25GB dynamic storage
- Completed server installation with OpenSSH enabled
- Updated all system packages via apt
```bash
sudo apt update && sudo apt upgrade -y
```

### 2. Apache Web Server
- Installed and configured Apache HTTP server
- Configured VirtualBox port forwarding (host 8080 → guest 80)
- Verified web server accessible from host machine browser
```bash
sudo apt install apache2 -y
sudo systemctl status apache2
```

![Apache web server](screenshots/apache.png)

### 3. SSH Remote Access
- Configured VirtualBox port forwarding (host 2222 → guest 22)
- Connected to the server remotely from Windows host via PowerShell
- Verified remote administration without needing the VirtualBox console
```bash
ssh user@127.0.0.1 -p 2222
```

![SSH connection](screenshots/ssh.png)

### 4. UFW Firewall Configuration
- Enabled UFW with default deny incoming policy
- Whitelisted only necessary ports: SSH (22), HTTP (80), HTTPS (443)
- Explicitly blocked Telnet (port 23) — an insecure legacy protocol
- Verified rules with verbose status output
```bash
sudo ufw enable
sudo ufw default deny incoming
sudo ufw default allow outgoing
sudo ufw allow ssh
sudo ufw allow 80/tcp
sudo ufw allow 443/tcp
sudo ufw deny 23/tcp
sudo ufw status verbose
```

![UFW firewall rules](screenshots/ufw.png)

## Skills Demonstrated
- Linux server installation and administration
- Package management with apt
- Web server deployment and configuration
- SSH remote access and port forwarding
- Firewall policy design and implementation
- VirtualBox VM networking

## What I Learned
Configuring UFW reinforced the principle of least privilege from 
my CompTIA Security+ studies — only allowing exactly what is needed 
and explicitly blocking known insecure protocols. Managing the server 
entirely through SSH mirrors how real production servers are 
administered in enterprise environments.

## Next Steps
- User and permission management
- Bash scripting and cron job automation
- System monitoring and log analysis
- Integration with Wazuh SIEM for centralized logging
