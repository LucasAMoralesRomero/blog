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

 Continuemos con los bucles y luego pasemos al mini proyecto para cerrar el post.

## Bucle do-while 

El bucle do-while es similar al while, pero garantiza que el código dentro del bloque se ejecute al menos una vez, incluso si la condición inicial no se cumple.

Estructura básica del do-while:

```cpp
do 
{ // Código a ejecutar al menos una vez } 
while (condicion); 

```

Ejemplo: Solicitar un número positivo

```cpp


#include <iostream> 
using namespace std; 
int main() { 
int numero; 
do 
{ cout << "Ingresa un número mayor a 0: "; cin >> numero; } 
while (numero <= 0); 
cout << "¡Número válido ingresado: " << numero << "!" << endl; return 0; } 

```

En este caso:

El programa siempre pedirá al usuario ingresar un número al menos una vez. Si el número ingresado es menor o igual a 0, el bucle se repetirá hasta que se ingrese un valor válido. 

## Bucle for 

El bucle for es ideal cuando sabemos de antemano cuántas veces queremos que se ejecute un bloque de código. Es comúnmente usado para recorrer rangos o colecciones.

Estructura básica del for:
```cpp
for (inicialización; condición; incremento) 
{ // Código a ejecutar mientras la condición sea verdadera } 
```

Ejemplo: Imprimir los primeros 10 números

```cpp
#include <iostream> 
using namespace std; 
int main() { 
for (int i = 1; i <= 10; i++) 
{ cout << "Número: " << i << endl; } 
return 0; } 
```

En este caso:

Inicialización: int i = 1 establece el valor inicial de la variable i. Condición: i <= 10 verifica si el bucle debe continuar. Incremento: i++ incrementa el valor de i después de cada iteración. 

## break y continue 

A veces necesitamos interrumpir un bucle o saltar a la siguiente iteración antes de que termine el bloque completo.

break: Detiene el bucle inmediatamente y sale de él. continue: Salta al final del bucle y comienza la siguiente iteración. 

Ejemplo con break:

#include <iostream> using namespace std; int main() { for (int i = 1; i <= 10; i++) { if (i == 5) { cout << "Se detiene en el número: " << i << endl; break; } cout << "Número: " << i << endl; } return 0; } 

Ejemplo con continue:

#include <iostream> using namespace std; int main() { for (int i = 1; i <= 10; i++) { if (i % 2 == 0) { continue; // Salta los números pares } cout << "Número impar: " << i << endl; } return 0; } 

## Mini Proyecto: Juego de Adivina el Número 

En este mini proyecto, pondremos en práctica las condicionales y los bucles que hemos aprendido. El programa generará un número aleatorio entre 1 y 100, y el jugador tendrá un número limitado de intentos para adivinarlo.

¿Qué queremos lograr?

Generar un número aleatorio entre 1 y 100. Permitir al jugador adivinar con un máximo de 5 intentos. Dar pistas indicando si el número es "mayor" o "menor" al intento. Mostrar un mensaje final indicando si ganó o perdió. 
