# Instalación y configuración de Git en local


Git es un sistema de control de versiones que nos sirve para poder tener un sistema de seguimiento de nuestras prácticas o proyectos tanto de nosotros como de la empresa con la que estemos trabajando.
La mayoría de empresas,por no decir todas, actualmente usan un sistema de control de versiones para sus proyectos,acompañándose de software donde se almacenan los repositorios como GitHub.

En la guia que estás viendo a continuación vamos a aprender a configurar Git en una máquina Ubuntu 21.04.Lo primero que haremos sera instalarlo a través del administrador de paquetes que nos viene en el sistema operativo,una vez hecho esto lo configuraremos de manera que sea más facil poder recoger y subir información a nuestros proyectos.


## Instalación de Git con el administrador de paquetes de Ubuntu


### Comprobar que está todo correcto
Lo primero que debemos tener es una máquina Ubuntu.
Una vez dentro de la máquina procederemos a abrir una terminal y pondremos el siguiente comando.

![Captura1](https://media.discordapp.net/attachments/889884555736121365/890656207675719740/unknown.png)

Este comando nos sirve para actualizar los repositorios donde se almacenan los paquetes de aplicaciones que podemos tener en máquinas Linux y normalmente son Software Libre.

Otra cosa que podemos hacer y es recomendable si llevamos bastante tiempo con la máquina y no hemos actualizado las aplicaciones de este es ejecutar el comando:
**Sudo apt-get upgrade**
El cual sirve para actualizar las aplicaciones que tengan una nueva versión de esta.


### Instalación

El siguiente paso que debemos hacer es comprobar que no tenemos Git instalado,esto lo podemos hacer con el comando git --version .Si no está instalado nos dará la siguiente salida:


![Captura2](https://media.discordapp.net/attachments/889884555736121365/890656251959201792/unknown.png)

En caso de que la salida sea un mensaje el cual sea algo así: **git version 2.30.2**
significa que ya tiene instalado y lo que tendrá que hacer es pasar al apartado de configuración de Git.

Si no lo tiene instalado y le ha salido el mensaje que apareció en la última captura lo que tendrá que hacer es ejecutar el comando **sudo apt install git.**

Una vez ejecutado el comando comprobamos que hemos instalado bien Git ejecutando el comando que ya hicimos antes para comprobar si lo teníamos instalado y ahora nos debería salir lo que se ve en la siguiente captura:
![Captura3](https://media.discordapp.net/attachments/889884555736121365/890656294866911232/unknown.png)

Una vez hecho esto hemos terminado la instalación de Git y procederemos a configurarla.


### Configuración de Git
Lo que debemos hacer para configurar Git correctamente es configurar el usuario y el correo electrónico.


Configuración usuario
Para configuar el  usuario en Git debemos ejecutar el siguiente comando:


**git config --global user.name “Tu nombre”**

Configuración correo
Para configurar el correo electrónico debemos ejecutar el siguiente comando:


**git config --global user.email “Tucorreoelectronico@gmail.com”**

### Comprobar Usuarios configurados
Para comprobar los usuarios que estan configurados bastaría con ejecutar el siguiente comando:

**git config --list**
![Captura3](https://media.discordapp.net/attachments/889884555736121365/890656340899430400/unknown.png)


Otra manera que podemos usar para poder configurar el git es entrar directamente en el archivo de configuración de Git de la siguiente manera.

**nano ~/.gitconfig**


El siguiente comando debería de abrirse un editor de texto dentro de la consola el cual te dejará editar el usuario que has añadido anteriormente.

![Captura4](https://media.discordapp.net/attachments/889884555736121365/890656395161124884/unknown.png)

Para salir de este editor una vez hemos editado nuestra configuración es pulsando **CTRL + X y luego de este pulsando la Y,ENTER** para guardar los cambios correctamente.

Una vez hecho todo.Ya habremos instalado y configurado Git.
