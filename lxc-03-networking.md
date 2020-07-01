## Networking 
Listar redes
```
lxc network list
```
Crear una nueva red
```
lxc network create testbr0
```
Crear y configurar una red
```
lxc network create testbr0 ipv6.address=none ipv4.address=10.0.3.1/24 ipv4.nat=true
```
Obtener informacion de una red 
```
lxc network info testbr0
```
Propiedades de una red
```
lxc network show testbr0
```
Asociar una red
```
lxc network attach testbr0 webserver eth1
```
Desasociar una red
```
lxc network detach testbr0 webserver
```
Configuracion DHCP
```
lxc network list-leases testbr0
```
Asignar IP estatica
```
lxc config device set webserver eth1 ipv4.address 10.220.251.200
```
Eliminar una red existente
```
lxc network delete testbr0
```