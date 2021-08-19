---
description: >-
  Estas estructuras permiten realizar operaciones repetitivas, las cuales se
  ejecutan siempre y cuando se cumpla una condición.
---

# Estructuras cíclicas

### Ciclo while - mientras que

Se ejecuta mientras que la condición sea verdadera, primero se evalua la condición y luego si la condición es verdadera se realiza el procedimiento interno definido entre llaves.

![Diagrama de flujo y ejemplo de c&#xF3;digo ciclo while](../.gitbook/assets/imagen%20%2817%29.png)

```text
var condicion = true;

while(condicion){
    console.log("Entra al ciclo, porque la condición es verdadera");
    condicion = false;
}
```

{% hint style="info" %}
Internamente el ciclo debe definir una sentencia o procedimiento que convierta la condición en falso, para poder salir del ciclo. De otra forma se produce un ciclo infinito.
{% endhint %}

### Ciclo do-while / hasta que

Se ejecuta primero el procedimiento interno en el ciclo y al final se evalua la condición.

![Diagrama de flujo y ejemplo de c&#xF3;digo ciclo do-while](../.gitbook/assets/imagen%20%2810%29.png)

```text
var condicion = false;

do{
    console.log("Siempre se ejecuta por lo menos una vez esta instrucción");
}while(condicion);
```

{% hint style="info" %}
Esta es de las pocas instrucciones en javascript que se pone un punto y coma al final, en javascript no es obligatorio poner punto y coma en ninguna sentencia, pero se recomienda hacerlo por mantener un estandar similar a otros lenguajes de programación.
{% endhint %}

¿Por qué no hay un ciclo infinito en el código de ejemplo del ciclo hasta que?

### Ciclos for

El ciclo for funciona similar a los ciclos anteriores, la única diferencia es que depende por lo general de un valor de control que define el número de iteraciones que realizará el ciclo. En javascript hay varias versiones, estudiaremos algunas de ellas:

![Diagrama de flujo y ejemplo de c&#xF3;digo ciclo for](../.gitbook/assets/imagen%20%2811%29.png)

#### Ciclo for tradicional

```text
for(var i = 0; i < 10; i++)
{
  console.log("Iteracion #",i);
}
```

{% hint style="info" %}
Recuerde que la expresión i++ es una versión simplificada de i = i + 1, es conocida como el operador pos incremento
{% endhint %}

#### Ciclo for + operador in

Permite recorrer una estructura en el siguiente ejemplo se muestra como imprimir cada uno de los valores de un arreglo usando esta variación de este ciclo. Incluye propiedades de objetos.

```text
var arreglo = [2,3,4,5,7,8];
for(var i in arreglo)
{
    console.log(i);
}
```

{% hint style="info" %}
La estructura arreglo, array o vector se estudiará más adelante, junto con los objetos
{% endhint %}

#### Ciclo for + operador of

Permite iterar sobre colecciones como arreglos, no incluye propiedades de objetos.

```text
var arreglo = [2,3,4];
arreglo.propiedad = "prueba";

for(var i of arreglo)
{
    console.log(i);
}
```

{% hint style="info" %}
Ejecute los dos ciclos anteriores y encuentre sus similitudes y diferencias
{% endhint %}

### Control adicional

#### break

Termina la ejecución del ciclo en el momento de su invocación

```text
while(true)
{
   if(Math.random()>.5)
   {
      break;
   }
}
```

{% hint style="info" %}
¿Por qué el ciclo anterior, no es un ciclo infinito?, ¿Cuántas veces se ejecuta?
{% endhint %}

#### continue

Avanza una iteración, pero no detiende la ejecución del ciclo

```text
for(var i=0;i<=10;i++){
    if(i%2==0)
    {
        continue;
    }
    console.log(i);
}
```

{% hint style="info" %}
¿Cuál es el resultado al ejecutar el ciclo anterior?
{% endhint %}

{% embed url="https://www.youtube.com/watch?v=Zp4ZrLpUmog" caption="Explicación y uso de ciclos en javascript " %}

### Bestiario de variables

#### Bandera

Controla el estado de una variable, puede ser true o false, dependiendo de este valor se toman decisiones en la ejecución del código.

![Ejemplo uso de una variable como una bandera de control](../.gitbook/assets/imagen%20%2818%29.png)

#### Centinela

Vigila que se produzca un valor, por lo general este valor es ingresado por el usuario, se puede usar por ejemplo para leer un grupo de valores y se incluye un centinela para terminar la lectura de los datos.

![Ejemplo de uso de un ciclo que se controla por medio de un centinela](../.gitbook/assets/imagen%20%289%29.png)

#### Contador

Variable que se incrementa por lo general en una unidad cada vez, se usa por ejemplo para contar o controlar el número de iteraciones que ejecuta un ciclo.

![Control de ejecuci&#xF3;n de un ciclo while, por medio de un contador](../.gitbook/assets/imagen%20%2813%29.png)

#### Acumulador

Es similar al contador, se diferencia en la forma como realiza el incremento, ya que puede acumular sumando, multiplicando, dividiendo, etc.

![Control de ejecuci&#xF3;n de un ciclo while usando un amuculador que multiplica el valor por 2](../.gitbook/assets/imagen%20%2815%29.png)

### Referentes

* [¿for each en javascript?](https://es.stackoverflow.com/questions/17640/for-each-en-javascript)
* [for ...of](https://developer.mozilla.org/es/docs/Web/JavaScript/Reference/Statements/for...of)
* [The for-of loop](https://exploringjs.com/es6/ch_for-of.html)

### Ejercicios

1. ¿Cuál es el operador preincremento, predecremento, posdecremento? Escriba ejemplos donde se evidencie su uso.
2. ¿Existe el preproducto, posdivisión...?
3. ¿Para que se utiliza forEach, every, some? 🤓Bonus



