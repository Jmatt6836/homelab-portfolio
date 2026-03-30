# Home Lab Portfolio

A self-built virtualized IT lab environment documenting hands-on skills in Linux administration, networking, and security.

## Environment
- **Host OS:** Windows, 32GB RAM
- **Hypervisor:** VirtualBox
- **Certifications:** CompTIA Security+, AWS Cloud Practitioner
- **Location:** Las Vegas, NV — open to relocation to Phoenix, AZ or Austin, TX

## Projects

### Ubuntu Server 22.04 ✅
- Installed and configured Ubuntu Server 22.04 LTS in VirtualBox
- Deployed Apache web server, verified via port forwarding
- Configured SSH remote access from Windows host via PowerShell
- Configured UFW firewall with default deny policy, whitelisted SSH/HTTP/HTTPS, explicitly blocked Telnet (port 23)
- Created users, groups, and file permissions simulating RBAC
- Automated backups with bash scripting and cron scheduling
- Performed system monitoring and log analysis via journalctl

[View full writeup →](ubuntu-server/README.md)

### Windows Server 2022 & Active Directory ✅
- Deployed Windows Server 2022 and promoted to Domain Controller
- Created lab.local domain with HR, IT, and Management OUs
- Created domain users and IT-Staff security group
- Configured Group Policy with password policy and login banner
- Configured DNS and DHCP with full scope and options
- Joined Ubuntu Server to the Windows domain via Kerberos/SSSD
- Verified cross-platform AD authentication from Linux

[View full writeup →](windows-server/README.md)

## In Progress
- **pfSense Firewall** — VLAN segmentation, firewall rules, network monitoring
- **AWS Cloud Infrastructure** — EC2, VPC, IAM, CloudWatch (free tier)
- **Wazuh SIEM** — centralized log collection across all VMs

## About
IT graduate (B.S. Computer Information Technology, BYU-Idaho) with CompTIA Security+ and AWS Cloud Practitioner certifications. Building this lab to develop hands-on skills across system administration, networking, and security. Bilingual English/Spanish — open to entry-level roles in IT support, cybersecurity, networking, or cloud operations.

📧 Joshskouson@gmail.com
🔗 [LinkedIn]((https://www.linkedin.com/in/joshskouson/))
