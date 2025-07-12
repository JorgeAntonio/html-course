## Tema: Etiquetas HTML esenciales

#### Descripcion:

En esta guía descubrirás las etiquetas HTML esenciales que te permitirán construir tu primera página web funcional y atractiva. Aprenderás cómo enlazar páginas, mostrar imágenes, organizar información con listas y tablas, y crear formularios básicos para interactuar con los usuarios. ¡Da el primer paso para convertirte en creador de sitios web!

---

### 1. Enlaces: `<a href="...">`

#### ¿Qué es un enlace?

Un enlace es un texto o imagen que, al hacer clic, lleva al usuario a otra página o sección. En HTML se crea con la etiqueta `<a>` y el atributo `href`.

#### Estructura:

```html
<a href="https://www.ejemplo.com">Visitar sitio web</a>
```

- `a`: significa "anchor" (ancla).
- `href`: es el destino del enlace.

#### Enlaces a otra página dentro del mismo sitio:

```html
<a href="contacto.html">Ir a Contacto</a>
```

#### Enlace que se abre en una nueva pestaña:

```html
<a href="https://openai.com" target="_blank">Abrir OpenAI</a>
```

#### Enlace a secciones del contenido:

```html
<a href="#inicio">Ir al inicio</a>
```

### Ejemplo

```html
<!DOCTYPE html>
<html lang="es">
  <head>
    <title>Enlaces HTML</title>
  </head>
  <body>
    <nav>
      <a href="index.html">Inicio</a>
      <a href="acerca.html">Acerca</a>
      <a href="contacto.html">Contacto</a>
    </nav>

    <h1>Página de Enlaces</h1>

    <p>
      Visita <a href="https://www.google.com" target="_blank">Google</a> en una
      nueva pestaña.
    </p>

    <p>Ir a la <a href="#seccion2">segunda sección</a>.</p>

    <section id="seccion2">
      <h2>Segunda Sección</h2>
      <p>Esta es la segunda sección de la página.</p>
    </section>
  </body>
</html>
```

> 💡 **Buena práctica:** Usa nombres descriptivos para que el usuario sepa a dónde irá.

---

### 2. Imágenes: `<img src="..." alt="...">`

#### ¿Qué hace esta etiqueta?

Muestra una imagen en la página. ¡Ojo! Es una etiqueta **autocontenida** (no se cierra con `</img>`).
Las imágenes se insertan con la etiqueta `<img>`. Es importante incluir el atributo alt para accesibilidad.

#### Estructura:

```html
<img src="logo.png" alt="Logotipo de la empresa" />
```

- `src`: ruta de la imagen.
- `alt`: texto alternativo (muy útil si la imagen no carga o para usuarios con discapacidad visual).
- `width/height`: o tamaño de la imagen.

#### Ejemplo:

```html
<!DOCTYPE html>
<html lang="es">
  <head>
    <title>Imágenes HTML</title>
  </head>
  <body>
    <h1>Galería de Imágenes</h1>

    <img
      src="https://via.placeholder.com/300x200"
      alt="Imagen de ejemplo"
      width="300"
      height="200"
    />

    <p>Esta es una imagen de ejemplo con texto alternativo.</p>

    <img
      src="https://via.placeholder.com/400x300/ff0000/ffffff"
      alt="Imagen roja de ejemplo"
      style="border: 2px solid #333;"
    />
  </body>
</html>
```

> 🛠️ **Error común:** Olvidar el atributo `alt`. Es obligatorio para accesibilidad y buena práctica web.

---

### 3. Listas: `<ul>`, `<ol>`, `<li>`

#### ¿Qué son?

Las listas agrupan elementos relacionados, como pasos o categorías. HTML ofrece dos tipos principales de listas.

- `<ul>`: lista desordenada (viñetas).
- `<ol>`: lista ordenada (numerada).
- `<li>`: elemento de lista (se usa en ambos tipos)

#### Ejemplo:

```html
<!DOCTYPE html>
<html lang="es">
  <head>
    <title>Listas HTML</title>
  </head>
  <body>
    <h1>Tipos de Listas</h1>

    <h2>Lista No Ordenada</h2>
    <ul>
      <li>Manzana</li>
      <li>Naranja</li>
      <li>Plátano</li>
    </ul>

    <h2>Lista Ordenada</h2>
    <ol>
      <li>Primer paso</li>
      <li>Segundo paso</li>
      <li>Tercer paso</li>
    </ol>

    <h2>Lista Anidada</h2>
    <ul>
      <li>
        Frutas
        <ul>
          <li>Manzana</li>
          <li>Naranja</li>
        </ul>
      </li>
      <li>
        Verduras
        <ul>
          <li>Lechuga</li>
          <li>Tomate</li>
        </ul>
      </li>
    </ul>
  </body>
</html>
```

