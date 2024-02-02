### CSS: Apuntes

#### 1. **Enlazar CSS en HTML:**

Siempre se debe incluir un enlace al archivo CSS en el HTML.

```HTML
htmlCopy code<!DOCTYPE html>
<html lang="es">
<head>
    <link rel="stylesheet" href="estilos.css">
</head>
<body>
    <!-- Contenido de la página -->
</body>
</html>
```

#### 2. **Sintaxis CSS:**

Los estilos se definen con llaves:

```CSS
cssCopy code.estilo {
    /* Estilos a asignar al elemento */
}
```

#### 3. **Selectores CSS:**

- Por ID: `#id_asignado`
- Por clase: `.class_asignada` o `etiqueta.clase`
- Universal: `*`

Ejemplo:

```CSS
cssCopy code#miId {
    /* Estilos para el elemento con ID 'miId' */
}

.miClase {
    /* Estilos para elementos con la clase 'miClase' */
}

p.textoRojo {
    /* Estilos para párrafos con la clase 'textoRojo' */
}
```

#### 4. **Comentarios en CSS:**

Se pueden realizar con `/* comentario */` o varias líneas.

Ejemplo:

```CSS
cssCopy code/* Este es un comentario de una línea */

/*
Este es
un comentario
de varias líneas
*/
```

#### 5. **Colores en CSS:**

- Hexadecimal: `#000`, `#f00`, `#0f0`, `#00f` o `#ff0000`.
- RGB: `rgb(red, green, blue)`.

Ejemplo:

```CSS
cssCopy code.fondoNegro {
    background-color: #000;
}

.textoVerde {
    color: rgb(0, 255, 0);
}
```

#### 6. **Bordes en CSS:**

```CSS
cssCopy code.bordeEjemplo {
    border: 5px black solid;
    border-color: aquamarine;
    border-style: dashed;
    border-radius: 5px;
    border-width: 5px;
```

#### 7. **Fondos en CSS:**

```CSS
cssCopy code.fondoEjemplo {
    background: #f00 url(/ruta/imagen.png) repeat-x center bottom;
    background-size: 200px 300px;
    background-repeat: repeat-y;
    background-position: center;
```

#### 8. **Margen y Padding:**

```CSS
cssCopy code.margenEjemplo {
    margin: 15px 20px 25px 30px;
}

.paddingEjemplo {
    padding: 30px 25px 20px 15px;
```

#### 9. **Overflow:**

`overflow: scroll;` / `hidden` / `visible`.

Ejemplo:

```CSS
cssCopy code.scrollEjemplo {
    overflow: scroll;
}
```

#### 10. **Outline:**

~~~CSS
cssCopy code`outline: 1px solid red;`

Ejemplo:
```css
.outlineEjemplo {
    outline: 1px solid red;
}
```
~~~

#### 11. **Propiedades de Texto:**

~~~CSS
cssCopy code```css
.textoEjemplo {
    text-align: justify;
    text-decoration: line-through;
    text-shadow: 3px 4px 3px blue;
```
~~~

#### 12. **Fuentes en CSS:**

~~~CSS
cssCopy code```css
.fuenteEjemplo {
    font-family: "Roboto", sans-serif;
}
```
~~~

#### 13. **Pseudoclases para Enlaces:**

~~~CSS
cssCopy code```css
a:link { color: yellow; }
a:visited { color: gray; }
a:hover { color: blueviolet; }
a:active { color: red; }
```
~~~

#### 14. **Listas en CSS:**

~~~CSS
cssCopy code```css
ul {
    background-color: cadetblue;
    list-style: none;
    padding-left: 0;
}
```
~~~

#### 15. **Tablas en CSS:**

~~~CSS
cssCopy code```css
table {
    width: 100%;
    border-collapse: collapse;
}
th, td {
    border: 1px solid black;
    text-align: left;
}
tr:nth-child(even) { background-color: #eee; }
tr:hover {
    background-color: aquamarine;
    cursor: pointer;
}
```
~~~

#### 16. **Display:**

~~~CSS
cssCopy code```css
span {
    display: block;
    max-width: 300px;
    background-color: aqua;
}
```
~~~

