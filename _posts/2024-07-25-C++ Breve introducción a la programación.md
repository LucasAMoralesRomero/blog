---
layout: post
title:  "C++: Breve introducción a la programación"
date:   2024-05-07 09:24:05 -0300
categories: cpp
---


## Parte I: introducción e instalación de herramientas
Buenos días y, bienvenidos a esta breve introducción a la programación en C++, en esta serie de artículos, veremos el proceso de instalación del entorno de desarrollo, los puntos claves del lenguaje y, finalmente, desarrollaremos un juego donde aplicaremos lo aprendido.


Pero, primero, ¿por qué aprender C++?, la respuesta a esta pregunta es que este lenguaje, aunque es un poco difícil de aprender al principio es uno de los lenguajes más utilizados en la industria del videojuego, es muy eficiente y es altamente portable.¹


#### Instalación del entorno de desarrollo
Para esta serie de tutoriales, utilizaremos el [IDE de Microsoft Visual Studio][IDE-VS], el mismo posee una versión gratuita (la versión Community).
Al ingresar a la web, iniciaremos la descarga del entorno de desarrollo y, una vez descargado, iniciaremos el instalador.
Una vez que se inicie, marcaremos la casilla de desarrollo para escritorio con C++, como se ve en la siguiente imagen:


![Instalación del entorno de desarrollo]({{ site.url }}{{site.baseurl }}/resources/cpp-clase-1/instalador.png)


Luego, pulsaremos en instalar y dejaremos al instalador hacer su trabajo, esto va a demorar un rato por lo que es recomendable dejar la PC libre (aprovecha el tiempo para tomar una buena taza de café)


![Instalación en progreso]({{ site.url }}{{site.baseurl }}/resources/cpp-clase-1/instalador-en-progreso.png)


#### Nuestro primer programa en C++
Una vez que el instalador haya finalizado, es hora de que escribamos nuestro primer programa en C++, el famoso "Hola Mundo!", para eso vamos a abrir Visual Studio y seleccionaremos Crear un nuevo proyecto.


![Seleccionamos un nuevo proyecto]({{ site.url }}{{site.baseurl }}/resources/cpp-clase-1/nuevo-proyecto.jpg)


Luego, selecciona aplicación de consola y presiona en siguiente.


![Seleccionamos proyecto de consola]({{ site.url }}{{site.baseurl }}/resources/cpp-clase-1/plantilla-consola.jpg)


Finalmente, le damos un nombre al proyecto y presionamos el botón crear.
![Asignamos un nombre al proyecto]({{ site.url }}{{site.baseurl }}/resources/cpp-clase-1/nombre-proyecto.jpg)


Una vez que se abra el editor, borra el contenido del archivo que aparece y pega el siguiente código:


{% highlight cpp %}
#include <iostream>


int main() {
    std::cout << "Hola, mundo!" << std::endl;
    return 0;
}
{% endhighlight %}


#### Analicemos el código:


Ahora, vamos a desglosar el código línea por línea para entender qué hace cada parte:


{%highlight cpp%}
#include <iostream>
{% endhighlight %}
Con la palabra reservada `include` le indicamos al compilador que vamos a usar la biblioteca `iostream`, tal vez te preguntes que es una biblioteca, una biblioteca es un conjunto de herramientas que fueron creadas para ayudarnos a crear nuestros programas, en este caso con esta biblioteca vamos a poder escribir en pantalla.


{%highlight cpp%}
int main()
{% endhighlight %}
Esta línea define la función principal del programa, cada programa en C++ debe tener una función main. La palabra int indica que al finalizar la ejecución del código está devolverá un valor entero, de esto vamos a hablar un poquito más adelante en el post.


{%highlight cpp%}
{
{% endhighlight %}
La llave de apertura `{` marca el inicio del bloque de código de la función main, este elemento junto con la llave de cierre `}` le indica al compilador que en ese código pertenece a la función `main`.


{%highlight cpp%}
std::cout << "Hola, mundo!" << std::endl;
{% endhighlight %}
Aquí hacemos uso del objeto `std::cout` para imprimir por pantalla el mensaje "Hola, mundo!"; luego, mediante el uso de la función `std::endl` indicamos que debe realizar un salto de línea. También podrás apreciar, que al final de la instrucción se ve el símbolo de punto y coma, que se usa para indicar que finaliza la instrucción.


{%highlight cpp%}
return 0;
{% endhighlight %}
Esta línea indica que el programa ha terminado con éxito. El 0 es un código de salida que significa que no hubo errores.


{%highlight cpp%}
}
{% endhighlight %}
La llave de cierre `}`, como dijimos anteriormente marca el final del bloque de código de la función main.




#### Ejecutar el Programa:


Una vez que pegues el código, presiona "Iniciar". Deberías ver una ventana de consola que muestra el mensaje "Hola, mundo!".


![Ejecutamos el codigo]({{ site.url }}{{site.baseurl }}/resources/cpp-clase-1/ejecutar_codigo.gif)


#### Conclusión:
¡Felicitaciones!, escribiste y ejecutaste el primer  programa en C++, tal vez parezca poco, pero con este pequeño ejercicio probamos que nuestro IDE funcione y entendimos (a grandes rasgos) cómo funciona el código.
A medida que avancemos en esta serie de tutoriales, veremos tipos de datos, estructuras de control e iremos construyendo con estos mini-proyectos para afianzar el conocimiento para, finalmente crear un juego que se ejecute en consola usando todo lo aprendido.


¹Vallejo, D., & Martín, C. (2015, January 1). Capítulo 3 :: C++. Aspectos Esenciales. In Desarrollo de Videojuegos: Un Enfoque Práctico. Vol 1: Arquitectura del Motor (p. 68). Cursos en Español. http://books.google.ie/books?id=nT0aEAAAQBAJ&pg=PP4&dq=978-1517309558&hl=&cd=1&source=gbs_api

[IDE-VS]: https://visualstudio.microsoft.com/es/vs/community/