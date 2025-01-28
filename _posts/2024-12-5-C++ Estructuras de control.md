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

```cpp
variable = (conficion) ?
valor-si-es-verdadero :
valor-si-es-falso;
```

tal vez resulte un poco difícil de entender, pero es bastante simple. Utilizamos una variable que comparamos y tenemos dos posibles salidas. Un ejemplo simple sería saber si aprobamos o no una materia:

```cpp
#include <iostream>
using namespace std;

int main()
{
    int notas = 7 + 5 + 9;
notas = notas / 3;
//veamos si aprobamos

cout << ((notas >= 7) ?
"Aprobado\n" : "Desaprobado\n");

    return 0;
}
```
### Bucles
Los `bucles` nos permiten ejecutar tantas veces como sea necesario una porcion de codigo, siempre y cuando una condicion se cumpla.

#### Bucle While
Llegamos a uno de nuestros "mejores amigos", el buen bucle while, este nos permite ejecutar el codigo que encerremos dentro mientras la consicion sea verdadera.
 Seguramente te estes preguntando por que es nuestro mejor amigo, bueno eso se debe a que 
 usaremos este bucle para crear el `game loop` (el bucle donde alojaremos la logica del juego y el que usaremos para salir del mismo)
 
 La estructura basica del while es la siguiente:

 ```cpp
 while ( condicion )
    {
        codigo-a-ejecutar;
    }
 ```

Ejemplo: Contador simple
```cpp
#include <iostream>
using namespace std;

int main() {
    int contador = 1;

    while (contador <= 5) {
        cout << "Iteración: " << contador << endl;
        contador++;
    }

    return 0;
}
```


En este caso:

1. El programa empieza con la variable contador igual a 1.


2. Mientras la condición contador <= 5 sea verdadera, se ejecuta el código dentro del bloque.


3. En cada iteración, se incrementa el valor de contador con contador++.
