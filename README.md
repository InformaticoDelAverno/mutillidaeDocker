# Mutillidae

Este repositorio contiene todo lo necesario para poder construir una imagen de Docker en la que se despliega la aplicación Mutillidae.

Para poder arrancar mutillidae, es necesario un servidor PHP y una base de datos, además de la propia aplicación mutillidae.

Para simplificar al máximo las tareas de mantenimiento de este contenedor, se utiliza XAMPP para instalar el servidor PHP y la base de datos MySQL.

Tanto el instalador de XAMPP como la aplicación mutillidae se encuentran disponibles en este repositorio para poder generar la imagen sin depender de otros repositorios o URLs.


## Generar la imagen

```sh
$ docker build ./dockerFile -t mutillidae
```
## Para arrancar un contenedor
Si has construido localmente la imagen, el comando que debes utilizar es:
```sh
$ docker run -d -p 80:80 -p 443:443 --name mutillidae mutillidae
```
Si no quieres construirte la imagen, puedes utilizar una ya construida que se encuentra publicada en [Docker hub](https://hub.docker.com/r/informaticodelaverno/mutillidae). Para arrancar un contenedor utilizando la imagen pública se debe utilizar:
```sh
$ docker run -d -p 80:80 -p 443:443 --name mutillidae informaticodelaverno/mutillidae:latest
```

 ## Accede a la aplicación
 
Una vez el contenedor se encuentra arrancado, es posible conectarse a la aplicación mutillidae haciendo uso del navegador.
Si has utilizado los comandos mencionados anteriormente, podrás acceder a la aplicación haciendo uso de HTTP y de HTTPS.


  - https://localhost/index.php
  - http://localhost/index.php

## Las dependencias que se incluyen en este repositorio son las siguientes
  - [Mutillidae](https://github.com/webpwnized/mutillidae)
  - [XAMPP (LAMPP)](https://www.apachefriends.org/es/index.html)