#### 17. **Position:**

~~~CSS
cssCopy code```css
.relative {
    position: relative;
}
.fixed {
    position: fixed;
}
.absolute {
    position: absolute;
}
.sticky {
    position: sticky;
}
```
~~~

#### 18. **Float e Inline-block:**

~~~CSS
cssCopy code```css
.left {
    float: left;
    width: 400px;
}
.right {
    float: right;
}
.inline-block {
    display: inline-block;
    height: 55px;
    background-color: red;
}
.center {
    text-align: center;
    width: 200px;
    margin: 0 auto;
    background-color: red;
}
```
~~~

### 19. **Grid en CSS:**

- Grid es un sistema de diseño bidimensional que permite dividir una página en columnas y filas.

#### **Definir Grid Container:**

- `display: grid;`: Indica que el elemento es un contenedor de cuadrícula.

  ```
  cssCopy code.gridContainer {
      display: grid;
  }
  ```

#### **Definir Columnas y Filas:**

- `grid-template-columns`: Define el ancho de las columnas.

- `grid-template-rows`: Define la altura de las filas.

  ```css
  cssCopy code.gridContainer {
      display: grid;
      grid-template-columns: 1fr 2fr 1fr;
      grid-template-rows: auto 100px;
  }
  ```

#### **Alineación del Contenido:**

- `justify-items`: Alinea el contenido horizontalmente.

- `align-items`: Alinea el contenido verticalmente.

  ```css
  cssCopy code.gridContainer {
      display: grid;
      justify-items: center;
      align-items: center;
  }
  ```

#### **Espaciado entre Celdas:**

- `grid-column-gap`: Establece el espacio entre columnas.

- `grid-row-gap`: Establece el espacio entre filas.

- `grid-gap`: Establece ambos espacios a la vez.

  ```css
  cssCopy code.gridContainer {
      display: grid;
      grid-column-gap: 10px;
      grid-row-gap: 20px;
  }
  ```

#### **Columnas y Filas Explícitas:**

- `grid-column-start` y `grid-column-end`: Indican dónde comienza y termina un elemento en columnas.

- `grid-row-start` y `grid-row-end`: Indican dónde comienza y termina un elemento en filas.

  ```css
  cssCopy code.gridItem {
      grid-column-start: 2;
      grid-column-end: 4;
      grid-row-start: 1;
      grid-row-end: 3;
  }
  ```

#### **Áreas de la Cuadrícula:**

- `grid-template-areas`: Define áreas nombradas en la cuadrícula.

  ```css
  cssCopy code.gridContainer {
      display: grid;
      grid-template-areas:
        "header header header"
        "main main sidebar"
        "footer footer footer";
  }
  
  .header {
      grid-area: header;
  }
  
  .main {
      grid-area: main;
  }
  
  .sidebar {
      grid-area: sidebar;
  }
  
  .footer {
      grid-area: footer;
  }
  ```

#### **Ordenar el Contenido:**

- `order`: Cambia el orden de los elementos en la cuadrícula.

  ```css
  cssCopy code.gridItem:nth-child(2) {
      order: -1;
  }
  ```

#### **Columnas y Filas Automáticas:**

- `auto`: Ajusta automáticamente el tamaño de las columnas o filas.

  ```css
  cssCopy code.gridContainer {
      display: grid;
      grid-template-columns: auto 1fr auto;
  }
  ```

### **20. Grid en CSS: Funciones Importantes**

#### **1. Autofill y Minmax:**

- `repeat(auto-fill, minmax(min, max))`: Crea un número automático de columnas o filas que se ajustan al contenedor.

```css
cssCopy code.gridContainer {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(100px, 1fr));
}
```

#### **2. Grid-Auto-Flow:**

- `grid-auto-flow`: Controla cómo se colocan automáticamente los elementos.

```css
cssCopy code.gridContainer {
    display: grid;
    grid-auto-flow: dense; /* dense para rellenar huecos automáticamente */
}
```

#### **3. Grid-Auto-Rows:**

