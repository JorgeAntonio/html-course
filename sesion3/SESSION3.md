---
## 🌈 Sesión: Introducción a CSS – Estilizando la web
---

### 🎯 Objetivo de la sesión

Al finalizar esta clase, el estudiante podrá aplicar estilos básicos a sus páginas HTML utilizando CSS en sus diferentes formas, comprenderá los selectores principales y dominará propiedades esenciales como color, tipografía, tamaño, borde y fondo.

---

### 🧩 1. ¿Qué es CSS y para qué sirve?

**CSS (Cascading Style Sheets)** es un lenguaje utilizado para **definir la presentación y el estilo** de documentos HTML.

Sirve para:

- Cambiar colores, tamaños y tipografías.
- Posicionar elementos en la pantalla.
- Crear diseños atractivos y responsivos.
- Separar el contenido (HTML) del diseño (CSS).

> Ejemplo básico sin y con CSS:

```html
<!-- HTML sin estilos -->
<p>Hola, soy un párrafo</p>

<!-- Con CSS -->
<p style="color: blue; font-size: 20px;">Hola, soy un párrafo con estilo</p>
```

---

### 🧠 2. Formas de incluir CSS

#### ✅ a) CSS en línea (inline)

Se aplica directamente en el atributo `style` de una etiqueta HTML.

```html
<h1 style="color: red;">Título en rojo</h1>
```

🟡 **Ventaja:** Rápido para cambios puntuales.
🔴 **Desventaja:** No es escalable ni limpio.

---

#### ✅ b) CSS interno (internal)

Se escribe dentro de la etiqueta `<style>` en la cabecera del documento.

```html
<!DOCTYPE html>
<html>
  <head>
    <style>
      p {
        color: green;
      }
    </style>
  </head>
  <body>
    <p>Texto en verde</p>
  </body>
</html>
```

🟡 **Uso:** Ideal en páginas pequeñas o demostraciones.

---

#### ✅ c) CSS externo (external)

Se crea un archivo `.css` separado y se enlaza desde el HTML.

**Archivo:** `estilos.css`

```css
h1 {
  color: purple;
}
```

**HTML:**

```html
<link rel="stylesheet" href="estilos.css" />
```

🟢 **Ventaja:** Limpio, organizado y reutilizable.
🔵 **Recomendado para proyectos grandes.**

---

### 🔍 3. Selectores básicos

#### 📌 a) Por etiqueta

Aplica estilo a todas las etiquetas de un tipo.

```css
p {
  font-family: Arial;
}
```

#### 📌 b) Por clase (.clase)

Usa el atributo `class` para aplicar un estilo a elementos específicos.

```css
.destacado {
  color: orange;
  font-weight: bold;
}
```

```html
<p class="destacado">Este párrafo es importante.</p>
```

#### 📌 c) Por ID (#id)

Usa el atributo `id` para aplicar un estilo único a un solo elemento.

```css
#principal {
  background-color: lightgray;
}
```

```html
<div id="principal">Contenido principal</div>
```

> ⚠️ Consejo: usa clases para estilos repetibles, IDs para únicos.

---

### 🎨 4. Propiedades principales

Estas son las más usadas al comenzar:

| Propiedad     | Ejemplo                    | Descripción                         |
| ------------- | -------------------------- | ----------------------------------- |
| `color`       | `color: blue;`             | Cambia el color del texto           |
| `font-size`   | `font-size: 18px;`         | Tamaño del texto                    |
| `font-family` | `font-family: Verdana;`    | Fuente del texto                    |
| `background`  | `background: yellow;`      | Fondo del elemento                  |
| `border`      | `border: 1px solid black;` | Añade un borde                      |
| `padding`     | `padding: 10px;`           | Espacio interno entre borde y texto |
| `margin`      | `margin: 10px;`            | Espacio externo entre elementos     |

---

### 🛠️ 5. Ejercicio práctico en clase

> **🎯 Actividad:** Aplicar estilos a las páginas HTML que construimos en sesiones anteriores.

**Instrucciones:**

1. Abre uno de los archivos HTML que ya has creado.
2. Añade un `<style>` interno o enlaza un archivo `style.css`.
3. Aplica al menos:

   - Un color de fondo a la página.
   - Diferente color y tamaño para títulos y párrafos.
   - Borde y espacio (margin/padding) a alguna sección.
   - Usa una clase para destacar un texto.
   - Usa un ID para dar estilo especial a un bloque.

**Ejemplo resultado:**

```html
<!DOCTYPE html>
<html lang="es">
  <head>
    <meta charset="UTF-8" />
    <title>Mi Página</title>
    <style>
      body {
        background-color: #f0f0f0;
        font-family: Arial;
      }
      h1 {
        color: navy;
        text-align: center;
      }
      .destacado {
        color: crimson;
        font-weight: bold;
      }
      #footer {
        background: black;
        color: white;
        padding: 10px;
        text-align: center;
      }
    </style>
  </head>
  <body>
    <h1>Bienvenido a mi sitio</h1>
    <p class="destacado">Este texto es importante.</p>
    <p>Otro párrafo con estilo normal.</p>
    <div id="footer">© 2025 - Todos los derechos reservados</div>
  </body>
</html>
```

---
