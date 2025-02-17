# Resumen del captilo 13 


 **📌 Capítulo 13: Transformaciones 3D en CSS3**
Las transformaciones **3D** en CSS permiten manipular elementos en tres dimensiones utilizando el **eje Z**, además de los ejes X e Y utilizados en las transformaciones 2D. Esto se logra con la propiedad **transform** y sus diversas funciones.

 **🔹 Conceptos Claves**
1. **Ejes en el espacio tridimensional**:
   - **X**: Izquierda ↔ Derecha
   - **Y**: Arriba ↔ Abajo
   - **Z**: Hacia adelante ↔ Atrás

2. **Funciones de Transformación 3D**:
   - **rotateX(ángulo)**: Rotación en el eje X.
   - **rotateY(ángulo)**: Rotación en el eje Y.
   - **rotateZ(ángulo)**: Rotación en el eje Z.
   - **translate3d(x, y, z)**: Mueve un elemento en los tres ejes.
   - **scale3d(sx, sy, sz)**: Escala un elemento en 3D.
   - **perspective(valor)**: Define la profundidad de la perspectiva.

3. **Propiedad `transform-style`**:
   - **flat**: Aplana elementos 3D en el mismo plano.
   - **preserve-3d**: Mantiene la profundidad en los elementos anidados.

---

**🎨 Ejemplo: Caja Giratoria en 3D**
Este código muestra un **cubo que rota en 3D** cuando pasas el mouse sobre él.  
