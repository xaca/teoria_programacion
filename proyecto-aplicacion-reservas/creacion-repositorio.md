---
description: >-
  Para que la aplicación se vea bien, es importante personalizar su aspecto
  gráfico, para esto en esta sección explicaremos de manera breve como podemos
  hacerlo.
---

# Maquillaje \(CSS\)

### ¿Qué es una hoja de estilos?

Es un archivo que se crea aparte del html, en una carpeta llamada **css**, el nombre del archivo por lo general se asigna **main.css**, en este archivo se asignan las reglas gráficas que permiten modificar los elementos o etiquetas html.

{% hint style="info" %}
Válida la carpeta del proyecto, y realiza la configuración corespondiente a la hoja de estilos, recuerda que el nombre de los archivos y carpetas es en mínuscula
{% endhint %}

### **¿Cómo se comunican el html con el css?**

Se hace por medio de la etiqueta _link_, que se pone en el archivo html, que permite vincular el archivo de estilos, adicionalmente se usan los selectores para indicar desde el css que se va a modificar en el html.

### **¿Qué son los selectores?**

Son palabras que se escriben en el html que permiten localizar desde el css a elementos o grupos de elementos que se van a modificar.

#### Existen tres selectores principales:

* Identificador: Se usa para modificar una **única** etiqueta

En el html:

```text
<a href="login.html" id="enlace_login">Login</a>
```

En el css:

```text
#enlace_login{
    /* Acá se ponen las reglas gráficas */
}
```

{% hint style="info" %}
/\* \*/ A escribir un texto entre estos simbolos, se crea un comentario, es decir una sentencia que no se ejecuta como regla de estilo, sirve como informaci\[on sobre el código.
{% endhint %}

* Clase: Permite seleccionar un **grupo** de etiquetas

En el html:

```text
<a href="login.html" class="item_menu">Login</a>
<a href="registro.html" class="item_menu">Registro</a>
<a href="recordar_clave.html" class="item_menu">Recordar contraseña</a>
```

En el css:

```text
.item_menu{
   /* Reglas gráficas que se aplicaran al grupo de etiquetas*/
}
```

{% hint style="info" %}
Los selectores se pueden combinar entre varios elementos, es decir una etiqueta puede tener un selector identificador y una o varias clases, las clases se deben separar por espacios.
{% endhint %}

* Tipo: Son los nombres de las etiquetas que sirven como selectores, pueden ser únicos o grupos, depende del número de etiquetas en el html.

En el html:

```text
<a href="login.html">Login</a>
<a href="registro.html">Registro</a>
<a href="recordar_clave.html">Recordar contraseña</a>
```

En el css:

```text
a{
     /* 
     Reglas gráficas que se aplicarán a los selectores 
     que cumplan con el criterio de selección, es decir
     las etiquetas a (enlaces)          
     */
}
```

### Referencias

\`\`[`Selectores`](https://developer.mozilla.org/es/docs/Web/CSS/CSS_Selectors)\`\`

\`\`[`Comentarios`](https://developer.mozilla.org/en-US/docs/Web/CSS/Comments)\`\`

