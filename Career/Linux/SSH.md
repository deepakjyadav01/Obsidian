
# SSH 

- Learnt about how to operate an ssh command

```
ssh username@device_ip
```

1) I had given a scenario where I needed to ssh into webserver and postgres server and install the certain packages.
2) User name of bob with password was given.

```
ssh bob@devapp01
ssh bob@devdb01 
```
3) You will be prompted with password and you are into that device.


# IPTABLES

- It is a packet level filtering firewall built into linux kernel.
- iptables is a rule engine that evaluates every network packet and decides whether to ACCEPT, DROP, or REJECT it.

## Rules to write them

```
iptables <OPERATION> <CHAIN> \
  -p <protocol> \
  -s <source_ip> \
  -d <destination_ip> \
  --sport <source_port> \
  --dport <destination_port> \
  -j <ACTION>
```

1) The chains are INPUT, OUTPUT & FORWARD
2) Operations available are A - append, I for insert -D delete and -L list.Use:
	usage:
- `-I` when rules must come before DROPs
- `-A` when order doesn’t matter or policy is DROP

1) protocol's available are ssh/http/https -tcp,  DNS- tcp/udp & ping - ICMP
2) Actions available are ACCEPT , DROP and REJECT.

one example of INPUT accepting all the https on port 443 

```
iptables -I/-A INPUT -p tcp --dport 443 ESTABLISHED,RELATED -j ACCEPT
```

other example of dropping all the incoming packets 

```
iptables -A INPUT  -j DROP
```



