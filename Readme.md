#Linux Hardening Lab

This project demonstrates how to secure a Linux server by applying enterprise-grade security controls.

##Objective
Transform a default Ubuntu server into a hardened secure system resistant to common cyber attacks.

##Security Layers Implemented

| Layer | Description |
|------|-----------|
| Identity Security | Non-root user, sudo controls |
| SSH Hardening | Key-based auth, root blocked, custom port |
| Firewall | UFW with default deny |
| Intrusion Prevention | Fail2Ban |
| Log Monitoring | Real-time auth log analysis |
| Attack Simulation | Port scanning & brute force tests |

##Tools Used
- Ubuntu Server 22.04
- OpenSSH
- UFW Firewall
- Fail2Ban
- Nmap
##What i learn
difference between apt upgrade and apt dist-upgrade we prefer to use apt dist-upgrade so we delete ,install or replace files  .
apt install unattended-upgrades for Automatic upgrades very usefull for Devops / cybersecurity 
## 📸 Screenshots


fail2ban-client status
ss -tulpn
