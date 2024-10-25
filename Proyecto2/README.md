## Jutiapa

|VLAN|ID de VLAN|Equipos|
|-|-|-|
|RRHH|15|10|
|Contabilidad|25|4|
|Ventas|35|25|
|Inforatica|45|12|

## Escuintla

|VLAN|ID de VLAN|Equipos|
|-|-|-|
|RRHH|15|5|
|Ventas|35|20|

## Quiche

|VLAN|ID de VLAN|Equipos|
|-|-|-|
|RRHH|15|12|
|Contabilidad|25|10|
|Ventas|35|36|
|Inforatica|45|21|

## Peten

|VLAN|ID de VLAN|Equipos|
|-|-|-|
|RRHH|15|10|
|Ventas|35|30|
|Inforatica|45|15|

## Izabal

|VLAN|ID de VLAN|Equipos|
|-|-|-|
|RRHH|15|10|
|Contabilidad|25|5|
|Ventas|35|25|

## Area de Firewall

|VLAN|ID|
|-|-|
|DB_Server|55|
|Management_Server|65|
|File_Server|75|


# 🛠 Detalle de Comandos

| Comando                          | Descripción                                               |
| -------------------------------- | --------------------------------------------------------- |
| `Switch>`                        | Modo de usuario no privilegiado.                          |
| `en`                             | Entra en el modo privilegiado.                            |
| `conf t`                         | Entra en el modo de configuración global.                 |
| `hostname SW5`                   | Cambia el nombre del switch a "SW5".                      |
| `vlan 15`                        | Crea o accede a la configuración de la VLAN 15.           |
| `name RRHH`                      | Asigna el nombre "RRHH" a la VLAN 15.                     |
| `vtp domain G10`                 | Cambia el dominio VTP al nombre "G10".                    |
| `vtp mode server`                | Configura el switch en modo servidor VTP.                 |
| `int range f0/1-5`               | Configura el rango de interfaces FastEthernet 0/1 a 0/5.  |
| `switchport mode access`         | Configura el puerto como modo acceso.                     |
| `switchport access vlan 15`      | Asigna la VLAN 15 al puerto.                              |
| `int range f0/6-24`              | Configura el rango de interfaces FastEthernet 0/6 a 0/24. |
| `do write`                       | Guarda la configuración.                                  |
| `int f0/10`                      | Configura la interfaz FastEthernet 0/10.                  |
| `switchport mode trunk`          | Configura el puerto en modo trunk.                        |
| `switchport trunk allowed vlan`  | Especifica las VLANs permitidas en un enlace trunk.       |
| `hostname SW4`                   | Cambia el nombre del switch a "SW4".                      |
| `vtp domain Quiche`              | Cambia el dominio VTP a "Quiche".                         |
| `vtp mode client`                | Configura el switch en modo cliente VTP.                  |
| `do sh vlan`                     | Muestra la configuración de las VLANs.                    |
| `int range f0/1-2`               | Configura el rango de interfaces FastEthernet 0/1 a 0/2.  |
| `switchport access vlan 35`      | Asigna la VLAN 35 al puerto.                              |
| `switchport access vlan 45`      | Asigna la VLAN 45 al puerto.                              |
| `switchport trunk encapsulation` | Configura el encapsulamiento de trunk (dot1q).            |
