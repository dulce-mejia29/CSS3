# **Capítulo 12: Transformaciones 2D**

Debido a la forma en que funciona HTML, con cada elemento compuesto por bloques rectangulares y esquinas en ángulos rectos, las páginas web tradicionalmente han parecido cuadriculadas, con muchas líneas horizontales y verticales rectas. La única manera de proporcionar alguna variación a esta regla era usar imágenes. Pero en 2008, el equipo de WebKit propuso un nuevo módulo que permite rotar, escalar, inclinar y, en general, modificar los elementos. Este módulo fue adoptado para su estandarización por el W3C y formalizado como el **Módulo de Transformaciones 2D** (http://www.w3.org/TR/css3-2d-transforms/).

Gran parte del proceso de transformación de elementos fue adaptado de funciones en el lenguaje **Scalable Vector Graphics (SVG)**, que se usa para dibujar imágenes vectoriales bidimensionales. SVG es compatible con la mayoría de los navegadores modernos, por lo que Firefox y Opera implementaron rápidamente las Transformaciones 2D en sus productos, y IE9 siguió poco después.

Las propiedades de transformación para CSS y SVG eran tan similares que el W3C decidió fusionarlas en una única especificación común: **CSS Transforms** (http://dev.w3.org/csswg/css-transforms/), que es donde continúa el desarrollo del módulo. A pesar de que este módulo de CSS Transforms aún es un **Borrador de Trabajo**, las propiedades que incluye están bien implementadas y se pueden utilizar de inmediato.

**La Propiedad transform**

Se pueden aplicar una variedad de transformaciones diferentes, pero todas se declaran como funciones dentro de la propiedad **transform**. Aquí está la sintaxis básica:

```css
E { transform: function(valor); }
```

Hay varias funciones disponibles; exploraremos cada una de ellas a lo largo de este capítulo. Cada función acepta un solo valor o una lista de valores separados por comas. También explicaremos qué significa esto en cada caso específico.

Se pueden aplicar múltiples transformaciones a un solo elemento simplemente listando las funciones separadas por espacios en la propiedad **transform**:

```css
E { transform: function(valor) function(valor); }
```

Es importante tener en cuenta un aspecto clave al usar la propiedad **transform**, pero antes de hablar de eso, es necesario presentar las diferentes funciones.

**rotate**

Probablemente, la más sencilla de todas las funciones de transformación es **rotate()**, que hace exactamente lo que su nombre indica: rota el elemento alrededor de un punto fijo. Aquí está la sintaxis:

```css
E { transform: rotate(valor); }
```

El valor aquí es un único valor de ángulo, al igual que en los gradientes CSS introducidos en el Capítulo 11. Como en ese capítulo, nos quedaremos con los grados (deg) para nuestros ejemplos.

Para mostrar **rotate()** en acción, vamos a rotar un elemento `<h2>` en **−15 grados** (o 345 grados) usando esta regla:

```css
h2 { transform: rotate(-15deg); }
```

**Soporte en Navegadores para Transformaciones 2D**

Como se mencionó al inicio del capítulo, la compatibilidad con las transformaciones 2D es bastante amplia, aunque no todos los navegadores admiten la propiedad **transform** sin un prefijo de proveedor. IE9, Safari y versiones antiguas del navegador de Android requieren un prefijo, lo que significa que para usar esta propiedad actualmente, hay que especificarla tres veces:

```css
E {
    -ms-transform: function(valor); /* IE9 */
    -webkit-transform: function(valor); /* WebKit */
    transform: function(valor);
}
