---
layout: post
title:  "C++: Breve introducción a la programación - Parte 2: Tipos de datos"
date:   2024-11-25 09:24:05 -0300
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
Las variables pueden ser de varios tipos, como enteros, números no enteros (flotantes), caracteres o booleanos, veamoslas con algunos ejemplos:

### Tipos de datos

#### Enteros:

Los enteros, Los utilizaremos para almacenar números enteros, podemos hacer que estos enteros sean con o sin signo negativo, o que sean pequeños o grandes, esto nos permite ahorrar espacio en memoria, veamos un cuadro con los valores y, luego lo aplicaremos en el IDE:

|Tipo de dato|Rango de números que puede almacenar|Tamaño en memoria|
|------------|------------------------------------|-----------------|
|short int   |-32767 a 32767                      |16 bits (2 bytes)|
|unsigned short int|0 a 65535                     |16 bits (2 bytes)|
|int         |            -2147483647 a 2147483647|32 bits (4 bytes)|
|unsigned int|0 a 4294967295                      |32 bits (4 bytes)|
|long int    |            -2147483647 a 2147483647|32 bits (4 bytes)|
|unsigned long int|0 a 4294967295                 |32 bits (4 bytes)|

Estos tipos de datos, aunque parecidos son diferentes, pero, ¿por que? ¡porque cada uno se puede usar para distintos casos!

**Short int** puede utilizarse para almacenar números que seran positivos o negativos, pero que no seran muy grandes, como por ejemeplo la temperatura medida por un sensor de temperatura, mientras que **unsigned short int** puede ser utilizado para valores que no seran negativos, como por ejemplo los dias del año, la edad de una persona.

**Int** se puede utilizar para valores positivos o negativos que sean moderadamente grandes, como el balance de la cuenta de una persona, mientras que **unsigned int** puede utilizarse para valores que sean positivos y moderadamente grandes, como la distancia recorrida cuando andamos en bicicleta o la cantidad de puntos que hagamos en un juego.

**Long int** se puede utilizar para números muy grandes, como por ejemplo el balance de una empresa o las deudas de un pais, mientras que **unsigned long int** se utiliza para almacenar datos muy grandes, pero que no pueden ser negativos, como las estrellas en la galaxia.

#### Números no enteros:

Los números no enteros, o flotantes son los números que poseen una parte fraccional (como por ejemplo el peso de una porcion de queso), existen dos tipos los **float** y los **double**, ¿la diferencia entre ellos? ¡la presición!, por ejemplo con **float** podemos almacenar la altura de un edificio o la temperatura en el interior de una casa.
**Double** posee una mayor presición, lo podemos usar para almacenar calculos financieros, o la distancia recorrida por una sonda espacial

| Tipo de dato |            Rango de números que puede almacenar                 | Tamaño en memoria |
|--------------|-----------------------------------------------------------------|-------------------|
| float        | Aproximadamente 1.2 × 10<sup>-38</sup> a 3.4 × 10<sup>38</sup>  | 32 bits (4 bytes) |
| double       | Aproximadamente 2.2 × 10<sup>-308</sup> a 1.7 × 10<sup>308</sup>| 64 bits (8 bytes) |

#### Caracteres (char):

Los **caracteres** almacenan dentro de una variable un caracter de la tabla ASCII, en memoria va a ocupar un byte, por lo que va a poder almacenar una letra, un numero o un símbolo.

#### Booleanos:

Los **booleanos** almacenan dos valores `verdadero` o `falso`, lo utilizaremos com banderas para poder controlar el flujo de nuestro programa, puedes imaginarlo como un interruptor, si se establece en `0` o `false` podemos hacer que una parte de nuestro codigo no se ejecute, en cambio si lo establecemos en `1` o en `true` esa porción de código si se ejecutará.

veamos un ejemplo para demostrarlo:

```cpp
//creamos un booleano llamado caminar
bool caminata;

//lo establecemos en verdadero
caminata = true;

//si caminar es verdadero, mostramos en pantalla que podemos salir a caminar, sino mostramos que no
if (caminata == true) {
    cout << "Vamos a salir a caminar, yeah!"
}
else {
    cout << "No vamos a salir a caminar =("
}

```
### Operadores

Llegamos a la ultima parte de este articulo (lo se, se hizo un poco mas complejo este articulo, pero creeme que valdra la pena para establecer un buen cimiento para los proximos articulos). Dicho lo anterior, avancemos! =D

En C++, los `operadores` nos permiten, como dice la palabra realizar operaciones con las variables de nuestro programa; podemos realizar calculos matemáticos, comparar valores o combinar condiciones.

Veamos los mas importantes **operadores aritméticos, operadores de comparacón y operadores lógicos**.

