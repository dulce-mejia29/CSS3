# **Resumen del Capítulo 7: Múltiples Columnas**  

El capítulo 7 del libro trata sobre el módulo de diseño de múltiples columnas en CSS3, el cual permite dividir el contenido en varias columnas de forma flexible, similar a los diseños tradicionales en periódicos y revistas. Esto es útil para mejorar la legibilidad y aprovechar mejor el espacio en pantallas anchas.  

A lo largo del capítulo, se presentan dos métodos principales para crear columnas:  

1. **Columnas prescriptivas (`column-count`)**: Permiten definir un número fijo de columnas dentro de un contenedor.  
2. **Columnas dinámicas (`column-width`)**: En lugar de establecer una cantidad de columnas fija, se define un ancho mínimo y el navegador determina cuántas columnas caben en el espacio disponible.  

También se abordan propiedades complementarias para mejorar la apariencia del diseño en columnas, como los espacios entre columnas (`column-gap`), las reglas visuales entre ellas (`column-rule`) y la distribución del contenido (`column-fill`).  

---

**Creación de Columnas con `column-count`**  
La forma más sencilla de dividir el contenido en columnas es especificando un número fijo con `column-count`.  

**Ejemplo básico:**  
```css
.container {
    column-count: 3; /* Divide el contenido en 3 columnas */
}
```
Esto distribuye automáticamente el texto en tres columnas de igual altura dentro del contenedor.  

---

**Columnas Dinámicas con `column-width`**  
En lugar de establecer un número de columnas, podemos definir un ancho mínimo para cada una, permitiendo que el navegador ajuste la cantidad de columnas en función del espacio disponible.  

**Ejemplo:**  
```css
.container {
    column-width: 200px; /* Cada columna tendrá al menos 200px */
}
```
Si el contenedor tiene suficiente ancho, se agregarán más columnas automáticamente para llenar el espacio.  

---

**Espaciado y Líneas Entre Columnas (`column-gap` y `column-rule`)**  
Para mejorar la estética del diseño, se pueden agregar espacios entre columnas y reglas divisorias.  

- **`column-gap`** define el espacio entre columnas.  
- **`column-rule`** agrega una línea entre ellas, similar a un borde.  

**Ejemplo:**  
```css
.container {
    column-count: 3;
    column-gap: 20px; /* Espacio de 20px entre columnas */
    column-rule: 2px solid gray; /* Línea divisoria de 2px en color gris */
}
```
Esto crea tres columnas con un espacio de 20px entre ellas y una línea divisoria.  

---

**Distribución del Contenido (`column-fill`)**  
Por defecto, el navegador intenta equilibrar el contenido en todas las columnas (`balance`), pero podemos cambiar este comportamiento con `auto`, lo que hace que el contenido se distribuya de arriba hacia abajo antes de pasar a la siguiente columna.  

**Ejemplo:**  
```css
.container {
    column-count: 3;
    column-fill: auto; /* Llena las columnas de arriba hacia abajo */
}
```

---

**Elementos que Abarcan Varias Columnas (`column-span`)**  
Si necesitamos que un elemento ocupe el ancho completo del contenedor en un diseño de múltiples columnas, podemos usar `column-span`.  

**Ejemplo:**  
```css
h2 {
    column-span: all;
}
```
Esto hace que el `h2` interrumpa el flujo de las columnas y se extienda a lo ancho del contenedor.  

---

**Imágenes y Otros Elementos en Columnas**  
Si una imagen o cualquier otro elemento dentro de una columna es más grande que el ancho de la columna, el navegador puede cortarlo o hacer que sobresalga. Para evitar esto, se recomienda usar `max-width: 100%` en las imágenes.  

**Ejemplo:**  
```css
img {
    max-width: 100%; /* La imagen no excederá el ancho de la columna */
}
```

---

**7. Consideraciones y Problemas Comunes**  
Si bien las columnas múltiples en CSS3 pueden mejorar la presentación del contenido, hay algunas limitaciones a tener en cuenta:  

- Algunos navegadores más antiguos pueden requerir prefijos (`-webkit-`, `-moz-`).  
- La propiedad `column-span` no está soportada en todos los navegadores.  
- En dispositivos móviles, el uso de muchas columnas puede afectar la legibilidad.  

---

