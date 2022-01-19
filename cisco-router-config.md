# Router commands


privileged mode
```bash
enable
```

router configuration mode
```bash
configure

#answer for configuration mode
terminal


#config mode enabled as terminal
ROUTER(config)#
```

Move to configure interface config sub mode
```bash
interface FastEthernet0/0

#effect that should be displayed
ROUTER(config-if)#
```

Move back from sub menu
```bash
# or just hit CTRL+Z
exit
```

Help 
```bash
#command name or just type '?'
?

# use tab to hit
#interface <TAB>
#to use command click ENTER afterwards
```
Show network interface configuration
```bash
show ip interface [<interface>] [brief]

#example
show ip interface GigabitEthernet0/0 brief 
```

Change ip address inside interface configuration
```bash
ip address <adressIP> <mask>

#example
ip address 10.10.1.155 255.255.0.
```

Delete ip address
```bash
no ip address
```

Shutdown interface / Turn on
```bash
#off
shutdown
#Turn on
no shutdown
```

Enable / Disable routing 
```bash
#use to reset wrong configuration settings without losing mechanic data

#turn off
no ip routing

#turn on
ip routing
```

Display routing while inside privileged mode #
```bash
show ip route [connected | static] 
```

Adding and removing static routing
(configuration mode)
```bash
# adding
# remote distribution
 ip route <address> <mask> <next-hop>

# remote local
ip route <address> <mask> <interface>

#examples
ip route 192.168.1.0 255.255.255.0 10.1.1.1
ip route 10.100.0.0 255.255.0.0 GibabitEthernet0/2

# removing - just use the same as above but with word no before
# example
no ip route 192.168.1.0 255.255.255.0 10.1.1.1
no ip route 10.100.0.0 255.255.0.0 GibabitEthernet0/2
```
Dynamic routing
```bash
# go to configuration router mode
(config-router)# network 

# distributed connected
redistribute connected [subnets] 

# distribute static
redistribute static [subnets]

# redistributte with ospf protocol with number inside
redistribute ospf <instation>

# redistribute rip protocol numbers
redistribute rip [subnets]

#with ospf use subnets keyword
#with rip use default-metric 10
```


Show ip protocols routing information 
```bash
show ip protocols
```
