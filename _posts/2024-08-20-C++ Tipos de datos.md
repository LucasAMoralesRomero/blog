---
layout: post
title:  "C++: Breve introducción a la programación - Parte 2: Tipos de datos"
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
Las variables pueden ser de varios tipos, como enteros, numeros no enteros (flotantes), caracteres o booleanos, veamoslas con algunos ejemplos:

### Tipos de datos

#### Enteros:

Los enteros, Los utilizaremos para almacenar numeros enteros, podemos hacer que estos enteros sean con o sin signo negativo, o que sean pequeños o grandes, esto nos permite ahorrar espacio en memoria, veamos un cuadro con los valores y, luego lo aplicaremos en el IDE:

|Tipo de dato|Rango de numeros que puede almacenar|Tamaño en memoria|
|------------|------------------------------------|-----------------|
|short int   |-32767 a 32767                      |16 bits (2 bytes)|
|unsigned short int|0 a 65535                     |16 bits (2 bytes)|
|int         |            -2147483647 a 2147483647|32 bits (4 bytes)|
|unsigned int|0 a 4294967295                      |32 bits (4 bytes)|
|long int    |            -2147483647 a 2147483647|32 bits (4 bytes)|
|unsigned long int|0 a 4294967295                 |32 bits (4 bytes)|

Estos tipos de datos, aunque parecidos son diferentes, pero, ¿por que? ¡porque cada uno se puede usar para distintos casos!

**Short int** puede utilizarse para almacenar numeros que seran positivos o negativos, pero que no seran muy grandes, como por ejemeplo la temperatura medida por un sensor de temperatura, mientras que **unsigned short int** puede ser utilizado para valores que no seran negativos, como por ejemplo los dias del año, la edad de una persona.

**Int** se puede utilizar para valores positivos o negativos que sean modeardamente grandes, como el balance de la cuenta de una persona, mientras que **unsigned int** puede utilizarse para valores que sean positivos y moderadamente grandes, como la distancia recorrida cuando andamos en bicicleta o la cantidad de puntos que hagamos en un juego.

**Long int** se puede utilizar para numeros muy grandes, como por ejemplo el balance de una empresa o las deudas de un pais, mientras que **unsigned long int** se utiliza para almacenar datos muy grandes, pero que no pueden ser negativos, como las estrellas en la galaxia.

#### Numeros no enteros:

Los numeros no enteros, o flotantes son los numeros que poseen una parte fraccional (como por ejemplo el peso de una porcion de queso), existen dos tipos los **float** y los **double**, ¿la diferencia entre ellos? ¡la presicion!, por ejemplo con **float** podemos almacenar la altura de un edificio o la temperatura en el interior de una casa.
**Double** posee una mayor presicion, lo podemos usar para almacenar calculos financieros, o la distancia recorrida por una sonda espacial

| Tipo de dato |            Rango de números que puede almacenar                 | Tamaño en memoria |
|--------------|-----------------------------------------------------------------|-------------------|
| float        | Aproximadamente 1.2 × 10<sup>-38</sup> a 3.4 × 10<sup>38</sup>  | 32 bits (4 bytes) |
| double       | Aproximadamente 2.2 × 10<sup>-308</sup> a 1.7 × 10<sup>308</sup>| 64 bits (8 bytes) |

#### Caracteres (char):

Los **caracteres** almacenan dentro de una variable un caracter de la labla ASCII, en memoria va a ocupar un byte, por lo que va a poder almacenar una letra, un numero o un simblolo.

#### Booleanos:

Los **booleanos** almacenan dos valores `verdadero` o `falso` 