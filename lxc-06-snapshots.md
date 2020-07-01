Snapshot
Listar snapshots
lxc snapshot list

Creacion de un snapshot
lxc snapshot webserver
lxc snapshot webserver snap-20180827

Restaurar
lxc restore webserver snap-20180827

Renombrar
lxc move webserver/snap-20180827 webserver/snap-01

Eliminar
lxc delete websever/snap-20180827

Crear un contendor desde un snapshot
lxc copy webserver/snap-20180827 webserver100




Habilitar conexion
lxc config set core.https_address "[::]:8443"

Establecer clave
lxc config set core.trust_password password

Añadir en el cliente el repositorio
lxc remote add atixlibre 192.168.100.110
lxc remote add atixlibre images.atixlibre.org

Listado de repositorios
lxc remote list

Listado de imagenes
lxc image list atixlibre:


Crear un contendore desde el repositorio
lxc launch atixlibre:centos-7 dnsserver

Listado de contenedores remoto
lxc list atixlibre:

Creacion de contendor remoto
lxc launch atixlibre:centos-7 atixlibre:printserver

Detener un contenedor
lxc stop atixlibre:printserver


