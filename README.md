# docker-apache
## Part 1
1.1.- Descargar la imagen de Docker:
```php
docker pull bitnami/apache
```
1.2.- Crear el contenedor
```php
sudo docker run --name xxxx -P bitnami/apache:latest
```
1.3.- Consultar los puertos docker asigandos
```php
sudo docker ps -a
```
Despues de optener los puertos:
```php
sudo docker ps -a
```
Puedes abrir el navegador en uno de los puertos para comprobarlos, si todo esta bien veras el mensaje *It Works*
## Part 2
###### 2.1.- Generar volúmenes y asociarlos a un contenedor Docker generado