#### Operadores aritméticos:

Los `operadores aritméticos` son aquellos que nos permiten realizar calculos matemáticos como la **suma, resta, multiplicación, división y módulo (o resto)**


|Operador    |Descripción                         |Ejemplo de uso (x = 5, y = 4)       |
|------------|------------------------------------|------------------------------------|
|      +     |                Suma                |x + y // la salida sera:  5 + 4 = 9 |
|      -     |                Resta               |x - y // la salida sera: 5 - 4 = 1  |
|      *     |                Multiplicación      |x * y // la salida sera: 5 * 4 = 20 |
|      /     |          División entera           |x / y // la salida sera: 5 / 4 = 1  |
|      %     |                Módulo (o resto)    |x % y // la salida sera: 5 % 4 = 1  |

Tal vez sea un poco trivial explicar todo el cuadro, pero, nos centraremos en los ultimos dos operadores que nos dio el mismo resultado, pero ¿por que?

Eso se debe a que el primer operador, el de división entera nos devuelve el rsultado de la division entera, en este caso 5 dividido 4 es uno. Ahora, el operador de módulo nos devuelve el resto de la division, en este caso 5 dividido 4 nos da uno, y nos queda 1 de resto.

#### Operadores de asignación

Los `operadores de asignación` nos permiten guardar un valor en una variable, el mas comun de ellos es el de igualdad `=`, el que ya vimos anteriormente para almacenar un valor, pero tenemos otros que nos permiten realizar una operacion matematica y luego guardarlo, veamoslo en un cuadro:

|Operador    |Descripción                         |Ejemplo de uso (x = 5)              |
|------------|------------------------------------|------------------------------------|
|      =     |      Asignación simple             |x = 5 // la salida sera:  5         |
|      +=    |      Suma y asigación              |x += 1 // la salida sera:  6        |
|      -=    |      Resta y asignación            |x -= 1 // la salida sera:  4        |
|      *=    |      Multiplicación y asignación   |x *= 2 // la salida sera:  10       |
|      /=    |      División y asignación         |x /= 2 // la salida sera:  2        |
|      %=    |      Módulo y asignación           |x %= 4 // la salida sera:  1        |

#### Operadores lógicos

Los `operadores lógicos` son utilizados para comprobar si una variable es verdadera o falsa, con ellos podemos comparar una o multiples variables, veamoslos mas a detalle:

**Operador && (and)**

El operador and, nos permite evaluar dos variables, y en caso de que ambas sean verdaderas, nos da true, si una de ellas es falsa o si ambas lo son, nos dara falso.
Veamoslo con un ejemplo:

```cpp

//creamos un booleano, llamada dia
bool dia;
//creamnos un booleano llamado zapatillas
bool zapatillas;

//establecemos en verdadero el dia 
dia = true;

//hacemos lo mismo con zapatillas
zapatillas = true;



//si es de dia y tenemos zapatillas podemos salir a caminar, sino no
if (dia == true && zapatillas == true) {
    cout << "Salgamos a camiran en este hermoso dia =)"
}
else {
    cout << "Si no es de dia y no tenemos zapatillas no podremos salir a caminar =("
}

```

**Operador &#124;&#124; (or)**

El operador or al igual que el and nos permite evaluar dos variables, pero en este caso sera verdadero siempre que una de las dos condiciones sea verdadera, en caso de que ambas sean falsas nos dara falso:

```cpp
//crearemos un booleano llamado tarea
bool tarea;

//crearemos un booleano llamado permiso de salir
bool permisoDeSalir;

//tareas sera falso (porque no las hiciste)
tareas = false;

//permisoDeSalir sera verdadero porque tus padres te dieron permiso para salir hot
permisoDeSalir = true;

//ahora con un if y un OR evaluamos si tareas es erdadero o si permisoDeSalir lo es (cono uno de los dos es verdadero, podreas salir!) 

if (tarea == true || permisoDeSalir == true) {
    cout << "Puedes salir con tus amigos! =D" << endl;
} else {
    cout << "No puedes salir hasta que termines la tarea o te den permiso." << endl;
}

```

**Operador ! (not)**

El operador not nos sirve para invertir un valor, o para evaluar hasta que algo no sea verdad, este operador logico sera nuestro mejor amigo a la hora de evaluar los bucles en los juegos que hagamos, pero no nos adelantemos y vemos un pequeño ejemplo:

```cpp
//creamos un booleano llamado cinturón puesto
bool cinturonPuesto;

//establecemos en false porque el conducto no se puso el cinturon
cinturonPuesto = false;

//evaluamos si el conductor se puso el cinturon, si se lo puso nos vamos, sino no salimos

if (!cinturonPuesto) {
    cout << "¡Si no te pones el cinturón no podes manejar!" << endl;
} else {
    cout << "¡Bien! Te pusiste el cinturón, ¿a donde vamos?" << endl;
}

```

