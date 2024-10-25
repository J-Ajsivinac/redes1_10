
# Resumen de Direcciónes IP y VLAN

## VLANS
La estructura de las vlans proporcionadas es:

| VLAN         | ID de VLAN | Equipos |
| ------------ | ---------- | ------- |
| RRHH         | 1Y         | nn      |
| Contabilidad | 2Y         | mm      |
| Ventas       | 3Y         | xx      |
| Inforatica   | 4Y         | yy      |

> (Y) es el último dígito del número de carnet con mayor denominación
> Carnet con mayor denominación: 20220013**5**

Quedando las vlans de la siguiente manera:

### Jutiapa

| VLAN         | ID de VLAN | Equipos |
| ------------ | ---------- | ------- |
| RRHH         | 15         | 10      |
| Contabilidad | 25         | 4       |
| Ventas       | 35         | 25      |
| Inforatica   | 45         | 12      |

### Escuintla

| VLAN   | ID de VLAN | Equipos |
| ------ | ---------- | ------- |
| RRHH   | 15         | 5       |
| Ventas | 35         | 20      |

### Quiche

| VLAN         | ID de VLAN | Equipos |
| ------------ | ---------- | ------- |
| RRHH         | 15         | 12      |
| Contabilidad | 25         | 10      |
| Ventas       | 35         | 36      |
| Inforatica   | 45         | 21      |

### Peten

| VLAN       | ID de VLAN | Equipos |
| ---------- | ---------- | ------- |
| RRHH       | 15         | 10      |
| Ventas     | 35         | 30      |
| Inforatica | 45         | 15      |

### Izabal

| VLAN         | ID de VLAN | Equipos |
| ------------ | ---------- | ------- |
| RRHH         | 15         | 10      |
| Contabilidad | 25         | 5       |
| Ventas       | 35         | 25      |

### Area de Firewall

| VLAN              | ID  |
| ----------------- | --- |
| DB_Server         | 55  |
| Management_Server | 65  |
| File_Server       | 75  |

## IPS

### Sede Jutiapa
> RED: 192.168.10.0/24

| Subred       | ID de VLAN | Equipos | Nº de Hosts | IP de red         | Máscara         | Primer Host   | Último Host   | Broadcast     |
| ------------ | ---------- | ------- | ----------- | ----------------- | --------------- | ------------- | ------------- | ------------- |
| Ventas       | 35         | 25      | 30          | 192.168.10.0 /27  | 255.255.255.224 | 192.168.10.1  | 192.168.10.30 | 192.168.10.31 |
| Informatica  | 45         | 12      | 14          | 192.168.10.32 /28 | 255.255.255.240 | 192.168.10.33 | 192.168.10.46 | 192.168.10.47 |
| RRHH         | 15         | 10      | 14          | 192.168.10.48 /28 | 255.255.255.240 | 192.168.10.49 | 192.168.10.62 | 192.168.10.63 |
| cONTABILIDAD | 25         | 4       | 6           | 192.168.10.64 /29 | 255.255.255.248 | 192.168.10.65 | 192.168.10.70 | 192.168.10.71 |

### Sede Escuintla
> RED: 192.148.10.0/24

| Subred | ID de VLAN | Equipos | Nº de Hosts | IP de red         | Máscara         | Primer Host   | Último Host   | Broadcast     |
| ------ | ---------- | ------- | ----------- | ----------------- | --------------- | ------------- | ------------- | ------------- |
| Ventas | 35         | 20      | 30          | 192.148.10.0 /27  | 255.255.255.224 | 192.148.10.1  | 192.148.10.30 | 192.148.10.31 |
| RRHH   | 15         | 5       | 6           | 192.148.10.32 /29 | 255.255.255.248 | 192.148.10.33 | 192.148.10.38 | 192.148.10.39 |

### Sede Quiche
> RED: 192.178.10.0/24

| Subred       | ID de VLAN | Equipos | Nº de Hosts | IP de red          | Máscara         | Primer Host    | Último Host    | Broadcast      |
| ------------ | ---------- | ------- | ----------- | ------------------ | --------------- | -------------- | -------------- | -------------- |
| Ventas       | 35         | 36      | 62          | 192.178.10.0 /26   | 255.255.255.192 | 192.178.10.1   | 192.178.10.62  | 192.178.10.63  |
| Informatica  | 45         | 21      | 30          | 192.178.10.64 /27  | 255.255.255.224 | 192.178.10.65  | 192.178.10.94  | 192.178.10.95  |
| RRHH         | 15         | 12      | 14          | 192.178.10.96 /28  | 255.255.255.240 | 192.178.10.97  | 192.178.10.110 | 192.178.10.111 |
| Contabilidad | 25         | 10      | 14          | 192.178.10.112 /28 | 255.255.255.240 | 192.178.10.113 | 192.178.10.126 | 192.178.10.127 |


