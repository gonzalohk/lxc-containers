## Manejo de Recursos
CPU
Verificar el uso de CPUs
```
lxc exec webserver -- cat /proc/cpuinfo | grep ^proces
```
Hacer uso de 2 cores de CPU
```
lxc config set webserver limits.cpu 2
```
Hacer uso de los cores 1 y 4
```
lxc config set webserver limits.cpu 1,4
```
RAM
Limites de memoria
```
lxc config set webserver limits.memory 256MB
```
Deshabilitar el swap del contenedor
```
lxc config set webserver limits.memory.swap false
```
DISCO
Verificar el espacio de un contenedor
```
lxc exec webserver -- df -h
```
Limitar espacio
```
lxc config device set webserver root size 5GB
```
Limites de escritura y lectura
```
lxc config device set webserver root limits.read 30MB
lxc config device set webserver root limits.write 10MB
```
RED
Limites por medio del profile
```
lxc profile device set default eth0 limits.ingress 100Mbit
lxc profile device set default eth0 limits.egress 100Mbit
```
## Profiles
Listado de profiles
```
lxc profile list
```
Propiedades de un profile
```
lxc profile show default
```
Crear un profile
```
lxc profile create perfil01
```
Personalizar un profile
```
lxc profile set perfil01 limits.cpu 1
```
Asociar un profile
```
lxc profile assign webserver perfil01
```
Desasociar
```
lxc profile remove webserver default
```
Asociar varios profiles
```
lxc init centos/7 webserver03 --profile default --profile perfil01
```
Crear y ejecutar un contenedor con cierto profile
```
lxc launch images:centos/7 webserver04 --profile perfil01
```
Asociar una red
```
lxc network attach-profile testbr0 perfil01 eth1
```
Desasociar
```
lxc network detach-profile testbr0 perfil01
```
Asociar un storage
```
lxc storage volume attach-profile lxd vol10 perfil01 data /opt/data
```
Desasociar
```
lxc storage volume detach-profile lxd vol10 perfil01
```



