# **Resumen del Capítulo 6 de  css3: Efectos de Texto y Estilos Tipográficos**  

El capítulo 6 explora las nuevas características de CSS3 que mejoran la tipografía y los efectos visuales del texto en las páginas web. Con el tiempo, la web ha evolucionado más allá del texto básico, permitiendo a los desarrolladores aplicar sombras, controlar el desbordamiento, alinear el texto de nuevas formas y mejorar la legibilidad con opciones avanzadas de tipografía.  

---

**Sombra de Texto (`text-shadow`)**  
Uno de los efectos más llamativos en CSS3 es la propiedad `text-shadow`, que permite agregar sombras al texto para mejorar la estética y la legibilidad.  

**Sintaxis básica:**  
```css
h1 {
    text-shadow: 3px 3px 5px rgba(0, 0, 0, 0.5);
}
```
En esta configuración:  
- `3px` es el desplazamiento horizontal de la sombra.  
- `3px` es el desplazamiento vertical.  
- `5px` es el radio de difuminado.  
- `rgba(0, 0, 0, 0.5)` establece un color negro semitransparente.  

**Sombras múltiples**  
Es posible agregar múltiples sombras separándolas por comas:  
```css
h1 {
    text-shadow: 1px 1px 2px black, 2px 2px 3px gray;
}
```
Esto crea un efecto de sombra en capas.  

---

**Desbordamiento de Texto (`text-overflow`)**  
Cuando el contenido de un texto es más largo que su contenedor, CSS3 permite gestionar cómo se muestra el exceso de contenido con la propiedad `text-overflow`.  

**Opciones disponibles:**  
- `clip`: recorta el texto sin indicar el desbordamiento.  
- `ellipsis`: reemplaza el texto cortado con puntos suspensivos (`...`).  

**Ejemplo de uso:**  
```css
p {
    width: 200px;
    white-space: nowrap;
    overflow: hidden;
    text-overflow: ellipsis;
}
```
Esto evita que el texto se extienda más allá del ancho de `200px` y muestra puntos suspensivos cuando se corta.  

---

**Alineación de Texto (`text-align` y `text-align-last`)**  
CSS3 introduce nuevas opciones para la alineación del texto.  

- **`text-align: start | end;`**: Alinea el texto según la dirección de lectura del idioma.  
- **`text-align-last: left | right | center | justify;`**: Define la alineación de la última línea de un párrafo justificado.  

**Ejemplo de uso:**  
```css
p {
    text-align: justify;
    text-align-last: right;
}
```
Esto justifica el párrafo pero alinea la última línea a la derecha.  

---

**4. Control de Salto de Línea (`word-wrap`, `overflow-wrap`)**  
Algunos textos contienen palabras largas que pueden causar problemas de diseño. CSS3 permite controlar el ajuste del texto dentro de su contenedor.  

**Opciones disponibles:**  
- `word-wrap: break-word;` permite dividir palabras largas en varias líneas.  
- `overflow-wrap: break-word;` es una versión más moderna con el mismo efecto.  

**Ejemplo de uso:**  
```css
p {
    width: 150px;
    word-wrap: break-word;
}
```
Esto evita que las palabras largas sobresalgan del contenedor.  

---

**5. Guionización Automática (`hyphens`)**  
Para mejorar la legibilidad en textos justificados, CSS3 permite agregar guiones automáticos en los saltos de línea.  

**Opciones disponibles:**  
- `none`: Desactiva la guionización.  
- `manual`: Usa guiones insertados manualmente en el HTML con `&shy;`.  
- `auto`: Deja que el navegador agregue guiones donde sea necesario.  

**Ejemplo de uso:**  
```css
p {
    hyphens: auto;
}
```
Esto permite que el navegador inserte guiones según el idioma del texto.  

---

**Redimensionamiento de Elementos (`resize`)**  
CSS3 introduce la propiedad `resize`, que permite a los usuarios cambiar el tamaño de los elementos de texto arrastrando sus bordes.  

**Opciones disponibles:**  
- `none`: No permite el redimensionamiento.  
- `horizontal`: Permite cambiar el ancho.  
- `vertical`: Permite cambiar la altura.  
- `both`: Permite cambiar ambas dimensiones.  

**Ejemplo de uso:**  
```css
textarea {
    resize: both;
}
```
Esto agrega un control para ajustar manualmente el tamaño de la caja de texto.  

---

**Resumen Final**  
Las nuevas propiedades de CSS3 mejoran significativamente la presentación y legibilidad del texto en la web. `text-shadow` agrega efectos visuales llamativos, mientras que `text-overflow` y `word-wrap` ayudan a manejar el contenido en espacios limitados. Además, la alineación de texto y la guionización automática permiten una mejor legibilidad en diferentes dispositivos y contextos.  

Estas características, junto con la capacidad de redimensionar elementos, brindan a los diseñadores más herramientas para mejorar la tipografía y la usabilidad de sus sitios web.  

