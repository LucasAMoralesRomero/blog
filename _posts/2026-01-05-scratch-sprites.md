---
layout: post
title: "CC101 - Programacion con Scratch - Parte 1: Sprites"
date: 2026-01-05 09:24:05 -0300
categories: scratch
youtubeId: 3ZRCnEmdP90
youtubeId2: jv0GdpUEPT0
---

>**Nota:**
>Este material es una traducción adaptada del primer capítulo del curso CS50S: Introduction to Programming with Scratch de Harvard.
>Se han agregado explicaciones, ejemplos y recursos visuales para facilitar su comprensión a estudiantes de nivel secundario.
 
# Sprites

## Introducción
---------
<br>
Scratch es un entorno de programación visual basado en bloques, originalmente desarrollado por un equipo del  [MIT´s Media Lab][MIT-Media-Lab] y, actualmente mantenido por la [Scratch Foundation][Scratch-Foundation]. 

Al combinar los bloques de código, podemos crear historias visuales, animaciones, juegos y otros programas.

Aprenderemos y usaremos conceptos de programación como **funciones**, **bucles**, **condicionales** y **variables**.

Aunque Scratch utiliza bloques visuales en lugar de código escrito, los programas que desarrollaremos están basados en las mismas ideas fundamentales y utiliza los mismos principios del [pensamiento computacional][Pensamiento-Computacional].

## Conceptos básicos de la interfaz Scratch
---------
<br>
Podemos dirigirnos al [sitio web de Scratch][Sitio-Web-Scratch] y veremos una interfaz como la siguiente:
![Interfaz de Scratch]({{site.baseurl }}/resources/cc101-scratch-01/scratch-interfaz.webp)

En la parte izquierda tenemos la **biblioteca de bloques**, desde donde podemos seleccionar cualquier combinación de ítems hacia el área central, que es el **área de programación**.
En la parte superior derecha, tenemos el **escenario**, donde se ejecuta nuestro proyecto.

## Sprites
---------
<br>

### Denominación y posicionamiento
Cuando creamos un proyecto nuevo, vemos un **sprite** con la imagen del gato que es la mascota de Scratch. 
Un **sprite** es cualquier objeto que podemos mostrar en el escenario.

Debajo del **escenario**, vemos todos los **sprites** que están en nuestro proyecto, por el momento solo tenemos uno llamado 
`Sprite1`.

Podemos mover el **sprite** por el **escenario**, haciendo click con el mouse y arrastrándolo a la posición deseada.
A medida que lo trasladamos en el escenario podemos observar las coordenadas `X` e `Y` que van cambiando.
En la imagen, podemos ver que nuestro **sprite** se encuentra en la posición `X: 15` e `Y: 90`. 

![Coordenadas del sprite]({{site.baseurl }}/resources/cc101-scratch-01/caja-sprites.webp)

Los **sprites** están ubicados en un sistema de coordenadas cartesianas, donde el valor `X` indica qué tan a la derecha o izquierda se encuentra el **sprite** y el valor `Y` nos muestra qué tan arriba o abajo se encuentra. 

El centro del escenario se encuentra en la posición `X: 0` e `Y: 0`, los valores positivos x se encuentran a la derecha del centro, y los negativos a la izquierda, similarmente, los valores positivos de `Y` están arriba del centro y los negativos abajo.
En la imagen, podemos ver más claramente el sistema de coordenadas.
![Sistema de coordenadas]({{site.baseurl }}/resources/cc101-scratch-01/scratch-ejes-cartesianos.webp)

Por ahora, lo movemos manualmente, pero más adelante aprenderemos a mover los **sprites** con bloques.

También podemos cambiar las coordenadas directamente escribiendo los valores en las cajas de `X` e `Y`.

Además, podemos **mostrar** u **ocultar** el **sprite** haciendo click en el icono del ojo, también podemos cambiar el tamaño (mostrado en porcentaje) y rotarlo en grados haciendo click en la caja de **Dirección**, como se muestra en la imagen.

![Opciones del sprite]({{site.baseurl }}/resources/cc101-scratch-01/scratch-direccion.webp)

Al hacer click en la caja de **Dirección**, podemos modificar la rotación y ver en tiempo real como se va rotando, así como se ve en el siguiente GIF:

![Rotación del sprite]({{site.baseurl }}/resources/cc101-scratch-01/scratch-rotacion.gif)

<br>

### Agregar nuevos sprites
Agreguemos un nuevo **sprite**. Si hacemos click en el icono del Gato con un signo de suma en el fondo del **área de sprites**, también veremos otras opciones, como se ve en la siguiente imagen:


![Elegir un sprite]({{site.baseurl }}/resources/cc101-scratch-01/scratch-agregar-sprite.webp)

Por ahora, usaremos la opción `Agregar un objeto`, y si pulsamos veremos una lista con todos los **sprites** que vienen por defecto en la biblioteca de **Scratch**.

En la biblioteca podemos buscar el **sprite** que queramos usar mediante la caja de búsqueda (que se encuentra en la parte superior izquierda) o recorrer las clases de objetos.

Para seguir, elegiremos el **sprite** del pez, y, veremos que ambos están ahora en el **escenario**, podemos moverlos para que no se solapen.
![gregar sprite y moverlo]({{site.baseurl }}/resources/cc101-scratch-01/scratch-mover-sprites.gif)

Ahora, en el **área de sprites**, podemos ver ambos **sprites**, resaltado en color violeta podemos ver el **sprite** con el que estamos trabajando, al cual le podemos modificar la posición, el tamaño y la dirección por ejemplo.

