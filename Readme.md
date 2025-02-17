# **Resumen del Capítulo 9: Efectos de Bordes y Cajas en CSS3**  

El capítulo 9 se centra en las nuevas propiedades de CSS3 para mejorar los bordes y los efectos de caja. Estas herramientas permiten crear elementos visualmente atractivos sin necesidad de imágenes adicionales ni estructuras HTML complicadas. CSS3 introduce propiedades como `border-radius` para esquinas redondeadas, `box-shadow` para sombras externas e internas, y `border-image` para bordes personalizados con imágenes. ¡Vamos a desglosarlo!  

---

**Esquinas Redondeadas (`border-radius`)**  

La propiedad `border-radius` permite crear esquinas redondeadas en elementos sin necesidad de imágenes. Se define usando valores de píxeles o porcentajes para cada esquina.  

✅ **Sintaxis básica:**  
```css
div {
    border-radius: 20px;
}
```
Esto aplica un radio de 20 píxeles a las cuatro esquinas del elemento.  

✅ **Valores individuales por esquina:**  
```css
div {
    border-top-left-radius: 20px;
    border-top-right-radius: 10px;
    border-bottom-right-radius: 30px;
    border-bottom-left-radius: 15px;
}
```
Cada esquina puede tener un radio diferente, creando formas más dinámicas.  

✅ **Shorthand:**  
```css
div {
    border-radius: 20px 10px 30px 15px;
}
```
El orden es: **superior izquierda**, **superior derecha**, **inferior derecha**, **inferior izquierda**.

---

**Imágenes para Bordes (`border-image`)**  

`border-image` permite utilizar una imagen como borde, en lugar de los colores o estilos de borde tradicionales.  

✅ **Propiedades principales:**  
- **`border-image-source`**: Define la imagen a usar.  
- **`border-image-slice`**: Divide la imagen en nueve secciones (cuatro esquinas, cuatro lados y el centro).  
- **`border-image-width`**: Define el ancho del borde de la imagen.  
- **`border-image-outset`**: Controla cuánto sobresale la imagen del borde.  
- **`border-image-repeat`**: Define cómo se repite la imagen (stretch, repeat o round).  

✅ **Ejemplo completo:**  
```css
div {
    border-image-source: url('borde.png');
    border-image-slice: 34;
    border-image-width: 10px;
    border-image-outset: 5px;
    border-image-repeat: round;
}
```

✅ **Shorthand:**  
```css
div {
    border-image: url('borde.png') 34 / 10px / 5px round;
}
```
Este código ahorra espacio, combinando todas las propiedades en una sola línea.

---

**Sombras de Caja (`box-shadow`)**  

CSS3 introduce la propiedad `box-shadow` para aplicar sombras a los elementos, ya sea en el exterior o en el interior de la caja.  

✅ **Sintaxis básica:**  
```css
div {
    box-shadow: 4px 4px 10px rgba(0, 0, 0, 0.5);
}
```
- **4px**: Desplazamiento horizontal.  
- **4px**: Desplazamiento vertical.  
- **10px**: Radio de difuminado.  
- **rgba(0, 0, 0, 0.5)**: Color de la sombra.  

✅ **Sombras múltiples:**  
```css
div {
    box-shadow: 0 4px 8px rgba(0,0,0,0.3), 0 -4px 8px rgba(0,0,0,0.2);
}
```
Esto aplica dos sombras superpuestas.

✅ **Sombras internas (`inset`):**  
```css
div {
    box-shadow: inset 4px 4px 10px rgba(0, 0, 0, 0.5);
}
```
La palabra clave `inset` coloca la sombra dentro del elemento, en lugar de fuera.

---

**Control de la Repetición de Bordes (`border-image-repeat`)**  

La propiedad `border-image-repeat` controla cómo se repite la imagen del borde entre las esquinas del elemento.  

✅ **Valores disponibles:**  
- `stretch`: Estira la imagen para llenar el borde (valor por defecto).  
- `repeat`: Repite la imagen en su tamaño natural.  
- `round`: Similar a `repeat`, pero escala la imagen para ajustarla perfectamente al espacio disponible.

✅ **Ejemplo:**  
```css
div {
    border-image-repeat: stretch round;
}
```
Esto estira el borde horizontalmente y lo redondea verticalmente.

---

**Desbordamiento del Borde (`border-image-outset`)**  

Esta propiedad controla cuánto sobresale la imagen del borde fuera del contenedor del elemento.  

✅ **Ejemplo:**  
```css
div {
    border-image-outset: 10px;
}
```
Esto hace que la imagen del borde se extienda 10px fuera del contenedor.

---

**Soporte entre Navegadores**  

✅ **Compatibilidad actual:**  
| Propiedad         | Chrome | Firefox | Safari | IE 11+ |
|------------------|--------|---------|--------|--------|
| `border-radius`  | Sí     | Sí      | Sí     | Sí     |
| `border-image`   | Sí     | Sí      | Sí     | Sí     |
| `box-shadow`     | Sí     | Sí      | Sí     | Sí     |

---

**7. Resumen Final**  

El módulo de Bordes y Fondos de CSS3 ofrece herramientas poderosas para mejorar la presentación visual de las páginas web. Gracias a estas propiedades, los diseñadores web pueden lograr efectos sofisticados sin depender de imágenes de fondo complejas ni HTML adicional, reduciendo el peso de las páginas y mejorando el rendimiento.  