### Sede Petén
> RED: 192.158.10.0/24

| Subred     | ID de VLAN | Equipos | Nº de Hosts | IP de red         | Máscara         | Primer Host   | Último Host   | Broadcast     |
| ---------- | ---------- | ------- | ----------- | ----------------- | --------------- | ------------- | ------------- | ------------- |
| Ventas     | 35         | 30      | 30          | 192.158.10.0 /27  | 255.255.255.224 | 192.158.10.1  | 192.158.10.30 | 192.158.10.31 |
| Inforatica | 45         | 15      | 30          | 192.158.10.32 /27 | 255.255.255.224 | 192.158.10.33 | 192.158.10.62 | 192.158.10.63 |
| RRHH       | 15         | 10      | 14          | 192.158.10.64 /28 | 255.255.255.240 | 192.158.10.65 | 192.158.10.78 | 192.158.10.79 |

### Sede Izabal
> RED: 192.167.10.0/24

| Subred       | ID de VLAN | Equipos | Nº de Hosts | IP de red         | Máscara         | Primer Host   | Último Host   | Broadcast     |
| ------------ | ---------- | ------- | ----------- | ----------------- | --------------- | ------------- | ------------- | ------------- |
| Ventas       | 35         | 25      | 30          | 192.167.10.0 /27  | 255.255.255.224 | 192.167.10.1  | 192.167.10.30 | 192.167.10.31 |
| RRHH         | 15         | 10      | 14          | 192.167.10.32 /28 | 255.255.255.240 | 192.167.10.33 | 192.167.10.46 | 192.167.10.47 |
| Contabilidad | 25         | 5       | 6           | 192.167.10.48 /29 | 255.255.255.248 | 192.167.10.49 | 192.167.10.54 | 192.167.10.55 |

### Core
> No de Subredes: 6

| Subred   | Nº de Hosts | IP de red      | Máscara         | Primer Host | Último Host | Broadcast  |
| -------- | ----------- | -------------- | --------------- | ----------- | ----------- | ---------- |
| Subred 1 | 30          | 10.0.0.0 /27   | 255.255.255.224 | 10.0.0.1    | 10.0.0.30   | 10.0.0.31  |
| Subred 2 | 30          | 10.0.0.32 /27  | 255.255.255.224 | 10.0.0.33   | 10.0.0.62   | 10.0.0.63  |
| Subred 3 | 30          | 10.0.0.64 /27  | 255.255.255.224 | 10.0.0.65   | 10.0.0.94   | 10.0.0.95  |
| Subred 4 | 30          | 10.0.0.96 /27  | 255.255.255.224 | 10.0.0.97   | 10.0.0.126  | 10.0.0.127 |
| Subred 5 | 30          | 10.0.0.128 /27 | 255.255.255.224 | 10.0.0.129  | 10.0.0.158  | 10.0.0.159 |
| Subred 6 | 30          | 10.0.0.160 /27 | 255.255.255.224 | 10.0.0.161  | 10.0.0.190  | 10.0.0.191 |

# 🛠 Detalle de Comandos

