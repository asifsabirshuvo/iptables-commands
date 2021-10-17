Self practicing cheat-sheet for iptables, ufw 
in iptables  
# iptables-commands (NOT TESTED ENOUGH). Please use UFW or AWS SG


list all the rules of iptables
```console
iptables -L -n -v
```

list a specific type
```console
iptables -t nat -L -n -v
```
drop an outgoing domain/ip
```console
iptables -I INPUT -s www.agoda.com -j DROP
```

allow/cancel rule of an outgoing domain/ip
```console
iptables -D INPUT -s www.agoda.com -j DROP
```

cancel all outgoing domain/ip .
```console
iptables -I INPUT -j DROP
```

now allow all outgoing domain/ip .
```console
iptables -D INPUT -j DROP
```

allow/deny particular ip for incoming/outgoing
```console
iptables -A INPUT -s 192.168.1.1 -j ACCEPT
```
```console
iptables -A OUTPUT -d 192.168.1.1 -j ACCEPT
```
```console
iptables -P INPUT DROP
```
```console
iptables -P OUTPUT DROP
```
