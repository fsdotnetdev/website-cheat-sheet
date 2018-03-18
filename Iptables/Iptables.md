# Iptables
Description
```bash

```

# Table of Content
* Block IP

## Block IP
* Create IP Blacklist
```bash
# vi banlist.txt
```

* Check Iptables Rule Before
```bash
# iptables -L -v -n 
```

* Set Variable
```bash
# ban=$(more banlist.txt) 
```

* Check Loop
```bash
# for i in $ban; do echo iptables -A INPUT -s $i -j DROP ; done
```

* Exec Script
```bash
# for i in $ban; do iptables -A INPUT -s $i -j DROP ; done
```

* Check Iptables Rule After

## License
Webneena license.