# Sesión 6: HTML avanzado, formularios y buenas prácticas

**Fecha:** Lunes 21 de julio de 2024  
**Horario:** 4:00 p.m. - 7:00 p.m.  
**Instructor:** Jorge Antonio Del Águila Malafaya

## 📋 Contenido de la Sesión

### 1. HTML5 Semántico

- Uso de etiquetas semánticas: `<header>`, `<nav>`, `<main>`, `<section>`, `<footer>`
- Ventajas de la semántica para SEO y accesibilidad

**Ejemplo:**

```html
<header>
  <h1>Mi sitio web</h1>
</header>
<nav>
  <ul>
    <li><a href="#">Inicio</a></li>
    <li><a href="#">Contacto</a></li>
  </ul>
</nav>
<main>
  <section>
    <h2>Bienvenido</h2>
    <p>Contenido principal...</p>
  </section>
</main>
<footer>
  <p>Derechos reservados</p>
</footer>
```

---

### 2. Formularios completos en HTML5

- Inputs: `type="text"`, `type="email"`, `type="checkbox"`, `type="radio"`, `select`, `textarea`
- Uso de `<label>` correctamente asociado
- Validación básica con atributos (`required`, `pattern`, etc.)

**Ejemplo:**

```html
<form>
  <label for="nombre">Nombre:</label>
  <input type="text" id="nombre" name="nombre" required />

  <label for="email">Correo:</label>
  <input type="email" id="email" name="email" required />

  <label>Género:</label>
  <input type="radio" id="masc" name="genero" value="masculino" />
  <label for="masc">Masculino</label>
  <input type="radio" id="fem" name="genero" value="femenino" />
  <label for="fem">Femenino</label>

  <label for="intereses">Intereses:</label>
  <select id="intereses" name="intereses">
    <option value="html">HTML</option>
    <option value="css">CSS</option>
    <option value="js">JavaScript</option>
  </select>

  <input type="checkbox" id="suscribir" name="suscribir" />
  <label for="suscribir">Suscribirse al boletín</label>

  <button type="submit">Enviar</button>
</form>
```

---

### 3. Accesibilidad básica en HTML

- Uso de `alt` en imágenes
- Asociación de `<label>` y campos de formulario
- Uso de `aria-label` cuando no es posible usar `<label>`
- Estructura clara y roles semánticos

**Ejemplo:**

```html
<img src="logo.png" alt="Logo de la empresa" />
<input type="text" aria-label="Buscar" />
```

---

### 4. Introducción rápida al SEO on-page

- Uso de `<title>`, `<meta name="description">`, `<meta name="keywords">`
- Encabezados jerárquicos (`<h1>`, `<h2>`, ...)
- Estructura semántica y enlaces internos

**Ejemplo:**

```html
<head>
  <title>Mi sitio web</title>
  <meta name="description" content="Página de ejemplo para SEO." />
  <meta name="keywords" content="HTML, CSS, SEO, accesibilidad" />
</head>
```

---

## 🎯 Ejercicio Práctico

**Maquetar un formulario semántico y accesible:**

- Utiliza etiquetas semánticas para la estructura general
- Incluye al menos: input de texto, email, radio, checkbox, select
- Usa `<label>` correctamente y atributos de accesibilidad
- Agrega metaetiquetas y títulos adecuados en el `<head>`

---

## 📚 Recursos Adicionales

- [MDN - HTML Semántico](https://developer.mozilla.org/es/docs/Glossary/Semantics)
- [MDN - Formularios HTML](https://developer.mozilla.org/es/docs/Learn/Forms)
- [MDN - Accesibilidad](https://developer.mozilla.org/es/docs/Web/Accessibility)
- [Guía rápida de SEO on-page](https://ahrefs.com/blog/on-page-seo/)

---

**¡Listos para crear páginas web accesibles y optimizadas!**