- `grid-auto-rows`: Establece la altura de las filas automáticas.

```css
cssCopy code.gridContainer {
    display: grid;
    grid-auto-rows: 100px; /* Altura predeterminada de las filas automáticas */
}
```

#### **4. Grid-Column y Grid-Row:**

- `grid-column` y `grid-row`: Propiedades abreviadas para especificar el inicio y el final de una ubicación en la cuadrícula.

```css
cssCopy code.gridItem {
    grid-column: 2 / span 3; /* Empieza en la segunda columna y se extiende 3 columnas */
    grid-row: 1 / 3; /* Empieza en la primera fila y se extiende 2 filas */
}
```

#### **5. Grid-Gap Shorthand:**

- `grid-gap`: Propiedad abreviada para `grid-column-gap` y `grid-row-gap`.

```css
cssCopy code.gridContainer {
    display: grid;
    grid-gap: 10px;
}
```

#### **6. Media Queries con Grid:**

- Utiliza media queries para cambiar la disposición de la cuadrícula en diferentes tamaños de pantalla.

```css
cssCopy code@media screen and (max-width: 600px) {
    .gridContainer {
        grid-template-columns: 1fr; /* Cambia a una sola columna en pantallas pequeñas */
    }
}
```

#### **7. Aspect Ratio:**

- Crea un diseño de cuadrícula con un aspect ratio fijo.

```css
cssCopy code.gridContainer {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
    aspect-ratio: 16 / 9; /* Establece el aspect ratio de la cuadrícula */
}
```

#### **8. Place Items:**

- `place-items`: Propiedad abreviada para `align-items` y `justify-items`.

```css
cssCopy code.gridContainer {
    display: grid;
    place-items: center;
}
```

#### **9. Place Content:**

- `place-content`: Propiedad abreviada para `align-content` y `justify-content`.

```css
cssCopy code.gridContainer {
    display: grid;
    place-content: center space-between; /* Alinea y justifica el contenido */
}
```

#### **10. Named Areas:**

- Asigna nombres a las áreas de la cuadrícula para un diseño más legible.

```css
cssCopy code.gridContainer {
    display: grid;
    grid-template-areas:
        "header header header"
        "main main sidebar"
        "footer footer footer";
}

.header {
    grid-area: header;
}

.main {
    grid-area: main;
}
```

### 21. **Flexbox en CSS: Funciones Importantes**

#### **1. `display: flex;`:**

- Indica que el contenedor es un contenedor flexible.

```css
cssCopy code.flexContainer {
    display: flex;
}
```

#### **2. Dirección Principal:**

- `flex-direction`: Establece la dirección principal de los elementos flexibles.

```css
cssCopy code.flexContainer {
    display: flex;
    flex-direction: row; /* Por defecto, de izquierda a derecha */
}
```

#### **3. Justificación y Alineación:**

- `justify-content`: Alinea los elementos flexibles a lo largo de la dirección principal.
- `align-items`: Alinea los elementos flexibles en la dirección perpendicular a la principal.

```css
cssCopy code.flexContainer {
    display: flex;
    justify-content: space-between;
    align-items: center;
}
```

#### **4. Orden de los Elementos:**

- `order`: Cambia el orden de los elementos flexibles.

```css
cssCopy code.flexItem {
    order: 2; /* Cambia el orden a 2 */
}
```

#### **5. Flex Grow, Shrink y Basis:**

- `flex-grow`: Determina cuánto espacio adicional debe ocupar el elemento flexible.
- `flex-shrink`: Determina cuánto espacio puede contraerse el elemento flexible.
- `flex-basis`: Establece el tamaño inicial del elemento flexible.

```css
cssCopy code.flexItem {
    flex-grow: 1;
    flex-shrink: 0;
    flex-basis: 200px;
}
```

#### **6. Alinear Elementos:**

- `align-self`: Alinea un elemento flexible específico en la dirección perpendicular a la principal.

```css
cssCopy code.flexItem {
    align-self: flex-end;
}
```

#### **7. Envolver Elementos:**

- `flex-wrap`: Define si los elementos flexibles deben envolverse o no cuando no haya espacio suficiente.

