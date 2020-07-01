## Storage
Listado de pools de almacenamiento
```
lxc storage list
```
Informacion de almacenamiento
```
lxc storage info lxd
```
Propiedades de un storage
```
lxc storage show lxd
```
Listados volúmenes
```
lxc storage volume list lxd
```
Creación volúmenes
```
lxc storage volume create lxd vol10
```
Asociar 
```
lxc storage volume attach lxd vol10 webserver data /opt/data
```
Desasociar
```
lxc storage volume detach lxd vol10 webserver data
```
Copiar volumen
```
lxc storage volume copy lxd/vol10 lxd/vol11
```
Eliminar
```
lxc storage volume delete lxd vol11
```