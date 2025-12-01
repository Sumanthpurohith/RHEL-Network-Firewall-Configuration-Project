RHEL Network & Firewall Configuration Project

This project demonstrates complete network configuration, firewall management, and connectivity troubleshooting on Red Hat Enterprise Linux (RHEL 8/9).
It covers everything from setting up static IP addresses to validating DNS, NTP, and firewall rules.

🔧 Project Tasks Completed
✅ 1. Network Configuration using nmcli

Configured static IPv4 address

Assigned subnet mask & default gateway

Added DNS servers (Google DNS, Cloudflare DNS)

Brought interfaces up/down

Reloaded NetworkManager settings

Example Commands Used

nmcli connection show
nmcli connection modify ens160 ipv4.addresses 192.168.1.50/24
nmcli connection modify ens160 ipv4.gateway 192.168.1.1
nmcli connection modify ens160 ipv4.dns "8.8.8.8 1.1.1.1"
nmcli connection modify ens160 ipv4.method manual
nmcli connection up ens160

🔥 2. Firewall Configuration using firewalld

Added services (HTTP/HTTPS)

Opened specific ports

Assigned interfaces to firewall zones

Reloaded firewall rules

Commands Used

systemctl status firewalld
firewall-cmd --add-service=http --permanent
firewall-cmd --add-port=8080/tcp --permanent
firewall-cmd --reload
firewall-cmd --list-all

🕒 3. NTP Time Sync using chronyd

Configured and verified Chrony NTP synchronization.

Commands Used

systemctl enable chronyd --now
chronyc sources
chronyc tracking

🌐 4. Connectivity Testing

Validated end-to-end network functionality.

Tools Used

ping google.com
curl -I http://google.com
nslookup google.com
traceroute google.com

🧪 Troubleshooting Performed

DNS failures → fixed via /etc/resolv.conf and nmcli

No internet → corrected gateway & routing issues

Time drift → corrected using Chrony NTP

Firewalld blocking traffic → created permanent rules

🧠 Skills Demonstrated

✔ RHEL 8/9
✔ NetworkManager (nmcli)
✔ NIC configuration
✔ Routing, DNS, Gateway setup
✔ firewalld
✔ chrony for time sync
✔ Linux troubleshooting
✔ Networking basics (ICMP, DNS, HTTP, ports)

📸 Sample Output (Screenshots Recommended)

You can add your screenshots (optional):

ip a

nmcli c show

chronyc sources

firewall-cmd --list-all

📁 Repository Purpose

This repository showcases Linux administration skills for:

Interviews

DevOps learning

SysAdmin practice

LinkedIn portfolio