```css
cssCopy code.flexContainer {
    display: flex;
    flex-wrap: wrap;
}
```

#### **8. Alineación de Línea Transversal:**

- `align-content`: Alinea las líneas de elementos flexibles en la dirección perpendicular a la principal.

```css
cssCopy code.flexContainer {
    display: flex;
    align-content: space-around;
}
```

#### **9. Orden de las Líneas:**

- `flex-flow`: Propiedad abreviada para `flex-direction` y `flex-wrap`.

```css
cssCopy code.flexContainer {
    display: flex;
    flex-flow: column nowrap;
}
```

#### **10. Centrar en Ambas Direcciones:**

- `justify-content: center;` y `align-items: center;`: Centra los elementos flexibles tanto horizontal como verticalmente.

```css
cssCopy code.flexContainer {
    display: flex;
    justify-content: center;
    align-items: center;
}
```

#### **11. Auto Margen:**

- `margin: auto;`: Distribuye automáticamente el espacio restante entre los elementos flexibles.

```css
cssCopy code.flexItem {
    margin: auto;
}
```

#### **12. Justificar Contenido:**

- `justify-content`: Ajusta la distribución del espacio entre y alrededor de los elementos flexibles.

```css
cssCopy code.flexContainer {
    display: flex;
    justify-content: space-evenly;
}
```

#### **13. Flex para Centrar:**

- Usar `display: flex;` en un elemento para centrar su contenido horizontal y verticalmente.

```css
cssCopy code.centerContainer {
    display: flex;
    justify-content: center;
    align-items: center;
}
```

#### **14. Auto-Grow para Igualar Alturas:**

- Usa `flex: 1;` para que los elementos flexibles crezcan y ocupen el espacio disponible.

```css
cssCopy code.flexItem {
    flex: 1;
}
```

Estas funciones y propiedades ofrecen un control avanzado sobre el diseño y la alineación de elementos flexibles. ¡Explora y experimenta con ellas para crear diseños web más flexibles y dinámicos!

### **22. Transiciones y Animaciones:**

#### **Transiciones (`transition`):**

- `transition`: Propiedad que permite suavizar cambios en propiedades CSS durante un período de tiempo específico.

```css
cssCopy code.elementoTransicion {
    transition: propiedad duración timing-function retraso;
}
```

- Ejemplo:

  ```css
  cssCopy code.elementoTransicion {
      transition: opacity 0.5s ease-in-out;
  }
  ```

#### **Animaciones (`@keyframes`):**

- `@keyframes`: Regla que define una secuencia de cambios que se aplicarán gradualmente a un elemento.

```css
cssCopy code@keyframes nombreAnimacion {
    from { /* Estado inicial */ }
    to { /* Estado final */ }
}

.elementoAnimado {
    animation: nombreAnimacion duración timing-function retraso iteraciones dirección;
}
```

- Ejemplo:

  ```css
  cssCopy code@keyframes fadeIn {
      from { opacity: 0; }
      to { opacity: 1; }
  }
  
  .elementoAnimado {
      animation: fadeIn 1s ease-in-out 0.5s infinite alternate;
  }
  ```

### **23. Filtros y Efectos Visuales:**

#### **Filtros (`filter`):**

- `filter`: Aplica efectos visuales a un elemento, como desenfoque, saturación, etc.

```css
cssCopy code.elementoFiltrado {
    filter: blur(5px) brightness(120%);
}
```

- Ejemplo:

  ```css
  cssCopy code.imagenFiltrada {
      filter: grayscale(50%) contrast(150%);
  }
  ```

#### **Box Shadow (`box-shadow`):**

- `box-shadow`: Añade sombras alrededor de un elemento.

```css
cssCopy code.elementoSombrado {
    box-shadow: 5px 5px 10px rgba(0, 0, 0, 0.5);
}
```

- Ejemplo:

  ```css
  cssCopy code.tarjetaSombrada {
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
  }
  ```

#### **Perspectiva (`perspective`):**

- `perspective`: Controla la perspectiva en transformaciones 3D.

