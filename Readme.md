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
difference between apt upgrade and apt dist-upgrade we prefer to use apt dist-upgrade so we delete ,install or replace files  .
apt install unattended-upgrades for Automatic upgrades very usefull for Devops / cybersecurity
using publicKey for more security than a normal password with command :ssh-keygen -b 4096
that's creat a public for logs .
I change the port 22  in file /etc/ssh/sshd_config to port 777 so to not let hackers to know which port we are working at . and this modifications
PermitRootLogin no
PasswordAuthentication no
Port 777
next step we use farewall and let only our port to get in 777 .
enable fail2ban used for person who tries multple password to get one right to protect server from "brute force".
using log monitoring too see session's.




## 📸 Screenshots
<img width="1212" height="556" alt="Screenshot 2026-01-04 194347" src="https://github.com/user-attachments/assets/b0ded1ad-38de-4c0d-af2f-7abfa52ac7fb" />


fail2ban-client status
ss -tulpn
can you fix this 