### Proyecto del dia: Piedra, papel o Tijeras

Llegamos al final del artículo, y para poner en práctica lo visto hoy, haremos un mini proyecto: un juego de Piedra, Papel o Tijeras.

En el juego, elegiremos uno de los tres elementos (Piedra, Papel o Tijeras), y acto seguido, el programa seleccionará una opción de forma aleatoria.

Finalmente, el programa comparará las elecciones y nos indicará si hay un ganador o si el resultado es un empate.

¡Manos a la obra!



```cpp
#include <iostream>
#include <cstdlib> // Para rand() y srand()
#include <ctime>   // Para time()
using namespace std;

int main() {
	// Declaramos las variables
	int eleccionJugador;
	int eleccionComputadora;
	
	// Mostramos las opciones al jugador
	cout << "Elige una opcion: " << endl;
	cout << "1. Piedra" << endl;
	cout << "2. Papel" << endl;
	cout << "3. Tijeras" << endl;
	cout << "Ingresa el numero de tu eleccion: ";
	cin >> eleccionJugador;
	
	//Mostramos lo que eligio el jugador
	cout << "Elegiste: ";
	if (eleccionJugador == 1) {
		cout << "Piedra" << endl;
	} else if (eleccionJugador == 2) {
		cout << "Papel" << endl;
	} else {
		cout << "Tijeras" << endl;
	}
	
	// Generamos una eleccion aleatoria para la computadora
	srand(time(0)); // Semilla para generar numeros aleatorios
	eleccionComputadora = rand() % 3 + 1; // Genera un numero entre 1 y 3
	
	// Mostramos la eleccion de la computadora
	cout << "La computadora eligio: ";
	if (eleccionComputadora == 1) {
		cout << "Piedra" << endl;
	} else if (eleccionComputadora == 2) {
		cout << "Papel" << endl;
	} else {
		cout << "Tijeras" << endl;
	}
	
	// Comparamos las elecciones y determinamos el resultado
	if (eleccionJugador == eleccionComputadora) {
		cout << "Es un empate!" << endl;
	} else if ((eleccionJugador == 1 && eleccionComputadora == 3) || 
		(eleccionJugador == 2 && eleccionComputadora == 1) || 
		(eleccionJugador == 3 && eleccionComputadora == 2)) {
		cout << "Ganaste!" << endl;
	} else {
			cout << "Perdiste. La computadora gana." << endl;
		}
		
		return 0;
}
```

¿Demasiado código para esta altura del post, verdad? :) No te preocupes, analicemos juntos este juego paso a paso.

Al inicio del programa, importamos dos bibliotecas importantes:

* ctime: La utilizamos para obtener el tiempo actual de la computadora, que sirve como semilla para generar números "aleatorios".
* cstdlib: Incluye las funciones `srand()` y `rand()`, que nos permiten inicializar el generador de números aleatorios y generar valores diferentes cada vez que ejecutamos el programa.

Luego declaramos dos variables:

* eleccionJugador: Donde almacenaremos la elección del jugador.
* eleccionComputadora: Que guardará la elección generada por el programa.

A continuación, presentamos un menú básico con las opciones disponibles usando cout. Después, con cin, guardamos la elección 
del jugador y mostramos su selección en la consola.

Acto seguido, inicializamos la semilla de números aleatorios con srand(time(0)) y usamos rand() para generar un número aleatorio entre 1 y 3. 
Este número se guarda en eleccionComputadora, y mostramos su elección en la consola, igual que hicimos con el jugador.

Finalmente, con una estructura if anidada, comparamos las elecciones y mostramos el resultado: si hay un ganador o si el juego terminó en empate.

# Conclusión
Fue largo el articulo de hoy, pero valio la pena, porque con el vimos los conceptos de **variables**, **tops de datos** y **operadores**, y finalizamos
creadon nuestro primer juego: un Piedra Papel o Tijeras.

En mi [repositorio de GitHub][repo] te dejo el codigo del juego que desarrollamos para que lo descargue y lo modifiquies, y, si gustas puedes hacer una modificacion para mejorarlo, yo con gusto la revisare y la agregare.

En el proximo articulo daremos un  paso mas alla, viendo **estructuras de control** que nos permitiran crear programas mas complejos.

¡Nos vemos en el siguiente post!

[repo]: https://github.com/LucasAMoralesRomero/ejemplos-blog/blob/main/01-piedra-papel-tijera/piedra-papel-tijera.cpp
