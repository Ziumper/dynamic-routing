

# Usefull commands

Show networks and routers
```bash
ip addr print
```

Show interfaces
```bash
interface print 
```

Add netwatch
```bash
tool netwatch add host=192.168.0.1 interval=5s
```

List up the netwatch
```bash
tool netwatch print
```

# Router 1
```bash
#Enable interface for network F
interface set 3 disabled=no

#Network A - should be in default network 
ip addr add address=192.168.0.1/24 interface=ether2 
#Network B
ip addr add address=192.168.1.1/24 interface=ether3 
#Netowrk F
ip addr add address=192.168.10.1/24 interface=ether4
```

# Router 2
```bash
#network B
ip addr add address=192.168.1.2/24 interface=ether2
#netowrk C 
ip addr add address=192.168.2.2/24 interface=ether3
```

# Router 3 
```bash
#netowrk C
ip addr add address=192.168.2.3/24 interface=ether2
#netowrk D
ip addr add address=192.168.3.3/24 interface=ether3
```

# Router 4
```bash
#Enable interface for network F
interface set 3 disabled=no

#network D
ip addr add address=192.168.3.4/24 interface=ether2
#network E should be already set up 
ip addr add address=192.168.4.4/24 interface=ether3
#network F
ip addr add address=192.168.10.4/24 interface=ether4
``` 

# Add watch for all routers networks A, B, C, D, E, F.
```bash
tool netwatch add host=192.168.0.1 interval=5s
tool netwatch add host=192.168.1.1 interval=5s
tool netwatch add host=192.168.1.2 interval=5s
tool netwatch add host=192.168.2.2 interval=5s
tool netwatch add host=192.168.2.3 interval=5s
tool netwatch add host=192.168.3.3 interval=5s
tool netwatch add host=192.168.3.4 interval=5s
tool netwatch add host=192.168.4.4 interval=5s
tool netwatch add host=192.168.10.1 interval=5s
tool netwatch add host=192.168.10.4 interval=5s
tool netwatch add host=192.168.10.5 interval=5s
```