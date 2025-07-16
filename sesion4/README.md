# **Sesión: Modelo de caja y diseño básico con CSS**

## **Objetivo de la sesión**

Al finalizar la sesión, los participantes comprenderán el modelo de caja en CSS, las diferencias entre elementos `block` e `inline`, y aplicarán conceptos básicos de diseño como `float`, `inline-block` y `clearfix` para maquetar una página web simple.

---

## **1. Introducción al modelo de caja** (15 min)

📌 **Explicación teórica:**

- El modelo de caja define cómo se estructuran los elementos en una página web.
- Componentes principales:
  - **Content (contenido)**: El área donde se muestra el texto o imágenes.
  - **Padding (relleno)**: Espacio interno entre el contenido y el borde.
  - **Border (borde)**: Línea que rodea el padding y el contenido.
  - **Margin (margen)**: Espacio externo que separa el elemento de otros.

📌 **Demostración visual:**

```css
div {
  width: 200px;
  height: 100px;
  padding: 20px;
  border: 2px solid black;
  margin: 30px;
}
```

- Mostrar en el navegador cómo se calcula el tamaño total:
  - **Ancho total** = `width + padding-left + padding-right + border-left + border-right`
  - **Alto total** = `height + padding-top + padding-bottom + border-top + border-bottom`

---

## **2. Display: Block vs Inline** (10 min)

📌 **Diferencias clave:**

| **Block** (`display: block`)        | **Inline** (`display: inline`)        |
| ----------------------------------- | ------------------------------------- |
| Ocupa todo el ancho disponible.     | Solo ocupa el espacio necesario.      |
| Permite definir `width` y `height`. | No respeta `width` ni `height`.       |
| Ejemplos: `<div>`, `<p>`, `<h1>`    | Ejemplos: `<span>`, `<a>`, `<strong>` |

📌 **Ejemplo práctico:**

```html
<div style="background: lightblue;">Soy un bloque</div>
<span style="background: lightcoral;">Soy inline</span>
```

---

## **3. Ancho (width) y Alto (height)** (10 min)

📌 **Conceptos clave:**

- `width` y `height` definen dimensiones, pero **no aplican a elementos inline**.
- Se pueden usar unidades como `px`, `%`, `em`, `rem`.
- `max-width` y `min-height` son útiles para diseños responsivos.

📌 **Ejercicio rápido:**

```css
.box {
  width: 50%; /* Mitad del contenedor padre */
  height: 100px;
  background: lightgreen;
}
```

---

## **4. Introducción a Float, Inline-Block y Clearfix** (20 min)

📌 **Float:**

- Permite que un elemento flote a la izquierda o derecha.
- Problema común: El contenedor padre colapsa si todos sus hijos son `float`.

📌 **Solución con Clearfix:**

```css
.clearfix::after {
  content: "";
  display: table;
  clear: both;
}
```

📌 **Inline-Block:**

- Combina características de `block` e `inline`.
- Permite definir `width` y `height` pero se alinea como texto.

📌 **Comparación:**

```css
.float-left {
  float: left;
  width: 50%;
}
.inline-block {
  display: inline-block;
  width: 50%;
}
```

---

## **5. Ejercicio Práctico: Maquetar una página con cabecera y menú horizontal** (30 min)

📌 **Requisitos:**

1. Cabecera (`<header>`) con título centrado.
2. Menú horizontal (`<nav>`) con 4 enlaces usando `display: inline-block` o `float`.
3. Contenido principal (`<main>`) con dos columnas.

📌 **Estructura base:**

```html
<header>
  <h1>Mi Página Web</h1>
</header>
<nav>
  <ul>
    <li><a href="#">Inicio</a></li>
    <li><a href="#">Servicios</a></li>
    <li><a href="#">Contacto</a></li>
  </ul>
</nav>
<main>
  <section class="columna-izq">Contenido izquierdo</section>
  <section class="columna-der">Contenido derecho</section>
</main>
```

📌 **Solución CSS:**

```css
nav ul {
  list-style: none;
  padding: 0;
}
nav li {
  display: inline-block; /* Opción: float: left; */
  margin-right: 15px;
}
.columna-izq,
.columna-der {
  float: left;
  width: 50%;
}
main::after {
  content: "";
  display: table;
  clear: both;
}
```

---

## **6. Cierre y dudas** (10 min)

📌 Repasar conceptos clave:

- Modelo de caja (`content-padding-border-margin`).
- Diferencias entre `block`, `inline` e `inline-block`.
- Uso de `float` y `clearfix`.

📌 **Preguntas para reflexión:**

- ¿Qué pasa si no usamos `clearfix` en un diseño con `float`?
- ¿Por qué `inline-block` es útil para menús horizontales?

---

## **Material adicional**

- [MDN: Modelo de caja](https://developer.mozilla.org/es/docs/Learn/CSS/Building_blocks/The_box_model)
- [Guía de Float y Clearfix](https://css-tricks.com/all-about-floats/)

🚀 **¡Listos para diseñar layouts básicos con CSS!**
