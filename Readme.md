# Linux Hardening & Intrusion Prevention Lab

An implementation of enterprise-grade security controls on an Ubuntu 22.04 LTS server to mitigate unauthorized access and brute-force attacks.

## Objective
The goal of this lab was to transform a "stock" Linux installation into a hardened environment using the **Defense in Depth** strategy.

## Tech Stack
* **OS:** Ubuntu 22.04 LTS
* **Firewall:** UFW (Uncomplicated Firewall)
* **Security:** Fail2Ban, OpenSSH
* **Analysis:** Nmap, Linux Audit Logs

## Security Implementations

### 1. SSH Hardening & Identity Management
* **Disabled Root Login:** Prevented direct administrative access to reduce attack surface.
* **Key-Based Authentication:** Disabled passwords entirely in favor of **4096-bit RSA keys**.
* **Port Obscurity:** Moved SSH from the default port 22 to **port 777** to avoid automated bot scanning.

### 2. Network Security (UFW)
* Implemented a **Default Deny** policy.
* Only explicitly allowed traffic on the custom SSH port (777).

### 3. Intrusion Prevention (Fail2Ban)
* Configured Fail2Ban to monitor authentication logs.
* Automated the "banning" of IP addresses that show malicious patterns (brute-force attempts).



##  Lessons Learned
* **Package Management:** Learned the importance of `apt dist-upgrade` for handling complex dependency changes and `unattended-upgrades` for critical security patching.
* **Log Analysis:** Gained experience using `tail -f /var/log/auth.log` to monitor system health and detect live intrusion attempts.
* **Service Verification:** Used `ss -tulpn` to audit listening ports and ensure no unauthorized services were exposed.

## 📸 Lab Evidence
| Fail2Ban Status | Active Connections |
|---|---|
| ![Fail2Ban Status](screenshots/fail2ban_status.png) | ![Port Audit](screenshots/ufw_rules.png) |
