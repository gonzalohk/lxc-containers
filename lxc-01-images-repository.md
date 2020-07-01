## Repositorios
Listado de repositorios remotos
```
lxc remote list
```

Listado de un repositorio específico
```
lxc image list images:
lxc image list ubuntu:
```
Listado de imágenes del repositorio local
```
lxc image list
```
Listado por tipo de arquitectura
```
lxc image list amd64
```
Informacion de una imagen
```
lxc image info centos-7
```
Editar propiedades de una imagen
```
lc image edit ubuntu
```
Eliminar una imagen
```
lxc image delete ubuntu
```
Copiar una imagen al repositorio local
```
lxc image copy ubuntu:16.04 local:
```
Copiar la imagen con un alias
```
lxc image copy ubuntu:18.04 local: --alias ubuntu18
```
Copiar la imagen con su alias original
```
lxc image copy ubuntu:18.04 local: --copy-aliases
```