# **Resumen del cap 14**

**📌 Capítulo 14: Transiciones y Animaciones en CSS3**  
CSS3 introdujo **transiciones y animaciones** para agregar movimiento y dinamismo a las páginas web sin necesidad de JavaScript.  

**🔹 Diferencias Claves**
1. **Transiciones**: Ocurren **solo cuando hay un cambio de estado**, como `hover`.  
2. **Animaciones**: Se ejecutan **automáticamente** con keyframes, sin necesidad de eventos.  

---

**🔹Propiedades Clave de Transiciones**
- **`transition-property`**: Define qué propiedad CSS se animará.  
- **`transition-duration`**: Duración de la transición (ej. `2s`).  
- **`transition-timing-function`**: Controla la velocidad del cambio (`ease`, `linear`, etc.).  
- **`transition-delay`**: Retrasa el inicio de la transición.  

Ejemplo básico:  
```css
div {
    background-color: black;
    transition: background-color 2s;
}
div:hover {
    background-color: silver;
}
```
Cuando pasas el mouse, el fondo cambia de negro a plateado suavemente.  

---

**🔹Propiedades Clave de Animaciones**
- **`@keyframes`**: Define los pasos de la animación.  
- **`animation-name`**: Nombre de la animación.  
- **`animation-duration`**: Duración total de la animación.  
- **`animation-iteration-count`**: Veces que se repetirá (`infinite` para siempre).  
- **`animation-direction`**: Sentido de la animación (`normal`, `reverse`, `alternate`).  

Ejemplo básico:  
```css
@keyframes mover {
    0% { transform: translateX(0); }
    100% { transform: translateX(100px); }
}
div {
    animation: mover 2s infinite alternate;
}
```
Esto mueve el elemento 100px a la derecha y luego regresa.  
