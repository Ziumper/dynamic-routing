# OSPF

Show configuration ospf
```bash
show ip protocols

show ip ospf
```

Turn on/off ospf, go to specific configuration mode of instance 
```bash
#turn on
router ospf <instance number>

#turn off
no  router ospf <instance number>
```

Adding network
```bash
network <ip address of network> <mask with reversed > area <area address>

#example for network 204.12.0.0/24 in area 1.1.1.1
network 204.12.0.0 0.0.0.255 area 1.1.1.1
```

Add router id
```bash
router-id <number>
```

Show ospf router instances information
```bash
show ip ospf
```
Show ospf database
```bash
show ip ospf database
```

List of interfaces where ospf is on
```bash
show ip ospf interface [brief]
```

Show neighbors
```bash
show ip ospf neighbor
```

