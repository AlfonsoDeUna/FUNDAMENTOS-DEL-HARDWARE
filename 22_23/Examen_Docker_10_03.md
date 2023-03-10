# Examen práctico de Docker

Elige una de las siguiente opciones para realizar de manera práctica.
(En el caso de hacer más de una de las opciones la nota se aumentará)

La valoración de la prueba depende del tipo de ejercicio que has decidido resolver, creatividad, forma de resolverlo.

Debes presentar la prueba práctica un documento donde explicas detalladamente la resolución


## OPCIÓN 1 CREA UN CONTENEDOR PARA LANZAR COMANDOS EN KALI LINUX

1. Arranca un contenedor desde una imagen base kalilinux/kali-rolling.
2. Instala los paquetes amass,  kali-tools-information-gathering con distintas herramientas de redes.
3. Crea una imagen a partir de este contenedor (recuerda que tienes que utilizar el nombre de tu usuario Docker Hub). La imagen se debe llamar <tu_usuario_docker_hub>/comandos_redes.
4. Sube la imagen a Docker Hub.
5. Borra la imagen.
6. Descarga la imagen desde dockerhub y crea un contenedor a partir de ella. (Acuérdate dle paso anterior y borra la imagen en tu ordenador y bájala de Docker Hub en este ejercicio).
7. Lanza en el contenedor el comando nmap

*Deberás entregar los siguientes pantallazos en Classroom en un documento Google docs y adjuntarlo a la tarea*

* Pantallazo donde se vea la creación del contenedor.
* Pantallazo donde se vea el comando que crea la nueva imagen.
* Pantallazo donde se vea la imagen subida a tu cuenta de Docker Hub.
* Pantallazo donde se vea la imagen de la descarga en consola ( la subida a Docker Hub).
* Pantallazo donde se vea la imagen del contenedor ejecutando el comando nmap (de las gathering tools)
* Pantalalzo donde se vea la bajada de la imagen y la creación de un nuevo contenedor.

## OPCIÓN 2 CREA UNA IMAGEN PARA CREAR CONTENEDORES EN NGINX Y VISUALIZAR PÁGINAS WEB ESTÁTICAS


1. Crea una página web estática que contenga tu nombre, la página web se llamará index.html, en un directorio propio que te crees.
2. Crea un fichero Dockerfile que permita crear una imagen con un servidor web: La imagen que tienes que utilizar de Docker_hub**nginx** sirviendo la página. 
3. Realiza la copia en Dockerfile del directorio donde se encuentra el contenido de tu página web estática a /usr/share/nginx/html (nginx)
4. Ejecuta el comando docker que crea la nueva imagen. La imagen se debe llamar <tu_usuario_docker_hub>/mi_servidor_web.
5. Crea un contenedor a partir de ella. (Acuérdate dle paso anterior y borra la imagen en tu ordenador y bájala de Docker Hub en este ejercicio).
6. Ejecuta un contenedor con nombre some-nginx en segundo plano en el puerto 8083 y prueba desde un navegador que aparece tu página web.

*Deberás entregar los siguientes pantallazos en Classroom en un documento Google docs y adjuntarlo a la tarea*

* Pantallazo donde se vea el contenido del fichero Dockerfile.
* Pantallazo donde se vea el comando que crea la nueva imagen.
* (Pantallazo donde se vea la imagen subida a tu cuenta de Docker Hub.) opcional
* Pantallazo donde se vea la creación de un nuevo contenedor.
* Pantallazo donde se vea en el navegador web la página web estática con tu nombre.

## OPCIÓN 3 CREA UN SERVIDOR QUE EJECUTE PHP Y VISUALIZAR PÁGINAS EN PHP

Crea un directorio llamado app con un fichero que sea index.php en su interior añade el siguiente código


```php


<html>
<body>
El usuario es <pon aquí tu nombre>
La fecha del día de hoy es: <?= date("d/m/Y"); ?>.
<br />
La hora local del servidor es: <?= date("G:i:s"); ?>.

</body>
</html>

```

1. Crea un fichero Dockerfile que permita crear una imagen con un servidor web: La imagen que tienes que utilizar de Docker_hub **debian**
2. Especifica en Dockerfile que instale los siguientes paquetes: apache2 libapache2-mod-php7.3 php7.3
3. Especifica en Dockerfile que copie el directorio app creado anteriormente en el directorio /var/www/html/
4. Especifica en Dockerfile que lance el siguiente comando: rm /var/www/html/index.html
5. Especifica en Dockerfile que usaremos el puerto 80
6. Especifica en DockerFiel que lance el siguiente comando: "/usr/sbin/apache2ctl" -D en modo "FOREGROUND"
7. Ejecuta el comando docker que crea la nueva imagen. La imagen se debe llamar <tu_usuario_docker_hub>:v1
8. (opcional) Sube la imagen a Docker Hub a tu usuario
9. Crea un contenedor con el siguiente nombre ejemplo_<tu_nombre> en el puerto 80
10. Abre un navegador localhost puerto 80 por defecto y muestra la página php funcionando.
11. Dentro del navegador abre el fichero php.info

*Deberás entregar los siguientes pantallazos en Classroom en un documento Google docs y adjuntarlo a la tarea*

* Pantallazo donde se vea el contenido del fichero Dockerfile.
* Pantallazo donde se vea el comando que crea la nueva imagen.
* (Pantallazo donde se vea la imagen subida a tu cuenta de Docker Hub.) opcional
* Pantallazo donde se vea la creación de un nuevo contenedor.
* Pantallazo donde se vea en el navegador web la página index.php donde se vea el usuario, fecha y hora.
* Pantallazo donde se vea en el navegador web la página info.php donde se vea la información de php.





