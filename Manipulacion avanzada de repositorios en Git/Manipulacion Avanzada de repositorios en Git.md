Cristian León Méndez

### Manipulación avanzada de repositorios en Git


En este informe vamos a enseñar algunos comandos avanzados para manejar nuestros repositorios en git explicando que hace cada uno de los comandos que vamos a utilizar.

Para esto lo primero que haremos sera clonar el siguiente repositorio: <https://github.com/jpexposito/libro.git>

Para clonar un repositorio se usa el comando **git clone**

Para entrar en el repositorio usaremos el comando **cd libros**

Una vez hemos hecho esto,comenzaremos con los ejemplos de los uso de los comandos avanzados en Git

Ejercicio 1

- **Mostrar el historial de cambios del repositorio**
- Para esto usaremos el comando **git log**
- **Crear la carpeta capítulos y crear dentro de ella el fichero capitulo1.txt con el siguiente texto.**

*Git es un sistema de control de versiones ideado por Linus Torvalds.*

- Se puede hacer de distintas maneras pero en este caso elegiremos usar cat para crear el archivo desde la terminal y editar el archivo en el mismo momento.Para hacer esto debemos poner en la terminal **cat > capitulo1.txt ,** le damos a **ENTER**, escribimos lo que queramos que esté dentro del fichero,para salir y guardar lo que hemos escrito debemos hacer la combinación de teclas **CTRL + D**. Haciendo esto ya hemos creado el fichero y le hemos puesto el contenido que queremos.
- **Añadir los cambios a la zona de intercambio temporal.**
  - Para añadir los cambios a la zona de intercambio temporal se usa el comando **git add .**
- **Hacer un commit de los cambios con el mensaje *Añadido capítulo 2.***
  - Un commit es un mensaje descriptivo que nos indica que cambios hemos hecho en los ficheros,para hacer un commit debemos poner **git commit -m “Texto descriptivo”**
- **Volver a mostrar el historial de cambios del repositorio.**
  - Lo que debemos hacer es lo mismo que hemos hecho anteriormente, **git log**

A continuación hay una serie de capturas  donde se ven las salidas de todos los comandos que hemos explicado anteriormente:![](./img/1.png)

Ejercicio 2:

- **Crear el fichero capitulo2.txt en la carpeta capítulos con el siguiente texto**

***El flujo de trabajo básico con Git consiste en: 1- Hacer cambios en el repositorio. 2- Añadir los cambios a la zona de intercambio temporal. 3- Hacer un commit de los cambios.***

- Usaremos el mismo comando que usamos antes **cat > capitulo2.txt**
- **Añadir los cambios a la zona de intercambio temporal.**
  - **git add .**
- **Hacer un commit de los cambios con el mensaje Añadido capítulo 2.**
  - **git commit -m “Añadido capitulo 2”**
- **Mostrar las diferencias entre la ultima versión y dos versiones anteriores.**
  - Para mostrar las diferencias entre versiones en Git se usa git diff, en este caso tendremos que poner **git diff HEAD~2..HEAD![](./img/2.png)**

En la siguiente captura se ve como debería de salirte en tu terminal:


Ejercicio PAGE3

- **Crear el fichero capitulo3.txt en la carpeta capitulos con el siguiente texto. *Git permite la creación de ramas lo que permite tener distintas versiones del mismo proyecto y trabajar de manera simultanea en ellas.***
  - **cat > capitulo3.txt**
- **Añadir los cambios a la zona de intercambio temporal**
  - **git add .**
- **Hacer un commit de los cambios con el mensaje *Añadido capitulo 3.***
  - **git commit -m “Añadido capitulo 3”**
- **Mostrar las diferencias entre la primera y la última versión del repositorio.**
  - **git diff HEAD~ ..HEAD![](./img/3.png)**

A continuación la captura con los resultados de los comandos:

Ejercicio 4

- **Añadir al final del fichero indice.txt la siguiente línea:![](./img/4.png)**

***Capítulo 5: Conceptos avanzados***

- Para agregar contenido al final de un fichero lo que debemos hacer es usar el siguiente comando **echo “Capítulo 5:Conceptos avanzados” >> indice.txt**
- **Añadir los cambios a la zona de intercambio temporal.**
  - **git add .**
- **Hacer un commit de los cambios con el mensaje *Añadido capitulo 5 al índice.***
  - **git commit -m “Añadido capitulo 5 al índice”**
- **Mostrar quien ha hecho cambios sobre el fichero indice.txt**
  - Para ver quien ha hecho los cambios del fichero bastaría con usar el comando **git annotate indice.txt**