Ahora, si haces click derecho sobre el **sprite** del pez podemos desplegar el menú de las opciones. Podemos presionar el botón "duplicar" y ahora tenemos dos peces:

![Duplicar sprite]({{site.baseurl }}/resources/cc101-scratch-01/scratch-duplicar-sprite.gif)

A continuación encontrarán el proyecto de Scratch con los dos **sprites** que hemos creado: [proyecto sprites][Proyecto-sprites] 

### Disfraces

Cada **sprite** puede tener varios **disfraces**, que son las diferentes apariencias que puede tener un **sprite**, que es una imagen de como se debe ver el **sprite** en el escenario.

En la parte superior izquierda, veremos una pestaña llamada **Disfraces**

![Pestaña disfraces]({{site.baseurl }}/resources/cc101-scratch-01/scratch-disfraces.webp)

Podemos ver que nuestro pez tiene cuatro **disfraces** diferentes, y podemos seleccionar cualquiera de ellos para aplicárselo a nuestro pez.

En el caso del gato, posee dos **disfraces**, los cuales podemos usar para dar la sensación de que el gato "camina" (lo cual veremos más adelante).

En la sección de **disfraces** , podemos editar los que están presentes o pintar uno nuevo usando las herramientas de dibujo.

También podemos subir un **disfraz** desde nuestro equipo, como se ve en el ejemplo:

{% include youtubePlayer.html id=page.youtubeId %}

<br>

A continuación encontrarán el proyecto de Scratch con los dos **sprites** que hemos creado: [proyecto disfraces][Proyecto-disfrtaces]

### Sonidos

Cada **sprite** puede tener asociado uno o varios sonidos, que podemos agregar desde la pestaña **sonidos**:

![Pestaña sonidos]({{site.baseurl }}/resources/cc101-scratch-01/scratch-sonidos.webp)

Podemos ver que nuestro pez tiene dos sonidos: "bubbles" (un sonido de burbujas) y "ocean wave" (un sonido de olas del mar), y si seleccionamos el **sprite** del gato, veremos que tiene un sonido llamado "meow" (un maullido).

Podemos cambiar, eliminar o agregar nuevos sonidos desde la **biblioteca de sonidos** de Scratch o, grabar uno nuevo usando el micrófono de la computadora.

## Fondos
---------
<br>
Nuestro escenario tiene un fondo blanco por defecto, pero podemos cambiarlo haciendo click en el icono con la imagen del paisaje con un signo de suma

![Agregar fondo]({{site.baseurl }}/resources/cc101-scratch-01/scratch-agregar-fondo.webp)

Ahora, veremos un montón de fondos disponibles para usar en la **biblioteca de fondos** de Scratch.
Tomemos el fondo llamado "underwater" (bajo el agua) para ambientar la escena.

Ahora, nuestro gato no combina con el fondo, así que podemos seleccionar el **sprite** del gato y presionar en el icono de la papelera para eliminarlo.

Ahora, para darle un toque más lindo a la escena, voltearemos el **sprite** del pez utilizando el ítem "dirección" que se encuentra junto a las coordenadas `X` e `Y`, y cambiaremos el valor a `180`, para que mire hacia la izquierda (pero, recuerda presionar el botón del medio para bloquear el cambio solo sobre el eje horizontal) tal como se muestra en el ejemplo:

{% include youtubePlayer.html id=page.youtubeId2 %}

A continuación encontrarán el proyecto de **Scratch** con el fondo y el pez volteado: [proyecto de fondos][Proyecto-fondos]

## Guardar el proyecto
---------
<br>
Para guardar nuestro proyecto para poder seguir trabajando mas tarde, podemos pulsar el botón "Archivo" en la parte superior y pulsar el ítem "Guardar en tu computador", como se ve en la siguiente imagen:

![Guardar proyecto]({{site.baseurl }}/resources/cc101-scratch-01/scratch-guardar-computadora.webp)

Esto descargará un archivo con extensión `.sb3` en nuestra computadora, el cual podremos abrir más tarde desde el mismo menú "Archivo" seleccionando el ítem "Load from your computer" (Cargar desde tu computadora).

También podemos crear una cuenta en el sitio web usando el botón "Únete a Scratch" en la parte superior derecha, esto nos permitirá guardar nuestro proyecto en la página y compartirlo con otras personas.

## En el siguiente capítulo
---------
<br>
En el próximo capítulo, comenzaremos a usar bloques para hacer que nuestros **sprites** realicen diferentes acciones, e incluso crear historias interactivas y juegos basados en los inputs de los usuarios.

>Fuente original:
>[CS50’s Introduction to Programming with Scratch — Lecture 1: Sprites][Scratch-Lecture-1]


[MIT-Media-Lab]: https://www.media.mit.edu/about/overview/
[Scratch-Foundation]: https://scratch.mit.edu/credits
[Pensamiento-Computacional]: https://es.wikipedia.org/wiki/Pensamiento_computacional

[Sitio-Web-Scratch]: https://scratch.mit.edu/projects/editor/

[Proyecto-sprites]: https://scratch.mit.edu/projects/1263270519/

[Proyecto-disfrtaces]: https://scratch.mit.edu/projects/1263267017/

[Proyecto-fondos]: https://scratch.mit.edu/projects/1263731585/

[Scratch-Lecture-1]: https://cs50.harvard.edu/scratch/notes/1/