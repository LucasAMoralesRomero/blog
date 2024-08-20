---
layout: post
title:  "C++: Breve introducción a la programación - Parte 2: Tipps de datos"
date:   2024-08-20 09:24:05 -0300
categories: cpp
---


## Parte II: Variables, tipos de datos y operadores

Buenas tardes, y bienvenidos a la segunda parte del tutorial de inroduccion a la programacion en C++, en el articulo veremos variables, tipos de datos y operadores.

Comencemos con las variables

### Variables

Las variables, es un espacio en memoria utilizado para almacenar informacion que luego utilizaremos, tal vez te resulte un poco extrano esto, pero puedes pensarlo como una caja una variable es una caja conde puedes guardar cosas (datos) para luego reuperarlas y utilizarlas.
Es importante remarcar que en C++ las variables deben ser declaradas antes de ser usadas indicando el tipo de dato que va a contener, para declararlo,seguimos la siguiente  estructura `<tipo de dato><identificador>`, por ejemplo declaremos una variable que contenga el anio en el que nos encontramos:

```cpp
int anio;
```
la primer parte que llamamos tipo de dato, indica lo que contendra la variable y, por lo tanto determina el tamano en memoria para reservarlo, una vez declarado, podemos  asignarle un valor utilizando el signo igual `=`, sigamoscon el ejemplo anterior del anio en el que nos encontramos asignemosle el anio:

```cpp
//utilizando el signo igual asignaremos elvalor 2004 a la variable anio
anio = 2004;
```


Caracteres: char (también es un entero), wchar_t
Enteros: short, int, long, long long
Números en coma flotante: float, double, long double
Booleanos: bool
Vacío: void
