
## Conexiones Remotas
Habilitar conexion
```
lxc config set core.https_address "[::]:8443"
```
Establecer clave
```
lxc config set core.trust_password password
```
Añadir en el cliente el repositorio
```
lxc remote add mirepo-remoto 192.168.1.1
lxc remote add mirepo-remoto images.mirepor-remoto.com
```
Listado de repositorios
```
lxc remote list
```
Listado de imagenes
```
lxc image list mirepo-remoto:
```
Crear un contendore desde el repositorio
```
lxc launch mirepo-remoto:centos-7 dnsserver
```
Listado de contenedores remoto
```
lxc list mirepo-remoto:
```
Creacion de contendor remoto
```
lxc launch mirepo-remoto:centos-7 mirepo-remoto:printserver
```
Detener un contenedor
```
lxc stop mirepo-remoto:printserver
```