---
description: >-
  Los proyectos de node js, por lo general tienen una estructura determinada,
  que tiene en cuenta la creación de los archivos necesarios para su
  funcionamiento, independiente del uso que se le darán a l
---

# Configuración proyecto

## Archivo package.json

Este es un archivo de configuración que se pone en la raíz del proyecto, es donde se define la información básica del proyecto y donde se consigna la información de las dependencias es decir los paquetes que usa el proyecto.

Para crear este archivo, se hace de varias formas, en esta ocación usaremos un comando que crea un archivo por defecto.

```javascript
npm -y init
```

![Salida del comando en consola](<../.gitbook/assets/imagen (48).png>)

{% hint style="info" %}
Este comando crea una estructura en formato json como muestra la imagen y además crea el archivo con nombre package.json.
{% endhint %}

## Instalación paquete

Para instalar un paquete, lo que hacemos es buscar en el buscador de npm, la funcionalidad que requerimos para el proyecto, por lo general ya hay dependencias populares, la idea es empezar por ahí, para nuestro caso usaremos express.

En el buscador de npm ponemos el termino de búsqueda

![Búsqueda del paquete express](<../.gitbook/assets/imagen (46).png>)

Instalamos la dependencia siguiendo las instrucciones como lo indica la [pagina del paquete](https://www.npmjs.com/package/express)

```bash
npm install express
```

Al ejecutar este comando en la consola, se obtiene la siguiente respuesta

![Respuesta del comando de instalación del paquete](<../.gitbook/assets/imagen (43).png>)

{% hint style="info" %}
Se puede abreviar el parametro install y poner solo la letra i
{% endhint %}

En la carpeta del proyecto, se crea la carpeta `node_modules` y en el archivo `package.json` se crea una nueva dependencia, para `express`

![Resultado del proyecto luego de ejecutar los comandos](<../.gitbook/assets/imagen (45).png>)

Por último podemos crear el archivo index.js, en la raíz, para empezar a realizar pruebas, en este caso empezaremos creando un [servidor.](servidor.md)

```javascript
const express = require("express");
const port = 3000;
const app = express();

app.get("/",(req,res)=>{
	res.send("Hola Mundo");
});

app.listen(port,()=>{
	console.log("Funciona!")
});
```

En la consola ejecuta el archivo con `node index.js` y luego ingresas a la url [http://localhost:3000](http://localhost:3000), recuerda que esta url solo funciona en tu computador y siempre y cuando hayas iniciado el servidor local.

![Resultado final de la prueba del proyecto](<../.gitbook/assets/imagen (44).png>)

## Referencias

1. [Getting started express](http://expressjs.com/en/starter/installing.html)
2. [Express](https://www.npmjs.com/package/express)
