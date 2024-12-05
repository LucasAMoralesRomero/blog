---
layout: post
title:  "C++: Breve introducción a la programación - Parte 3: Estructuras de control"
date:   2024-12-05 09:24:05 -0300
categories: cpp
---

 Buenos dias, y bienvenidos a la tercera parte del tutorial de introducción a la programación en C++.

 Hoy, aprenderemos sobre las **estructuras de control**, herramientas fundamentales que nos permiten tomar decisiones y repetir acciones en nuestros programas.

En el artículo de hoy, exploraremos los conceptos de **condicionales** (para decidir que parte del código ejecutar en base a condiciones) y **bucles** (para poder repetir porciones de código tantas veces como sea necesario).

¡Empecemos!

### Condicionales

Los condicionales nos permiten tomar decisiones, evaluando una o más condiciones.
Comencemos viendo el **if**, **else if** y **else** 

#### If, else if y else

Mediante estas instrucciones podremos tomar decisiones, evaluando si es verdadero o falso la condición que se le indica, veamos la estructura de un if:

```cpp
if (condicion-a-evaluar) {
 código a ejecutar si la condición es verdadera
} 
else if (segunda-condicion-a-evaluar)
{
codigo a ejecutar en caso de que la segunda condicion sea verdadera y la primera sea falsaa
}
else (tercer-condicion-a-evaluar)
{
codigo a ejecutar si la primer y segunda condicion son falsas}
```
Al momento de ingresar a la estructura, el programa evalúa si la condición es verdadera o falsa, en caso de ser verdadera el, programa ejecutará el código dentro de las llaves, en caso de que no sea verdadero no se ejecutará.

#### Operador ternario

El operador ternario, nos permite realizar una evaluación de una expresión (puedes pensarlo como una forma más corta de escribir un **if**.

La estructura de un operador ternario es la siguiente:

