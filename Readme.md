# **Resumen detallado del Capítulo 5: Fuentes Web**  

El capítulo 5 se centra en la tipografía web y cómo CSS3 permite a los diseñadores utilizar fuentes personalizadas en sus páginas mediante la regla `@font-face`. Anteriormente, los diseñadores estaban limitados a un pequeño grupo de "fuentes seguras para la web" que estaban preinstaladas en la mayoría de los sistemas operativos, como Arial, Times New Roman o Verdana. Sin embargo, `@font-face` permite especificar y cargar fuentes personalizadas desde un servidor, lo que amplía enormemente las opciones tipográficas disponibles para los desarrolladores.  

**Uso de `@font-face`**  
Para usar una fuente personalizada en un sitio web, primero se debe definir en CSS con `@font-face`. Esta regla permite indicar el nombre de la fuente, su ubicación y su formato de archivo. Una vez definida, la fuente puede usarse como cualquier otra fuente en una hoja de estilos.  

Por ejemplo, la siguiente declaración define una fuente personalizada llamada `MiFuente` y luego la aplica a los encabezados de la página:  

```css
@font-face {
    font-family: 'MiFuente';
    src: url('MiFuente.woff2') format('woff2'),
         url('MiFuente.woff') format('woff');
}

h1 {
    font-family: 'MiFuente', sans-serif;
}
```

Esto permite que los navegadores descarguen la fuente y la apliquen al texto sin que el usuario necesite instalarla en su sistema.  

**Compatibilidad de formatos de fuentes**  
Dado que los navegadores no admiten los mismos formatos de fuente, se recomienda proporcionar múltiples formatos para garantizar compatibilidad. Los formatos más comunes son:  

- **WOFF (Web Open Font Format):** Optimizado para la web y ampliamente soportado.  
- **WOFF2:** Versión mejorada de WOFF con mejor compresión.  
- **EOT (Embedded OpenType):** Requerido para versiones antiguas de Internet Explorer.  
- **TTF (TrueType Font) y OTF (OpenType Font):** Compatibles con muchos sistemas operativos, pero menos optimizados para la web.  

Para garantizar compatibilidad con todos los navegadores, se puede utilizar la siguiente sintaxis "a prueba de balas":  

```css
@font-face {
    font-family: 'MiFuente';
    src: url('MiFuente.eot'); /* Para IE9 y versiones anteriores */
    src: url('MiFuente.eot?#iefix') format('embedded-opentype'),
         url('MiFuente.woff2') format('woff2'),
         url('MiFuente.woff') format('woff'),
         url('MiFuente.ttf') format('truetype');
}
```

**Manejo de diferentes variantes de fuente**  
Si una fuente tiene diferentes versiones (negrita, cursiva, etc.), cada variante debe definirse por separado dentro de `@font-face` para evitar que los navegadores creen versiones artificiales, lo que podría afectar la calidad visual del texto.  

```css
@font-face {
    font-family: 'MiFuente';
    font-weight: bold;
    src: url('MiFuente-Bold.woff') format('woff');
}
```

**Problemas de rendimiento y soluciones**  
Uno de los principales problemas de usar fuentes web es el tiempo de carga. Las fuentes deben descargarse antes de mostrarse, lo que puede causar un "flash" de texto sin estilo (FoUT, Flash of Unstyled Text). Para mitigar esto, se recomienda:  

1. **Minimizar el número de fuentes utilizadas** para reducir el tiempo de descarga.  
2. **Usar Web Font Loader**, una biblioteca de Google y Typekit que permite controlar la carga de fuentes para mejorar la experiencia del usuario:  

```js
WebFont.load({
    google: {
        families: ['Droid Sans', 'Droid Serif']
    }
});
```

**Propiedades adicionales de fuentes en CSS3**  
Además de `@font-face`, CSS3 introduce propiedades avanzadas para mejorar la tipografía en la web:  

- **`font-size-adjust`:** Ajusta el tamaño del texto basado en la altura de x de la fuente, mejorando la legibilidad.  

```css
p {
    font-size-adjust: 0.5;
}
```

- **`font-stretch`:** Permite modificar el ancho de los caracteres de una fuente, aunque no todos los navegadores lo soportan.  

```css
h1 {
    font-stretch: expanded;
}
```

**Conclusión**  
El uso de `@font-face` ha revolucionado la tipografía en la web, permitiendo una mayor personalización y mejor control sobre el diseño. Sin embargo, es importante optimizar la carga de fuentes para evitar problemas de rendimiento. Además, las propiedades avanzadas como `font-size-adjust` y `font-stretch` proporcionan un control adicional sobre la apariencia del texto, mejorando la experiencia del usuario en distintos dispositivos y navegadores.  

---