> 🧠 **Reflexión:** ¿Cuándo usar `<ul>` y cuándo `<ol>`? Usa `<ol>` solo si el orden importa (como pasos o recetas).

---

### 4. Tablas: `<table>`, `<tr>`, `<td>`, `<th>`

#### ¿Qué es una tabla?

Es una forma de mostrar información en filas y columnas, como una hoja de Excel.

#### Partes de una tabla:

```html
<table border="1">
  <tr>
    <!-- Fila -->
    <th>Nombre</th>
    <!-- Celda de encabezado -->
    <th>Correo</th>
  </tr>
  <tr>
    <td>Lucía</td>
    <!-- Celda de datos -->
    <td>lucia@email.com</td>
  </tr>
</table>
```

- `<table>`: define la tabla.
- `<tr>`: fila (table row).
- `<td>`: celda (table data).
- `<th>`: encabezado de columna (table header).

#### Ejemplo:

```html
<!DOCTYPE html>
<html lang="es">
  <head>
    <title>Tablas HTML</title>
  </head>
  <body>
    <h1>Tabla de Estudiantes</h1>

    <table border="1">
      <thead>
        <tr>
          <th>Nombre</th>
          <th>Edad</th>
          <th>Curso</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>Ana García</td>
          <td>20</td>
          <td>HTML</td>
        </tr>
        <tr>
          <td>Carlos López</td>
          <td>22</td>
          <td>CSS</td>
        </tr>
        <tr>
          <td>María Rodríguez</td>
          <td>19</td>
          <td>JavaScript</td>
        </tr>
      </tbody>
    </table>
  </body>
</html>
```

> 🛠️ **Nota:** El atributo `border="1"` se usa solo para visualizar el borde rápidamente. Más adelante lo haremos con CSS.

---

### 5. Formularios introductorios

#### ¿Qué es un formulario?

Es una forma de pedirle datos al usuario, como nombre o correo.

#### Estructura básica:

```html
<form>
  <label for="nombre">Nombre:</label>
  <input type="text" id="nombre" name="nombre" />
  <br /><br />
  <button type="submit">Enviar</button>
</form>
```

- `<form>`: contenedor del formulario.
- `<label>`: etiqueta para el campo (mejora accesibilidad).
- `<input type="text">`: caja de texto.
- `<button type="submit">`: botón para enviar.

#### Ejemplo:

```html
<!DOCTYPE html>
<html lang="es">
  <head>
    <title>Formularios HTML</title>
  </head>
  <body>
    <h1>Formulario de Contacto</h1>

    <form>
      <label for="nombre">Nombre:</label>
      <input type="text" id="nombre" name="nombre" required />
      <br /><br />

      <label for="email">Correo electrónico:</label>
      <input type="email" id="email" name="email" required />
      <br /><br />

      <label for="mensaje">Mensaje:</label>
      <textarea id="mensaje" name="mensaje" rows="4" cols="50"></textarea>
      <br /><br />
      <button type="submit">Enviar</button>
    </form>
  </body>
</html>
```

> 💬 **Consejo:** Siempre conecta `label` con el campo usando `for` e `id`.

---

### Ejercicio:

Vamos a poner todo en práctica. Crea un archivo llamado `index.html` y copia el siguiente código:

```html
<!DOCTYPE html>
<html lang="es">
  <head>
    <meta charset="UTF-8" />
    <title>Mi primera página web</title>
  </head>
  <body>
    <h1>Bienvenido a mi página personal</h1>

    <!-- Enlace -->
    <p><a href="contacto.html">Ir a la página de contacto</a></p>

    <!-- Imagen -->
    <img src="foto.jpg" alt="Foto de perfil" width="200" />

    <!-- Lista -->
    <h2>Mis intereses</h2>
    <ul>
      <li>Programación</li>
      <li>Diseño web</li>
      <li>Leer libros</li>
    </ul>

    <!-- Tabla -->
    <h2>Mis cursos</h2>
    <table border="1">
      <tr>
        <th>Curso</th>
        <th>Estado</th>
      </tr>
      <tr>
        <td>HTML</td>
        <td>Completado</td>
      </tr>
      <tr>
        <td>CSS</td>
        <td>En progreso</td>
      </tr>
    </table>

    <!-- Formulario -->
    <h2>Contáctame</h2>
    <form>
      <label for="nombre">Nombre:</label>
      <input type="text" id="nombre" name="nombre" />
      <br /><br />
      <button type="submit">Enviar</button>
    </form>
  </body>
</html>
```

### 📝 Preguntas para reflexionar 1. ¿Qué diferencia hay entre un enlace externo

y uno interno? 2. ¿Por qué es importante el atributo `alt` en una imagen? 3.
¿Cuándo debo usar una lista ordenada en lugar de una desordenada? 4. ¿Qué
etiquetas se usan para organizar los datos en una tabla? 5. ¿Qué otras entradas
podría tener un formulario además del texto?