| Comando                                     | Descripción                                                                                            |
| ------------------------------------------- | ------------------------------------------------------------------------------------------------------ |
| `Switch>`                                   | Modo de usuario no privilegiado.                                                                       |
| `en`                                        | Entra en el modo privilegiado.                                                                         |
| `conf t`                                    | Entra en el modo de configuración global.                                                              |
| `hostname SW5`                              | Cambia el nombre del switch a "SW5".                                                                   |
| `vlan 15`                                   | Crea o accede a la configuración de la VLAN 15.                                                        |
| `name RRHH`                                 | Asigna el nombre "RRHH" a la VLAN 15.                                                                  |
| `vtp domain G10`                            | Cambia el dominio VTP al nombre "G10".                                                                 |
| `vtp mode server`                           | Configura el switch en modo servidor VTP.                                                              |
| `int range f0/1-5`                          | Configura el rango de interfaces FastEthernet 0/1 a 0/5.                                               |
| `switchport mode access`                    | Configura el puerto como modo acceso.                                                                  |
| `switchport access vlan 15`                 | Asigna la VLAN 15 al puerto.                                                                           |
| `int range f0/6-24`                         | Configura el rango de interfaces FastEthernet 0/6 a 0/24.                                              |
| `do write`                                  | Guarda la configuración.                                                                               |
| `int f0/10`                                 | Configura la interfaz FastEthernet 0/10.                                                               |
| `switchport mode trunk`                     | Configura el puerto en modo trunk.                                                                     |
| `switchport trunk allowed vlan`             | Especifica las VLANs permitidas en un enlace trunk.                                                    |
| `hostname SW4`                              | Cambia el nombre del switch a "SW4".                                                                   |
| `vtp domain Quiche`                         | Cambia el dominio VTP a "Quiche".                                                                      |
| `vtp mode client`                           | Configura el switch en modo cliente VTP.                                                               |
| `do sh vlan`                                | Muestra la configuración de las VLANs.                                                                 |
| `int range f0/1-2`                          | Configura el rango de interfaces FastEthernet 0/1 a 0/2.                                               |
| `switchport access vlan 35`                 | Asigna la VLAN 35 al puerto.                                                                           |
| `switchport access vlan 45`                 | Asigna la VLAN 45 al puerto.                                                                           |
| `switchport trunk encapsulation`            | Configura el encapsulamiento de trunk (dot1q).                                                         |
| `enable`                                    | Entra en el modo privilegiado del router.                                                              |
| `configure terminal`                        | Accede al modo de configuración global.                                                                |
| `hostname ESCUINTLA`                        | Cambia el nombre del router a "ESCUINTLA".                                                             |
| `interface f5/0`                            | Selecciona la interfaz FastEthernet5/0.                                                                |
| `no shutdown`                               | Activa la interfaz FastEthernet5/0.                                                                    |
| `interface f5/0.15`                         | Crea una subinterfaz 15 en la interfaz FastEthernet5/0.                                                |
| `encapsulation dot1Q 15`                    | Configura la encapsulación 802.1Q con el ID de VLAN 15 en la subinterfaz 15.                           |
| `ip address 192.148.10.33 255.255.255.248`  | Asigna una dirección IP y máscara de subred a la subinterfaz FastEthernet5/0.15.                       |
| `no shutdown`                               | Activa la subinterfaz FastEthernet5/0.15.                                                              |
| `interface f5/0.35`                         | Crea una subinterfaz 35 en la interfaz FastEthernet5/0.                                                |
| `encapsulation dot1Q 35`                    | Configura la encapsulación 802.1Q con el ID de VLAN 35 en la subinterfaz 35.                           |
| `ip address 192.148.10.1 255.255.255.224`   | Asigna una dirección IP y máscara de subred a la subinterfaz FastEthernet5/0.35.                       |
| `no shutdown`                               | Activa la subinterfaz FastEthernet5/0.35.                                                              |
| `configure terminal`                        | Accede al modo de configuración global en el switch.                                                   |
| `interface f0/10`                           | Selecciona la interfaz FastEthernet0/10.                                                               |
| `switchport mode trunk`                     | Configura la interfaz en modo trunk para permitir múltiples VLANs.                                     |
| `switchport trunk allowed vlan 15,25,35,45` | Permite el tráfico de las VLANs 15, 25, 35 y 45 en la interfaz trunk.                                  |
| `exit`                                      | Sale del modo de configuración de la interfaz.                                                         |
| `do write`                                  | Guarda la configuración actual en la memoria del switch.                                               |
| `do show vlan`                              | Muestra la lista de VLANs activas, incluyendo nombres, estados y las interfaces asociadas a cada VLAN. |
| `do show running-config`                    | Muestra la configuración actual en ejecución en el switch.                                             |
| `enable`                                    | Cambia al modo privilegiado.                                                                           |
| `configure terminal`                        | Accede al modo de configuración global en el router.                                                   |
| `interface f5/0.15`                         | Selecciona la subinterfaz FastEthernet5/0.15.                                                          |
| `ip address 192.178.10.97 255.255.255.240`  | Asigna la dirección IP y máscara de subred a la subinterfaz f5/0.15.                                   |
| `do write`                                  | Guarda la configuración actual en la memoria del router.                                               |
| `interface f5/0.25`                         | Selecciona la subinterfaz FastEthernet5/0.25.                                                          |
| `encapsulation dot1Q 25`                    | Configura la encapsulación 802.1Q en la subinterfaz para la VLAN 25.                                   |
| `ip address 192.178.10.113 255.255.255.240` | Asigna la dirección IP y máscara de subred a la subinterfaz f5/0.25.                                   |
| `interface f5/0.35`                         | Selecciona la subinterfaz FastEthernet5/0.35.                                                          |
| `encapsulation dot1Q 35`                    | Configura la encapsulación 802.1Q en la subinterfaz para la VLAN 35.                                   |
| `ip address 192.178.10.1 255.255.255.192`   | Asigna la dirección IP y máscara de subred a la subinterfaz f5/0.35.                                   |
| `interface f5/0.45`                         | Selecciona la subinterfaz FastEthernet5/0.45.                                                          |
| `encapsulation dot1Q 45`                    | Configura la encapsulación 802.1Q en la subinterfaz para la VLAN 45.                                   |
| `ip address 192.178.10.65 255.255.255.224`  | Asigna la dirección IP y máscara de subred a la subinterfaz f5/0.45.                                   |
| `do show ip route`                          | Muestra la tabla de enrutamiento del router, con subredes directamente conectadas.                     |