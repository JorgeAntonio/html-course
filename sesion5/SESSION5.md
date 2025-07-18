# Sesión 5: Posicionamiento CSS y Flexbox

**Fecha:** Viernes 18 de julio de 2024  
**Horario:** 4:00 p.m. - 7:00 p.m.  
**Instructor:** Jorge Antonio Del Águila Malafaya

## 📋 Contenido de la Sesión

### 1. Posicionamiento CSS

#### ¿Qué es el posicionamiento?

El posicionamiento en CSS determina cómo se coloca un elemento en relación con su posición normal en el flujo del documento.

#### Tipos de posicionamiento:

##### `position: static` (por defecto)

- Es el comportamiento normal de los elementos
- Los elementos se posicionan según el flujo normal del documento
- Las propiedades `top`, `right`, `bottom`, `left` no tienen efecto

```css
.elemento {
  position: static;
  /* top, right, bottom, left no funcionan */
}
```

##### `position: relative`

- El elemento se posiciona relativo a su posición normal
- Mantiene su espacio en el flujo del documento
- Se puede mover usando `top`, `right`, `bottom`, `left`

```css
.elemento {
  position: relative;
  top: 20px; /* Se mueve 20px hacia abajo */
  left: 30px; /* Se mueve 30px hacia la derecha */
}
```

##### `position: absolute`

- El elemento se posiciona relativo al ancestro posicionado más cercano
- Se saca del flujo normal del documento
- Si no hay ancestro posicionado, se posiciona relativo al `<body>`

```css
.contenedor {
  position: relative; /* Necesario para que absolute funcione */
}

.elemento {
  position: absolute;
  top: 0;
  right: 0; /* Esquina superior derecha del contenedor */
}
```

##### `position: fixed`

- El elemento se posiciona relativo a la ventana del navegador
- Se mantiene fijo incluso al hacer scroll
- Se saca del flujo normal del documento

```css
.navbar {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  background: white;
  z-index: 1000;
}
```

##### `position: sticky`

- Combina `relative` y `fixed`
- Se comporta como `relative` hasta que alcanza un punto específico
- Luego se comporta como `fixed`

```css
.menu {
  position: sticky;
  top: 0;
  background: white;
}
```

#### Propiedades de coordenadas:

- `top`: Distancia desde el borde superior
- `right`: Distancia desde el borde derecho
- `bottom`: Distancia desde el borde inferior
- `left`: Distancia desde el borde izquierdo

### 2. Flexbox (CSS Flexible Box Layout)

#### ¿Qué es Flexbox?

Flexbox es un modelo de diseño unidimensional que permite distribuir elementos de manera flexible dentro de un contenedor.

#### Conceptos básicos:

##### Contenedor Flex (Flex Container)

```css
.contenedor {
  display: flex; /* o display: inline-flex */
}
```

##### Elementos Flex (Flex Items)

Los hijos directos del contenedor flex se convierten automáticamente en elementos flex.

#### Propiedades del contenedor:

##### `flex-direction`

Define la dirección del eje principal:

- `row` (por defecto): Izquierda a derecha
- `row-reverse`: Derecha a izquierda
- `column`: Arriba hacia abajo
- `column-reverse`: Abajo hacia arriba

```css
.contenedor {
  display: flex;
  flex-direction: row; /* horizontal */
  /* flex-direction: column; /* vertical */
}
```

##### `justify-content`

Alinea elementos en el eje principal:

- `flex-start` (por defecto): Al inicio
- `flex-end`: Al final
- `center`: Al centro
- `space-between`: Espacio entre elementos
- `space-around`: Espacio alrededor de elementos
- `space-evenly`: Espacio uniforme

```css
.contenedor {
  display: flex;
  justify-content: center; /* Centra horizontalmente */
}
```

##### `align-items`

Alinea elementos en el eje transversal:

- `stretch` (por defecto): Estira para llenar
- `flex-start`: Al inicio
- `flex-end`: Al final
- `center`: Al centro
- `baseline`: Alineado por línea base

```css
.contenedor {
  display: flex;
  align-items: center; /* Centra verticalmente */
}
```

##### `flex-wrap`

Controla si los elementos se envuelven:

- `nowrap` (por defecto): No se envuelven
- `wrap`: Se envuelven a la siguiente línea
- `wrap-reverse`: Se envuelven en dirección inversa

```css
.contenedor {
  display: flex;
  flex-wrap: wrap; /* Permite múltiples líneas */
}
```

##### `align-content`

Alinea múltiples líneas (cuando hay `flex-wrap: wrap`):

- `stretch` (por defecto)
- `flex-start`
- `flex-end`
- `center`
- `space-between`
- `space-around`

#### Propiedades de los elementos flex:

##### `flex-grow`

Define cuánto puede crecer un elemento:

```css
.elemento {
  flex-grow: 1; /* Toma el espacio disponible */
}
```

##### `flex-shrink`

Define cuánto puede encogerse un elemento:

```css
.elemento {
  flex-shrink: 0; /* No se encoge */
}
```

##### `flex-basis`

Define el tamaño base del elemento:

```css
.elemento {
  flex-basis: 200px; /* Ancho base de 200px */
}
```

##### `flex` (shorthand)

Combina `flex-grow`, `flex-shrink` y `flex-basis`:

```css
.elemento {
  flex: 1 0 200px; /* grow shrink basis */
  /* flex: 1; /* Equivale a flex: 1 1 0% */
}
```

##### `align-self`

Alinea un elemento específico en el eje transversal:

```css
.elemento-especial {
  align-self: flex-end; /* Al final del contenedor */
}
```

#### Orden de elementos:

```css
.elemento {
  order: 1; /* Cambia el orden visual */
}
```

## 🎯 Ejercicios Prácticos

### Ejercicio 1: Tipos de Posicionamiento

Crear ejemplos visuales de cada tipo de posicionamiento.

### Ejercicio 2: Coordenadas y Posicionamiento

Practicar el uso de `top`, `left`, `right`, `bottom` con diferentes tipos de posicionamiento.

### Ejercicio 3: Flexbox Básico

Crear layouts simples usando flexbox para centrar elementos.

### Ejercicio 4: Distribución con Flexbox

Practicar `justify-content` y `align-items` con diferentes valores.

### Ejercicio 5: Layout Completo

Crear una estructura con sidebar + contenido principal usando flexbox.

## 📚 Recursos Adicionales

- [MDN - CSS Position](https://developer.mozilla.org/es/docs/Web/CSS/position)
- [MDN - Flexbox](https://developer.mozilla.org/es/docs/Web/CSS/CSS_Flexible_Box_Layout)
- [CSS-Tricks - A Complete Guide to Flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)
- [Flexbox Froggy](https://flexboxfroggy.com/) - Juego interactivo

## 🏠 Tarea para la Próxima Sesión

Crear una página web con:

- Header fijo en la parte superior
- Sidebar lateral con navegación
- Contenido principal que se ajuste al espacio restante
- Footer fijo en la parte inferior
- Diseño responsive usando flexbox

---

**Próxima sesión:** Sesión 6 - CSS Grid y Diseño Responsive
