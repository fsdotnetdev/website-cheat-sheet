# Iptables
Description
```bash

```

# Table of Content
* Block IP

## Block IP
* Create IP Blacklist
```bash
# vi /home/[user]/script/banlist.txt
```

* Show Rule
```bash
# iptables -S
-P INPUT ACCEPT
-P FORWARD ACCEPT
-P OUTPUT ACCEPT
-N f2b-sshd
-A INPUT -p tcp -m multiport --dports 22 -j f2b-sshd
-A INPUT -s 216.244.66.198/32 -j DROP
-A INPUT -s 216.244.66.239/32 -j DROP
-A INPUT -s 216.244.66.205/32 -j DROP
-A INPUT -s 163.172.71.0/24 -j DROP
-A INPUT -s 104.131.147.112/32 -j DROP
-A INPUT -s 54.36.148.0/24 -j DROP
-A INPUT -s 54.36.149.0/24 -j DROP
-A INPUT -s 46.229.168.0/24 -j DROP
-A f2b-sshd -j RETURN
```

* Show Specific Rule
```bash
# iptables -S INPUT
```

* Check Iptables Rule Before
```bash
# iptables -L -v -n 
```

* Check Configure
```bash
# iptables-save
```

* Set Variable from Blacklist
```bash
# ban=$(more banlist.txt) 
```

* Check Loop before Execute
```bash
# for i in $ban; do echo iptables -A INPUT -s $i -j DROP ; done
```

* Execute Script
```bash
# for i in $ban; do iptables -A INPUT -s $i -j DROP ; done
```

* Check Iptables Rule After
```bash
# iptables -L -v -n 
```

* Check Website Log
```bash
# cd /var/www/[website]/log
# iptables -L -v -n
```

* Drop Rules
```bash
# iptables -D INPUT -s 1.2.3.4 -j DROP
```

* Source & Destination
```bash
# iptables -A INPUT -i eth0 192.168.1.100 -d 222.222.222.222 -p tcp -dport 80 -j ACCEPT
```

* Example
```bash
IP วง 216.244.66.XX
ฺฺลอง Block แค่ 3 IP ดูก่อน คือ
198 , 239 และ  250
 
IP วง 104.131.147
Block เฉพาะ IP 104.131.147.112
 
ที่เหลือ block ทั้งวง
```

## Credit
https://www.digitalocean.com/community/tutorials/how-to-list-and-delete-iptables-firewall-rules