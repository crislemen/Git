Cristian León Méndez

# Desplegar una aplicación de Node js con Docker

![](./img/Aspose.Words.71cb264d-a29a-47d6-a8b4-d6b89ee40057.001.png)

## Crear la aplicación de nodejs

Lo primero que haremos será crearnos una carpeta donde pondremos todos los ficheros que necesitamos para poder desplegar la aplicación.

Una vez estemos dentro.Crearemos el primer fichero que será un **package.json** donde describirá nuestra aplicación y las dependencias que necesitaremos.El contenido del archivo debé ser el siguiente:

![](./img/Aspose.Words.71cb264d-a29a-47d6-a8b4-d6b89ee40057.002.png)

Cuando hayamos puesto el contenido en el package.json.Deberemos abrir una terminal y ejecutar el comando **npm install (**Deberás tener una version de npm 5 o superior**).** Este comando nos generará todas las dependencias y un archivo **package-lock.json** que será el que se copiara en la imagen de docker

![](./img/Aspose.Words.71cb264d-a29a-47d6-a8b4-d6b89ee40057.003.jpeg)

Ahora creamos otro fichero llamado **server.js** que definirá que queremos usar **Express.js:**

![](./img/Aspose.Words.71cb264d-a29a-47d6-a8b4-d6b89ee40057.004.png)

## Crear el dockerfile

Creamos un archivo dockerfile donde debemos poner lo siguiente:

![](./img/Aspose.Words.71cb264d-a29a-47d6-a8b4-d6b89ee40057.005.jpeg)

Construir la imagen de docker

Para construir la imagen de docker una vez haber hecho todo lo anterior del informe,debemos ejecutar el siguiente comando:

**docker build . -t tunombre/node-web-app**

Si esta ha funcionado correctamente,nos dará el siguiente resultado a ejecutar el comando **sudo docker images**

![](./img/Aspose.Words.71cb264d-a29a-47d6-a8b4-d6b89ee40057.006.png)

## Arrancar la imagen

Para arrancar la imagen lo que debemos hacer es ejecutar el comando **docker run -p 49160:8080 -d tunombre/node-web-app**

![](./img/Aspose.Words.71cb264d-a29a-47d6-a8b4-d6b89ee40057.007.png)

![](./img/Aspose.Words.71cb264d-a29a-47d6-a8b4-d6b89ee40057.008.png)

![](./img/Aspose.Words.71cb264d-a29a-47d6-a8b4-d6b89ee40057.009.png)

## Resultado de Testeo

![](./img/Aspose.Words.71cb264d-a29a-47d6-a8b4-d6b89ee40057.010.png)

![](./img/Aspose.Words.71cb264d-a29a-47d6-a8b4-d6b89ee40057.011.png)
