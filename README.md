# docker-apache
## Parte 1
#### Crear el contenedor Apache
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
docker port apache
```
Despues de optener los puertos:
```php
8443/tcp -> 0.0.0.0:32768
8080/tcp -> 0.0.0.0:32769
```
Puedes abrir el navegador en uno de los puertos para comprobarlos, si todo esta bien veras el mensaje *It Works*
#### Modificar la imagen del contenedor Apache (página inicial)
1.4.- Crear otro contenedor
```php
sudo docker run --name xxxx2 -P bitnami/apache:latest
```
1.5.- Crear un archivo index.html para remplazar el que ya existe:
```php
sudo nano index.html
```
Archivo .html:
```html
  <!DOCTYPE html>
    <html lang="es">
    <head>
      <meta charset="utf-8">
      <title>Apache en Docker</title>
      <meta name="viewport" content="width=device-width, initial-scale=1.0">
    </head>
    <body>
      <h1>¡Hola, mundo!</h1>
    </body>
  </html>
```
1.6.- Copiar el archivo index.html que acabamos de crear en el contenedor
```php
sudo docker cp index.html xxxx2:/opt/bitnami/apache/htdocs/index.html
```
Comprobar en el navegador que el archivo se actualizó correctamente, si es así, veras el mensaje *¡Hola, mundo!*
###### Crear una nueva imagen
asdsad
## Parte 2
###### 2.1.- Generar volúmenes y asociarlos a un contenedor Docker generado
