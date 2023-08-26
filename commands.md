# Cisco commands

## set password for privileged mode
```
! weak encription
(config)#enable password {new_password}
```

```
! strong encription
(config)#enable secret {new_password}
```

## set password for console line
```
(config)#line console 0
(config-line)#password {new_password}
(config-line)#login
(config-line)#exit
```

## config ip for configuration interface (vlan 1)
```
! configure the ip for vlan1
(config)#interface vlan 1
(config-if)#ip address {ip} {mask}
(config-if)#no shutdown
```

## config virtual terminal as a telnet server
```
! ip address for vlan 1 should be configured
(config)#line vty 0 15
(config-line)#password {new_password}
(config-line)#login
(config-line)#transport input telnet
(config-line)#exit
```

## set hostname
```
(config)#hostname {new_hostname}
```

## show content of nvram
```
#dir nvram:
```

## show current configuration in the memory/
```
#show running-config
```

## show startup configuration
```
#show startup-config
```

## save configuration to nvram
```
#write
```
or
```
#write memory
```
or
```
#copy running-config startup-config
```

## set default configuration
```
#erase startup-config
```

## encrypt all non-encrypted passwords
```
(config)#service password-encryption
```