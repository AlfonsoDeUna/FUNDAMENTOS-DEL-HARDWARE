# Examen práctico de Docker

Elige una de las siguiente opciones para realizar de manera práctica.
(En el caso de hacer más de una de las opciones la nota se aumentará)

La valoración de la prueba depende del tipo de ejercicio que has decidido resolver, creatividad, forma de resolverlo.

Debes presentar la prueba práctica un documento donde explicas detalladamente la resolución


## OPCIÓN 1 CREA UN CONTENEDOR PARA LANZAR COMANDOS EN KALI LINUX

Arranca un contenedor desde una imagen base kalilinux/kali-rolling.
Instala los paquetes amass,  kali-tools-information-gathering con distintas herramientas de redes.
Crea una imagen a partir de este contenedor (recuerda que tienes que utilizar el nombre de tu usuario Docker Hub). La imagen se debe llamar <tu_usuario_docker_hub>/comandos_redes.
Sube la imagen a Docker Hub.
Borra la imagen.
Descarga la imagen desde dockerhub y crea un contenedor a partir de ella. (Acuérdate dle paso anterior y borra la imagen en tu ordenador y bájala de Docker Hub en este ejercicio).
Lanza en el contenedor el comando nmap 
Lanza 
Deberás entregar los siguientes pantallazos en Classroom

Pantallazo donde se vea la creación del contenedor.
Pantallazo donde se vea el comando que crea la nueva imagen.
Pantallazo donde se vea la imagen subida a tu cuenta de Docker Hub.
Pantallazo donde se vea la imagen de la descarga en consola ( la subida a Docker Hub).
Pantallazo donde se vea la imagen del contenedor ejecutando el comando nmap (de las gathering tools)
Pantalalzo donde se vea la bajada de la imagen y la creación de un nuevo contenedor.

## OPCIÓN 2 CREA UNA IMAGEN PARA CREAR CONTENEDORES EN NGINX Y VISUALIZAR PÁGINAS WEB ESTÁTICAS

Crea una página web estática que contenga tu nombre, la página web se llamará index.html, en un directorio propio que te crees.
Crea un fichero Dockerfile que permita crear una imagen con un servidor web: La imagen que tienes que utilizar de Docker_hub**nginx** sirviendo la página. 
Realiza la copia en Dockerfile del directorio donde se encuentra el contenido de tu página web estática a /usr/share/nginx/html (nginx)
Ejecuta el comando docker que crea la nueva imagen. La imagen se debe llamar <tu_usuario_docker_hub>/mi_servidor_web.
Crea un contenedor a partir de ella. (Acuérdate dle paso anterior y borra la imagen en tu ordenador y bájala de Docker Hub en este ejercicio).
Ejecuta un contenedor con nombre some-nginx en segundo plano en el puerto 8083 y prueba desde un navegador que aparece tu página web.

Deberás entregar los siguientes pantallazos comprimidos en un zip o en un documento pdf:

Pantallazo donde se vea el contenido del fichero Dockerfile.
Pantallazo donde se vea el comando que crea la nueva imagen.
(Pantallazo donde se vea la imagen subida a tu cuenta de Docker Hub.) opcional
Pantallazo donde se vea la creación de un nuevo contenedor.
Pantallazo donde se vea en el navegador web la página web estática con tu nombre.

# OPCIÓN 3 CREA UN SERVIDOR QUE EJECUTE PHP Y VISUALIZAR PÁGINAS EN PHP

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
Crea un fichero Dockerfile que permita crear una imagen con un servidor web: La imagen que tienes que utilizar de Docker_hub **debian** 
Especifica en Dockerfile que instale los siguientes paquetes: apache2 libapache2-mod-php7.3 php7.3
Especifica en Dockerfile que copie el directorio app creado anteriormente en el directorio /var/www/html/
Especifica en Dockerfile que lance el siguiente comando: rm /var/www/html/index.html
Especifica en Dockerfile que usaremos el puerto 80
Especifica en DockerFiel que lance el siguiente comando: "/usr/sbin/apache2ctl" -D en modo "FOREGROUND"
Ejecuta el comando docker que crea la nueva imagen. La imagen se debe llamar <tu_usuario_docker_hub>:v1
(opcional) Sube la imagen a Docker Hub a tu usuario
Crea un contenedor con el siguiente nombre ejemplo_<tu_nombre> en el puerto 80
Abre un navegador localhost puerto 80 por defecto y muestra la página php funcionando.
Dentro del navegador abre el fichero php.info

Deberás entregar los siguientes pantallazos comprimidos en un zip o en un documento pdf:

Pantallazo donde se vea el contenido del fichero Dockerfile.
Pantallazo donde se vea el comando que crea la nueva imagen.
(Pantallazo donde se vea la imagen subida a tu cuenta de Docker Hub.) opcional
Pantallazo donde se vea la creación de un nuevo contenedor.
Pantallazo donde se vea en el navegador web la página index.php donde se vea el usuario, fecha y hora.
Pantallazo donde se vea en el navegador web la página info.php donde se vea la información de php.





