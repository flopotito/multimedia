# FLORENCIA UMAÑA
<img src="https://i.imgur.com/8TCDjqY.png" alt="Imagen" width="300"><br><br>
<img src="https://github.com/flopotito/multimedia/blob/main/td/_perform_%202026-11-12%2009-58-03.mp4"/>

#### TALLER MULTIMEDIAL
### UNIDAD 1
*Archivo de pequeños recuerdos, imágenes y cosas que no quiero olvidar.*

---

## Índice
## UNIDAD 1
1. [Semana 1. Primeras huellas](#semana-1-primeras-huellas)
2. [Semana 2. Un lugar para quedarse](#semana-2-un-lugar-para-quedarse)
3. [Semana 3. Ordenar los recuerdos](#semana-3-ordenar-los-recuerdos)
4. [Semana 4. Pequeños cambios](#semana-4-pequeños-cambios)
5. [Semana 8. Página final](#semana-8-página-final)
6. [UNIDAD 2. TOUCHDESIGNER](#unidad-2-touchdesigner)

---
<img src="https://media2.giphy.com/media/0GZP1wAt0oCuO61rlt/giphy.gif" alt="Imagen" width="300"><br><br>
## Semana 1. Primeras huellas

Primer acercamiento a HTML. La idea inicial es construir una página sencilla que pueda funcionar como una presentación personal.

```html
<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<title>Florencia Umaña</title>
</head>

<body>

<h1>Florencia Umaña</h1>

<p>Un pequeño espacio para guardar cosas.</p>

<img src="imagen.jpg" width="300">

</body>
</html>
```

Me gustaría que la página no se sintiera como una presentación formal. Quiero que tenga algo de mí, pero sin tener que explicar demasiado. Fondos con textura, imágenes que estén llenando el fondo. Quiero que sea sutil pero que no sea fome.

---

## Semana 2. Un lugar para quedarse
```
Me interesa que las imágenes tengan espacio para respirar.
Comienzo a experimentar con los fondos, los colores y las tipografías. Busco una estética más tranquila, que permita que las imágenes y el nombre sean los protagonistas.
```
```html
<style>
body {
    background-color: black;
    color: white;
    font-family: Georgia, serif;
    margin: 0;
    text-align: center;
}

h1 {
    font-size: 32px;
    font-weight: normal;
}

img {
    width: 70%;
}
</style>
```

No quiero llenar todo de información. A veces una imagen puede decir más que una descripción.

---

## Semana 3. Ordenar los recuerdos

Comienzo a separar el contenido en distintas páginas para organizar mejor el sitio. Pienso en tres espacios: uno para presentarme, otro para mostrar mis obras y otro para dejar mis datos de contacto.

##Estructura propuesta:

- `index.html` — Inicio.
- `obras.html` — Obras y registros.
- `contacto.html` — Contacto.

Ejemplo de navegación:

```html
<nav>
    <a href="index.html">Inicio</a>
    <a href="obras.html">Obras</a>
    <a href="contacto.html">Contacto</a>
</nav>
```

Me gusta pensar que cada página es como una pequeña habitación. No todas tienen que guardar las mismas cosas.

---

## Semana 4. Pequeños cambios

Estoy buscando una manera de que la página se sienta más como un espacio que como un catálogo

Empiezo a probar distintas posiciones para los elementos, márgenes, tamaños de letra y transparencias. También quiero que el menú sea sencillo y que no quite protagonismo al fondo.

```css
.header {
    position: absolute;
    top: 50px;
    left: 60px;
}

.menu {
    position: absolute;
    top: 50px;
    right: 60px;
    display: flex;
    gap: 25px;
}

.menu a {
    color: white;
    text-decoration: none;
    opacity: 0.8;
    transition: opacity 0.3s;
}

.menu a:hover {
    opacity: 0.4;
}
```

**Nota:** Me gusta cuando las cosas no aparecen de inmediato. Que haya que acercarse un poco para encontrarlas.

---

## Semana 8. Página final

*Un lugar para dejar algo de mí, incluso cuando ya no esté mirando.*

Después de probar distintas formas de organizar el sitio, decido mantener una composición sencilla. El fondo ocupa casi toda la pantalla, mi nombre aparece en la esquina superior izquierda y las secciones se encuentran arriba a la derecha.

La intención es que el sitio tenga una apariencia tranquila, sin demasiados elementos que distraigan.

### Código final

```html
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>Florencia Umaña</title>

<link href="https://fonts.googleapis.com/css2?family=Libre+Baskerville&display=swap" rel="stylesheet">

<style>
body {
font-family: 'Libre Baskerville', serif;
margin: 0;
min-height: 100vh;
background-color: black;
background-image: url("fondo3.jpg");
background-size: cover;
background-repeat: no-repeat;
background-position: center;
}

/* capa oscura */
body::before {
content: "";
position: fixed;
top: 0;
left: 0;
width: 100%;
height: 100%;
background: rgba(0,0,0,0.2);
z-index: -1;
}

.contenedor {
position: relative;
width: 100%;
height: 100vh;
}

/* NOMBRE ARRIBA IZQUIERDA (más sutil) */
.header {
position: absolute;
top: 50px;
left: 60px;
}

h1 {
font-size: 28px;
margin: 0;
color: white;
font-weight: normal;
letter-spacing: 1px;
}

/* quitamos protagonismo al subtítulo */
p {
font-size: 14px;
margin-top: 6px;
color: rgba(255,255,255,0.6);
}

/* MENÚ ARRIBA DERECHA (más fino) */
.menu {
position: absolute;
top: 50px;
right: 60px;
display: flex;
gap: 25px;
}

.seccion a {
text-decoration: none;
color: white;
font-size: 16px;
opacity: 0.8;
transition: opacity 0.3s;
}

.seccion a:hover {
opacity: 0.4;
}
</style>
</head>

<body>

<div class="contenedor">

<div class="header">
<h1>Florencia Umaña</h1>
</div>

<div class="menu">
<div class="seccion">
<a href="obras.html">Obras</a>
</div>

<div class="seccion">
<a href="contacto.html">Contacto</a>
</div>
</div>

</div>

</body>
</html>
```

### Resultado

La página final busca mantener una relación entre la imagen de fondo, la oscuridad y la tipografía. Me interesa que sea un espacio sencillo, donde cada elemento tenga su lugar.

---

### Algunas cosas que me quedaron dando vueltas
¿Cuántas cosas olvidamos sin darnos cuenta?
¿Una fotografía guarda realmente un recuerdo o solamente lo que alcanzamos a ver?
¿Qué pasa con las cosas que ya no podemos recuperar?
Me gustaría que algunas imágenes pudieran quedarse conmigo un poco más.

---

# UNIDAD 2. TOUCHDESIGNER
<img src="https://i.imgur.com/lMZNy7g.gif" alt="GIF Florencia" width="300"><br>
```
Otro espacio de experimentación. Esta vez, trabajando con imágenes superpuestas y palabras.
```
### Registros de experimentación

[Experimentación](https://drive.google.com/drive/folders/1TPhxrVtmqLBfSc_1rInftr-To1jHRwG2?usp=drive_link)

### Desarrollo técnico

[Desarrollo técnico](https://drive.google.com/drive/folders/10MvU5c1Jyb_1p1g2aNi6xswpggMHd_5O?usp=drive_link)

*Algunas cosas se guardan en fotografías, otras en movimiento. No todo recuerdo tiene que permanecer quieto.*
---

No quiero que todo se pierda. Quizás por eso me gusta guardar imágenes, hacer registros y construir pequeños lugares donde las cosas puedan permanecer.
