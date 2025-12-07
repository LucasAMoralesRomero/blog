---
layout: post
title:  "Un Emoji como Favicon 🤔❔"
date:   2025-11-25 09:24:05 -0300
categories: HTML
---

#### Buenas tardes y bienvenido a un nuevo post, donde veremos una curiosa (aunque muy util) forma de poner un Favicon a una página web

Si has dado una vuelta por el blog, seguramente te has percatado de que no posee un icono y, que solo se muestra uno genérico.

![El blog sin Favicon]({{site.baseurl }}/resources/html-emoji-favicon/blog-no-icon.jpg)

Esto, que tal vez algunas personas ven como algo trivial es algo sumamente importante de cara al visitante nuestra web, ya que ayuda a que nos distinga entre todas las paginas que ve al navegar.

Si bien lo ideal es usar un **archivo .ico**, tambien podemos usar un modesto **emoji** como archivo **Favicon**.

Para este ejemplo, trabajaremos con esta breve historia basada en el **"Capitán Proton"**:

![La historia sin el favicon]({{site.baseurl }}/resources/html-emoji-favicon/capitan-proton-no-icon.jpg)

Si bien se ve bien, hay algo que nos hace ruido, algo falta... algo como el **Favicon**, asi que manos al código.

Si vemos el **código HTML** a continuación, notaremos que falta el enlace en el **header** para mostrar el icono

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Capitan Proton y la sobra del espacio perdido</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>

 <header>
    <h1>Capitán Proton y la Sombra del Espacio Perdido 🚀</h1>
  </header>

  <main>
    <p>Entre relámpagos cósmicos y un zumbido que hacía temblar las estrellas, el <strong>Rocket Ship</strong> del intrépido <strong>Capitán Proton</strong> emergió del espacio. Los indicadores centelleaban en rojo, y el <strong>humo eléctrico de sus cohetes</strong> llenaba la cabina. A su lado, el inseparable <strong>Buster Kincaid</strong> limpiaba el sudor de su frente con un pañuelo grasiento. “Capitán, esa señal… no es de esta galaxia”, dijo con voz temblorosa. Proton, con la mandíbula firme y la mirada perdida en el infinito, respondió: “Entonces, Buster, acabamos de cruzar la frontera del conocimiento humano”.</p>
```
Ahora, podemos usar este **tag** para poder utilizar un **emoji** como **favicon**:

```html
<link rel="icon" href="data:image/svg+xml,<svg xmlns=%22http://www.w3.org/2000/svg%22 viewBox=%220 0 100 100%22><text y=%22.9em%22 font-size=%2290%22>😊</text></svg>">
```
>
> 🛈 **Recuerda que justo antes del tag `</text></svg>` debemos de poner el emoji que quisieramos usar**
>

Ahora, ¿dónde colocamos el **tag**?, bueno, lo pondremos justo entre medio de los **tags** **title** y **link**, como se ve a continuación:

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Capitan Proton y la sobra del espacio perdido</title>
    <link rel="icon" href="data:image/svg+xml,<svg xmlns=%22http://www.w3.org/2000/svg%22 viewBox=%220 0 100 100%22><text y=%22.9em%22 font-size=%2290%22>🚀</text></svg>">
    <link rel="stylesheet" href="styles.css">
</head>
<body>

 <header>
    <h1>Capitán Proton y la Sombra del Espacio Perdido 🚀</h1>
  </header>

  <main>
    <p>Entre relámpagos cósmicos y un zumbido que hacía temblar las estrellas, el <strong>Rocket Ship</strong> del intrépido <strong>Capitán Proton</strong> emergió del espacio. Los indicadores centelleaban en rojo, y el <strong>humo eléctrico de sus cohetes</strong> llenaba la cabina. A su lado, el inseparable <strong>Buster Kincaid</strong> limpiaba el sudor de su frente con un pañuelo grasiento. “Capitán, esa señal… no es de esta galaxia”, dijo con voz temblorosa. Proton, con la mandíbula firme y la mirada perdida en el infinito, respondió: “Entonces, Buster, acabamos de cruzar la frontera del conocimiento humano”.</p>
```

Tras agregar ese **tag**, podremos ver que nuestra web se ve mucho mejor:

![La historia con el favicon]({{site.baseurl }}/resources/html-emoji-favicon/capitan-proton-with-icon.jpg)

Y así como el Capitán Proton necesita de su confiable compañero **Buster Kincaid** para triunfar, tu web también puede brillar con algo tan modesto como un **emoji**.

Un detalle que parece mínimo, pero que marca la diferencia.

¡Nos vemos en el próximo post!


> 🛈 **Aviso de Propiedad Intelectual**  
> *Capitán Proton* y *Buster Kincaid* son personajes pertenecientes a **Star Trek: Voyager**, propiedad de CBS Studios / Paramount Global.  
> Este artículo utiliza dichos nombres solo con fines demostrativos.

