# Rip commands

Show rip database
```bash
show ip rip database
```

Routing tables
```bash
show ip route
```

Turn on/off RIP on router, go on into RIP configuration mode (config-router)#
```bash
#turn on
router rip

#turn off
no router rip
```

Change rip version
```bash
version <version>
```

Disable auto aggregation
```bash
no auto-summary
```

Set rip timers in seconds
```bash
timers basic <update> <invalid> <holddown> <flush> 
```

Adding removing networks
```bash
#turn on
network <addressIP>

#turn off
no network <addressIP>
```

Passive interface, no sending rip communication trough , but still can read rip communication
```bash
#turn on
passive-interface <interface>

#turn off
passive-interface <interface>
```

Default metric for redistribute 
```bash
default-metric <value>
```

