## 🌈 Tema: Introducción a CSS

#### Descripción:

En esta sesión aprenderás qué es CSS, para qué sirve y cómo puedes aplicarlo para mejorar la apariencia de tus páginas web. Descubrirás las diferentes formas de incluir CSS, los selectores básicos y las propiedades más importantes para personalizar colores, fuentes, tamaños, bordes y fondos. ¡Da el siguiente paso para que tus sitios web luzcan profesionales y atractivos!

---

### 1️⃣ ¿Qué es CSS y para qué sirve?

CSS (Cascading Style Sheets, Hojas de Estilo en Cascada) es el lenguaje que usamos para definir la presentación y el diseño de las páginas web escritas en HTML. Permite separar el contenido (HTML) de la apariencia (CSS), facilitando el mantenimiento y la personalización de los sitios web.

- **HTML** = estructura y contenido
- **CSS** = diseño y estilo visual

**Ejemplo:**

```html
<p>¡Hola, mundo!</p>
```

```css
p {
  color: blue;
  font-size: 20px;
}
```

---

### 2️⃣ Formas de incluir CSS

Existen tres formas principales de aplicar CSS a una página web:

#### a) En línea

Se escribe el CSS directamente en la etiqueta HTML usando el atributo `style`.

```html
<p style="color: red; font-weight: bold;">Texto en rojo y negrita</p>
```

#### b) Interno (dentro del documento HTML)

Se coloca dentro de la etiqueta `<style>` en la sección `<head>` del HTML.

```html
<head>
  <style>
    h1 {
      color: green;
    }
  </style>
</head>
```

#### c) Externo (archivo .css)

Se crea un archivo aparte (por ejemplo, `styles.css`) y se enlaza con la etiqueta `<link>`.

```html
<head>
  <link rel="stylesheet" href="styles.css" />
</head>
```

Archivo `styles.css`:

```css
body {
  background-color: #f0f0f0;
}
```

> 💡 **Recomendación:** Usa archivos externos para proyectos grandes, así mantienes tu código organizado.

---

### 3️⃣ Selectores básicos

Los selectores permiten elegir a qué elementos HTML se aplicarán los estilos.

- **Por etiqueta:** Aplica a todas las etiquetas de ese tipo.

  ```css
  p {
    color: purple;
  }
  ```

- **Por clase:** Aplica a los elementos con el atributo `class`. Se escribe con un punto (`.`).

  ```css
  .destacado {
    background: yellow;
  }
  ```

  ```html
  <p class="destacado">Texto resaltado</p>
  ```

- **Por ID:** Aplica a un elemento con un identificador único (`id`). Se escribe con almohadilla (`#`).

  ```css
  #titulo-principal {
    font-size: 32px;
  }
  ```

  ```html
  <h1 id="titulo-principal">Bienvenido</h1>
  ```

---

### 4️⃣ Propiedades principales de CSS

Algunas de las propiedades más usadas para dar estilo a tus páginas:

- **color:** Color del texto.
- **background-color:** Color de fondo.
- **font-family:** Tipo de letra.
- **font-size:** Tamaño de la fuente.
- **border:** Bordes alrededor de los elementos.
- **padding:** Espacio interno.
- **margin:** Espacio externo.

**Ejemplo:**

```css
h1 {
  color: #3498db;
  background-color: #eaf6fb;
  font-family: Arial, sans-serif;
  font-size: 28px;
  border: 2px solid #2980b9;
  padding: 10px;
  margin-bottom: 20px;
}
```

---

### 5️⃣ Ejercicio práctico

1. Elige una de las páginas HTML que creaste en sesiones anteriores.
2. Aplica estilos usando las tres formas de incluir CSS (en línea, interno y externo).
3. Usa selectores de etiqueta, clase e ID para personalizar diferentes partes de la página.
4. Cambia colores, fuentes, tamaños, bordes y fondos para experimentar.

> ✨ **Reto:** Crea un archivo `styles.css` y enlázalo a tu página. Intenta que tu página se vea diferente y más atractiva solo cambiando el CSS.

---

### 📝 Preguntas para reflexionar

1. ¿Por qué es importante separar el contenido (HTML) del diseño (CSS)?
2. ¿Qué ventajas tiene usar archivos CSS externos?
3. ¿Cuál es la diferencia entre una clase y un ID en CSS?
4. ¿Qué propiedad usarías para cambiar el color de fondo de una página?
5. ¿Cómo puedes aplicar un mismo estilo a varios elementos diferentes?
