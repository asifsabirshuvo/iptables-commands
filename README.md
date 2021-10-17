
# iptables-commands


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
