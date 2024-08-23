---
layout: post
title:  "C++: Breve introducción a la programación - Parte 2: Tipps de datos"
date:   2024-08-20 09:24:05 -0300
categories: cpp
---
 
## Parte II: Variables, tipos de datos y operadores

Buenas tardes, y bienvenidos a la segunda parte del tutorial de introducción a la programación en C++. En el artículo de hoy, veremos variables, tipos de datos y operadores.

### Variables

Las variables son espacios en memoria utilizados para almacenar información que luego podemos recuperar y utilizar. Tal vez te resulte un poco extraño este concepto, pero puedes pensar en una variable como una caja. 
Una variable es una caja donde puedes guardar cosas (datos) para luego recuperarlas y utilizarlas.
Es importante remarcar que, en C++, las variables deben ser declaradas antes de ser usadas, indicando el tipo de dato que van a contener. Para eso, seguimos la siguiente estructura: `<tipo de dato> <identificador>`. Por ejemplo, si queremos declarar una variable que contenga el año en el que nos encontramos, haríamos lo siguiente:
```cpp
int anio;
```
La primera parte, que llamamos tipo de dato, indica qué contendrá la variable y, por lo tanto, determina el tamaño en memoria que será reservado. 
Ahora, que ya declaramos la variable, podemos "guardar" dentro un valor, para eso usaremos el signo de igualdad `=`.
Sigamos con el ejemplo anterior y asignemos el año actual a la variable:
```cpp
// Utilizando el signo igual asignaremos el valor 2024 a la variable anio

anio = 2024;
```
Las variables pueden ser de varios tipos, como enteros, flotantes, caracteres, cadenas de caracteres o booleanos, veamoslas con algunos ejemplos:

#### Enteros:

Los enteros, Los utilizaremos para almacenar numeros enteros, podemos hacer que estos enteros sean con o sin signo negativo, o que sean pequeños o grandes, esto nos permite ahorrar espacio en memoria, veamos un cuadro con los valores y, luego lo aplicaremos en el IDE:

|Tipo de dato|Rango de numeros|Tamaño en memoria|
|‐----------------------------------------------------------‐-----------------------------|
|short int|-32767 a 32767|16 bits (2 bytes)|