```css
cssCopy code.elemento3D {
    transform: perspective(1000px) rotateX(45deg);
}
```

- Ejemplo:

  ```css
  cssCopy code.caja3D {
      perspective: 800px;
  }
  ```

### **24. Variables CSS (Custom Properties):**

#### **Definir Variable:**

- `:root`: Pseudo-clase que establece variables CSS a nivel global.

```css
cssCopy code:root {
    --color-primario: #3498db;
}
```

#### **Utilizar Variable:**

- `var()`: Función que recupera el valor de una variable.

```css
cssCopy code.elementoConVariable {
    color: var(--color-primario);
}
```

- Ejemplo:

  ```css
  cssCopy code.temaClaro {
      background-color: var(--color-fondo-claro);
  }
  ```

### **25. CSS Grid y Flexbox Combinados:**

#### **Uso Conjunto de Grid y Flexbox:**

- Combinar las ventajas de ambos modelos de diseño para lograr resultados más flexibles y complejos.

```css
cssCopy code.contenedor {
    display: grid;
    grid-template-columns: 1fr 2fr;
}

.elementoFlexbox {
    display: flex;
    justify-content: center;
    align-items: center;
}
```

- Ejemplo:

  ```css
  cssCopy code.gridConFlexbox {
      display: grid;
      grid-template-columns: 1fr 2fr;
  }
  
  .flexboxDentroGrid {
      display: flex;
      justify-content: space-between;
  }
  ```

### **26. Unidades Relativas (vw, vh, %):**

#### **Viewport Width (`vw`) y Viewport Height (`vh`):**

- Unidades relativas al tamaño de la ventana gráfica.

```css
cssCopy code.elemento {
    width: 50vw;
    height: 75vh;
}
```

- Ejemplo:

  ```css
  cssCopy code.seccionPrincipal {
      height: 100vh;
  }
  ```

#### **Porcentaje (%):**

- Unidad relativa al contenedor padre.

```css
cssCopy code.elementoHijo {
    width: 50%;
}
```

- Ejemplo:

  ```css
  cssCopy code.columna {
      width: 33.33%;
  }
  ```

### **27. Media Queries Avanzadas:**

#### **Consulta de Medios Personalizada (`@media`):**

- Utilizar media queries para adaptar estilos según características específicas de la pantalla.

```css
cssCopy code@media screen and (max-width: 600px) {
    /* Estilos para pantallas pequeñas */
}
```

- Ejemplo:

  ```css
  cssCopy code@media (orientation: landscape) {
      .elementoLandscape {
          width: 100%;
      }
  }
  ```

### **28. Overflow y Scroll Snap:**

#### **Overflow (`overflow`):**

- Controlar el manejo del contenido que desborda su contenedor.

```css
cssCopy code.elementoDesbordado {
    overflow: hidden; /* Puedes usar scroll, auto, visible, etc. */
}
```

- Ejemplo:

  ```css
  cssCopy code.contenedorDesbordado {
      overflow: auto;
  }
  ```

#### **Scroll Snap (`scroll-snap`):**

- Definir puntos de anclaje para un desplazamiento suave.

```css
cssCopy code.contenedorDesplazado {
    scroll-snap-type: y mandatory;
}
```

- Ejemplo:

  ```css
  cssCopy code.scrollSnapElement {
      scroll-snap-align: start;
  }
  ```

### **29. Unidades EM y REM:**

#### **Unidad EM:**

- Relativa al tamaño de la fuente del elemento.

```css
cssCopy code.elementoEm {
    margin: 1em; /* 1em es igual al tamaño de la fuente del elemento */
}
```

- Ejemplo:

  ```css
  cssCopy code.textoConMargen {
      margin: 0.5em;
  }
  ```

#### **Unidad REM:**

- Relativa al tamaño de la fuente del elemento raíz (`html`).

```css
cssCopy code.elementoRem {
    font-size: 1.5rem; /* 1.5 veces el tamaño de la fuente del elemento raíz */
}
```

- Ejemplo:

  ```css
  cssCopy code.tituloPrincipal {
      font-size: 2rem;
  }
  ```