En la siguiente captura veras los resultados del ejercicio:


Ejercicio 5

- **Crear una rama bibliografia y mostrar las ramas del repositorio**
- Para crear una nueva rama usaremos el comando **git branch bibliografía![](./img/5.png)**
- Para mostrar las ramas del repositoria bastaría con poner **git branch**

Ejercicio 6

- **Crear el fichero capitulo4.txt y añadir el texto siguiente:**

***En este capítulo veremos cómo usar GitHub para alojar repositorios en remoto.***

- **cat > capitulo4.txt**
- **Añadir los cambios a la zona de intercambio temporal.**
  - **git add .**
- **Hacer un commit con el mensaje “Añadido capitulo 4.”**
  - **git commit -m “Añadido capitulo 4”**
- **Mostrar la historia del repositorio incluyendo todas las ramas.**
  - Para esto debemos usar el comando **git log** añadiendo tambien **--all** que nos sirve para incluir todas las ramas

Aquí verá los resultados del ejercicio:

Ejercicio 7

- **Cambiar a la rama bibliografía.**
- Para cambiar de rama basta con usar el comando **git checkout bibliografía**
- **Crear el fichero bibliografía.txt y añadir la siguiente referencia:**

***Chacon, S. and Straub, B. Pro Git. Apress.***

- **cat > bibliografía.txt**
- **Añadir los cambios a la zona de intercambio temporal.**
  - **git add .**
- **Hacer un commit con el mensaje “Añadida primera referencia bibliográfica.”**
  - **git commit -m “Añadida primera referencia bibliográfica.”**
- **Mostrar la historia del repositorio incluyendo todas las ramas.**
  - Además de poder ver la historia de las ramas con el comando **git log --all ,**también podemos añadir dos cosas más , **--graph** para que se vea de forma gráfica el ultimo cambio y también le añadimos **--oneline** para que se vea los cambios más resumidos.Por lo que el comando será **git log --graph --all --oneline![](./img/6.png)**

Adjunto captura de los resultados obtenidos:


Ejercicio 8

- **Fusionar la rama bibliografía con la rama main.**
  - Para fusionar una rama con otra debemos usar el comando **git merge**
- **Mostrar la historia del repositorio incluyendo todas las ramas.**
  - **git log --graph --all --oneline**
- **Eliminar la rama bibliografia**
  - Para eliminar una rama tenemos que utilizar el comando **git branch** y debemos añadir **-d** y el nombre del repositorio,en este caso **git branch -d bibliografia**
- **Mostrar de nuevo la historia del repositorio incluyendo todas las ramas.**
  - **git log --graph --all --oneline**

Captura de pantalla con el resultado del ejercicio:![](./img/7.png)


Ejercicio 9

- **Crear la rama bibliografía.**
  - **git branch bibliografia**
- **Cambiar a la rama bibliografía.**
  - **git checkout bibliografia**
- **Cambiar el fichero bibliografia.txt para que contenga las siguientes referencias:**

***Scott Chacon and Ben Straub. Pro Git. Apress.***

***Ryan Hodson. Ry’s Git Tutorial. Smashwords (2014)***

- **Cambiar a la rama main.**
  - **git checkout main**
- **Cambiar el fichero bibliografia.txt para que - contenga las siguientes referencias:**
- **Añadir los cambios a la zona de intercambio temporal y hacer un commit con el mensaje “Añadida nueva referencia bibliográfica.”**
- **Fusionar la rama bibliografía con la rama main.**
- Para fusionar dos ramas lo que debemos usar es el comando **git merge bibliografia**
- **Resolver el conflicto dejando el fichero bibliografia.txt con las referencias: Chacon, S. and Straub, B. Pro Git. Apress. Loeliger, J. and McCullough, M. Version control with Git. O’Reilly.**
  - Lo que haremos para arreglar el conflicto es entrar con el editor nano y cambiar lo correspondiente para que no haya problemas,por lo que debemos poner en la linea de comandos **nano bibliografia.txt**
- **Añadir los cambios a la zona de intercambio temporal y hacer un commit con el mensaje “Resuelto conflicto de bibliografía.”**
  - **git add . | git commit -m “Resuelto conflicto de bibliografia”**
- **Mostrar la historia del repositorio incluyendo todas las ramas.**
- **git log --all --oneline --graph**

A continuacion tenemos las capturas con la solucion del ejercicio

![](./img/8.png)


![](./img/9.png)

![](./img/10.png)
