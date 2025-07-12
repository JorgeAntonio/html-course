## 🌟 Tema: Introducción a HTML y Buenas Prácticas

#### Descripción:

En esta sesión aprenderás los conceptos y etiquetas más básicas de HTML para crear tu primera página web. Descubrirás la importancia de las buenas prácticas y el uso correcto de las etiquetas para lograr páginas más accesibles, organizadas y profesionales. ¡Comienza tu camino como desarrollador web desde cero!

---


### 1️⃣ Estructura básica de una página HTML

La estructura básica de cualquier documento HTML está compuesta por tres elementos principales:

- `<html>`: Es la etiqueta raíz que envuelve todo el contenido de la página.
- `<head>`: Contiene metadatos, el título de la página y enlaces a recursos como hojas de estilo.
- `<body>`: Incluye todo el contenido visible para el usuario, como textos, imágenes y enlaces.

**Ejemplo de estructura básica:**

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Mi primera página</title>
    <meta charset="UTF-8" />
  </head>
  <body>
    <h1>¡Hola, mundo!</h1>
    <p>Esta es mi primera página web.</p>
  </body>
</html>
```

> 💡 **Nota:** El `<!DOCTYPE html>` indica al navegador que el documento está escrito en HTML5.


### 2️⃣ Etiquetas básicas de HTML

Las etiquetas son la base de cualquier documento HTML. Algunas de las más importantes son:

```html
<h1>Encabezado 1</h1>
<h2>Encabezado 2</h2>
<h3>Encabezado 3</h3>
<h4>Encabezado 4</h4>
<h5>Encabezado 5</h5>
<h6>Encabezado 6</h6>
<p>Este es un párrafo</p>
<br />
<hr />
```

- `<h1>` a `<h6>`: Encabezados de mayor a menor importancia.
- `<p>`: Párrafo de texto.
- `<br>`: Salto de línea.
- `<hr>`: Línea horizontal de separación.

---


### 3️⃣ Buenas prácticas en HTML

- Usa etiquetas semánticas para dar significado al contenido.
- Evita usar `<div>` para todo. Prefiere etiquetas como `<h1>`, `<p>`, `<header>`, `<footer>`, etc.
- El HTML debe ser comprensible tanto para personas como para navegadores y buscadores.

**Ejemplo de mala práctica:**

```html
<div>Título</div>
<div>Contenido</div>
```

**Ejemplo de buena práctica:**

```html
<h1>Título</h1>
<p>Contenido descriptivo aquí.</p>
```

---


### 4️⃣ Corregir código: de lo incorrecto a lo correcto

**Código incorrecto:**

```html
<div>Mi titulo</div>
<p>Hola soy Juan</p>
<p>Estudio desarrollo web</p>
<div>Fin</div>
```

**Código corregido:**

```html
<h1>Mi título</h1>
<p>Hola, soy Juan.</p>
<p>Estudio desarrollo web.</p>
<hr />
<p>Fin</p>
```

---


### 5️⃣ Ejemplo de página personal

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Sobre mí - [Tu Nombre]</title>
  </head>
  <body>
    <h1>¡Hola, soy [Tu Nombre]!</h1>
    <hr />
    <h2>¿De dónde soy?</h2>
    <p>
      Soy de la ciudad de __________, un lugar muy interesante por ________.
    </p>
    <h2>¿Qué estudio?</h2>
    <p>Estoy estudiando __________. Me gusta porque ________.</p>
    <h2>Mis intereses</h2>
    <h3>Pasatiempos</h3>
    <p>Me gusta jugar videojuegos,<br />leer libros,<br />y ver películas.</p>
    <h3>Mis materias favoritas</h3>
    <p>
      Me gusta <strong>Matemática</strong>, <strong>Computación</strong> y
      <strong>Historia</strong>.
    </p>
    <hr />
    <h2>Contacto</h2>
    <p>Si quieres saber más de mí, ¡pregúntame al final de la clase!</p>
  </body>
</html>
```

---

### 📝 Preguntas para reflexionar

1. ¿Por qué es importante usar etiquetas semánticas en HTML?
2. ¿Qué problemas puede causar el uso excesivo de `<div>`?
3. ¿Para qué sirve la etiqueta `<hr>`?
4. ¿Cómo puedes mejorar la accesibilidad de tu página web?
5. ¿Qué aprendiste sobre la estructura básica de una página HTML?
