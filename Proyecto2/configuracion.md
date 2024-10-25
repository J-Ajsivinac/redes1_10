``` bash
hostname ESW1
no ip domain-lookup


enable
configure terminal
vlan 15
 name Recursos_Humanos
vlan 25
 name Contabilidad
vlan 35
 name Ventas
vlan 45
 name Informatica
exit

ROUTER JUTIAPA
```bash

enable
configure terminal

# Configuración de la interfaz Fa5/0 conectada a J1
interface FastEthernet5/0
ip address 11.0.0.1 255.255.255.0
no shutdown
exit

# Configuración de la interfaz Fa6/0 conectada a J2
interface FastEthernet6/0
ip address 11.0.1.1 255.255.255.0
no shutdown
exit

# Rutas estáticas para dirigir el tráfico a la red interna a través de J1 y J2
ip route 192.168.10.0 255.255.255.0 11.0.0.2
ip route 192.168.10.0 255.255.255.0 11.0.1.2
```

J1
```bash
enable
configure terminal

# Configuración de la interfaz Fa0/0 conectada al Router Jutiapa
interface FastEthernet0/0
ip address 11.0.0.2 255.255.255.0
no shutdown
exit

# Configuración de la interfaz Fa1/0 conectada al ESW1 y configuración de HSRP
interface FastEthernet1/0
ip address 192.168.10.2 255.255.255.0
standby 1 ip 192.168.10.1
standby 1 priority 110
standby 1 preempt
no shutdown
exit

```
J2
```bash
enable
configure terminal

# Configuración de la interfaz Fa0/0 conectada al Router Jutiapa
interface FastEthernet0/0
ip address 11.0.1.2 255.255.255.0
no shutdown
exit

# Configuración de la interfaz Fa1/0 conectada al ESW1 y configuración de HSRP
interface FastEthernet1/0
ip address 192.168.10.3 255.255.255.0
standby 1 ip 192.168.10.1
standby 1 priority 100
standby 1 preempt
no shutdown
exit


```

SW2
```BASH
enable
conf t 
interface range fa0/10-11
channel-protocol pagp
channel-group 1 mode desirable
do wr
show etherchannel summary

interface FastEthernet0/12
switchport mode trunk
switchport trunk allowed vlan all
no shutdown
exit


```

SW3
```bash

enable
conf t 
interface range fa0/10-11
channel-protocol pagp
channel-group 1 mode auto
do wr




```

ESW1
```bash
enable
configure terminal

interface FastEthernet0/1
switchport mode trunk
switchport trunk encapsulation dot1q
switchport trunk allowed vlan all
no shutdown
exit

interface FastEthernet0/3
switchport mode trunk
switchport trunk encapsulation dot1q
switchport trunk allowed vlan all
no shutdown
exit

```