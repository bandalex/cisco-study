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
(config-line)#end
```

## config virtual terminal as a telnet server
```
! configure the ip for vlan1
(config)#interface vlan 1
(config-if)#ip address {ip} {mask}
```

```
(config)#line vty 0 15
(config-line)#password {new_password}
(config-line)#login
(config-line)#transport input telnet
(config-line)#end
```

## set hostname
```
(config)#hostname {new_hostname}
```
