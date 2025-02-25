# Capítulo 2: Consultas de Medios

**Introducción a las Consultas de Medios**

En la era en la que la World Wide Web solo se accedía mediante navegadores en computadoras de escritorio o portátiles, escribir CSS era relativamente sencillo. Aunque era necesario considerar problemas de compatibilidad entre navegadores y plataformas, al menos se podía asumir con cierta certeza que todos los usuarios utilizaban dispositivos similares para visualizar el sitio web. Sin embargo, en los últimos años, hemos visto una explosión de nuevos dispositivos para acceder a la Web, desde consolas de videojuegos hasta dispositivos móviles como teléfonos inteligentes y tabletas. Presentar el contenido de la misma manera para todos los usuarios ya no tiene sentido cuando podrían estar viendo el sitio web en un monitor de escritorio de pantalla ancha o en una pantalla estrecha de un dispositivo portátil.

CSS ha ofrecido durante mucho tiempo una manera de aplicar estilos diferentes a distintos tipos de medios mediante el atributo media del elemento link:
````

<link href="style.css" rel="stylesheet" media="screen">

````
Sin embargo, este enfoque presenta varios inconvenientes, entre ellos que resulta ser una herramienta bastante rudimentaria cuando la pantalla en cuestión puede variar entre 3.5 pulgadas y 32 pulgadas. La lista de tipos es demasiado general y muchos no son compatibles con los dispositivos a los que están dirigidos; por ejemplo, no conozco ningún televisor con acceso a la Web que responda al tipo tv. No es de extrañar que el W3C haya comenzado a desaconsejar el uso de tipos de medios.

La solución de CSS3 a este problema es el uso de consultas de medios, definidas en el Módulo de Consultas de Medios. Estas consultas amplían los tipos de medios al proporcionar una sintaxis de consulta que permite aplicar estilos mucho más específicos al dispositivo del usuario, ofreciendo una experiencia personalizada. Aunque esta descripción pueda sonar un tanto técnica, esta característica es en realidad una de las más revolucionarias de toda la especificación de CSS3. Las consultas de medios te dan la libertad de crear sitios web verdaderamente independientes del dispositivo, brindando a los usuarios la mejor experiencia posible, sin importar cómo accedan a tu sitio.

El Módulo de Consultas de Medios tiene el estatus de Recomendación del W3C, por lo que se considera un estándar. Este módulo ya está bien implementado en todos los principales navegadores, incluyendo Internet Explorer a partir de la versión 9.

**Ventajas de las Consultas de Medios**

Como una demostración rápida del poder y la flexibilidad de las consultas de medios, mostraré un ejemplo de cómo los sitios web pueden optimizarse para navegadores móviles sin requerir un gran esfuerzo de desarrollo adicional.

Las personas que visitan tu sitio en un dispositivo móvil podrían tener dificultades para utilizarlo: el texto puede parecer demasiado pequeño, y al hacer zoom tendrán que desplazarse mucho para encontrar elementos de navegación; esos elementos de navegación podrían depender de funcionalidades desplegables activadas al pasar el cursor, una acción que a menudo no existe en dispositivos móviles; las imágenes grandes podrían tardar mucho tiempo en descargarse en una conexión débil y consumir una parte sustancial del plan de datos mensual del usuario. Algunos sitios abordan esto proporcionando versiones adaptadas para móviles, pero esto generalmente implica mucho trabajo de desarrollo: se debe configurar un subdominio con hojas de estilo y plantillas HTML que difieran del sitio principal; las imágenes deben redimensionarse para adaptarse mejor a pantallas pequeñas; y debe crearse un script para detectar si se está utilizando un navegador móvil y redirigir al sitio móvil en consecuencia. Este enfoque puede causar problemas: el script debe mantenerse actualizado con todas las versiones de navegadores móviles, y el mantenimiento a menudo implica duplicación para mantener sincronizadas las versiones móvil y de escritorio.

Las consultas de medios abordan muchos de estos problemas. Para empezar, detectan dispositivos basándose en sus atributos, por lo que no se requieren scripts de detección de navegadores. Permiten dirigirte directamente a las hojas de estilo según las capacidades del dispositivo, por lo que si se detecta un dispositivo con una pantalla pequeña, las reglas de CSS se adaptarán a ese tamaño de pantalla, eliminando elementos innecesarios, sirviendo imágenes más pequeñas y haciendo que el texto sea más legible.

**Sintaxis**

La sintaxis de una consulta de medios está compuesta por un tipo de medio y, opcionalmente, una o más expresiones que comprueban las condiciones de una o más características de los dispositivos. Estas consultas se especifican utilizando la regla @media de CSS. Por ejemplo, para aplicar estilos específicos a dispositivos con un ancho máximo de 480 píxeles, puedes escribir lo siguiente:
````

@media screen and (max-width: 480px) {
    body {
        font-size: 14px;
    }
}

````

En este caso, la consulta de medios asegura que el tamaño de fuente del cuerpo del documento sea de 14 píxeles solo cuando el ancho de la pantalla del dispositivo sea de 480 píxeles o menos.

**Características de los Medios**

Las consultas de medios utilizan características específicas de los dispositivos, como su ancho, alto, orientación, resolución y otras. A continuación, se describen algunas de las más comunes:

**Ancho y Alto:* Estas características especifican el ancho y el alto del área visible del dispositivo.

**Relación de Aspecto:* Permite definir estilos basados en la proporción entre el ancho y el alto de la pantalla.

**Resolución:* Utilizada para aplicar estilos en dispositivos con densidades de píxeles específicas, como pantallas Retina.

**Orientación:* Diferencia entre modo retrato y paisaje.
