## Creacion Contenedores
Crear y ejecutar un contenedor
```
lxc launch images:centos/7 webserver
```
Crear sin inicializar un contenedor
```
lxc init images:centos/7 webserver
```
Listado de contenedores
```
lxc list
```
Listado rápido
```
lxc list --fast
```
Informacion de un contenedor
```
lxc info webserver
```
### Operaciones Básicas
Iniciar contenedor
```
lxc start webserver
```
Detener contenedor
```
lxc stop webserver
```
Pausar un contenedor
```
lxc pause webserver
```
Eliminar un contenedor
```
lxc delete webserver
```
Acceso a un contenedor
```
lxc exec webserver bash
```
Renombrar un contenedor
```
lxc move webserver webserver01
```
Clonar un contenedor
```
lxc copy webserver webserver10
```
Ejecución de comandos
```
lxc exec webserver -- /bin/bash
lxc exec webserver -- apt-get update
lxc exec webserver -- ps -ef
```
Extraer archivos del contenedor
```
lxc file pull webserver/etc/hosts .
```
Llevar/mover archivos al contenedor
```
lxc file push webserver/tmp/
```