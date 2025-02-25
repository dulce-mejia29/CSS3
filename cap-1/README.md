# Introducing cSS3
Al principio solo nos da a conocer y explicar la historia de CSS3 y un poco de como funciona

**¿Que es CSS3 y como funciona?**

Qué es CSS3 y la forma que adopta: El enfoque del W3C hacia CSS3 es bastante diferente de su enfoque hacia CSS2, por lo que esta descripción general debería ayudarlo a comprender cómo y cuándo puede usar CSS3 y por qué tiene una implementación tan variada en diferentes navegadores.

**Mini Historia**

La última versión principal de CSS fue CSS2.1, una revisión de la especificación CSS2 que se publicó originalmente en 1997. A pesar del desarrollo y la revisión continuos desde entonces, muchas personas se sorprenden al saber que CSS2 solo se convirtió en una recomendación "oficial". del W3C en 2011. Aún más sorprendente es el hecho de que Internet Explorer 8 (IE8), lanzado en 2009, afirma ser el primer navegador compatible con el Completamente toda la especificación CSS2.1.

En los últimos años, se ha hablado de la nueva revisión: CSS3. Digo "nuevo", pero de hecho el trabajo en CSS3 comenzó en 1998, un año después de la publicación de CSS2. Sin embargo, la implementación de CSS2 en el navegador siguió siendo tan frustrantemente inconsistente que el W3C decidió detener el trabajo en cualquier nueva revisión y trabajar en CSS2.1, estandarizando la forma en que se había implementado CSS en el mundo real. En 2005, todos los módulos CSS3 volvieron al estado de Borrador de trabajo y el proceso de edición y revisión comenzó nuevamente.

Durante muchos años, Internet Explorer dominó el mercado de usuarios de Internet en constante expansión y no dio señales de querer implementar CSS3. Pero en los últimos diez años, ha aparecido una gama completamente nueva de navegadores que compite por los usuarios, y esta plétora de opciones ha llevado a una carrera armamentista de funciones. Uno de los beneficiarios de esa carrera armamentista ha sido CSS3. Cada uno de los navegadores quiere ofrecer a los desarrolladores y usuarios lo último en tecnologías web, y con la especificación CSS3 ya escrita en su mayor parte, implementar e incluso agregar nuevas características ha sido una obviedad.

**CSS3 es modular**

Crear el lenguaje de estilo predeterminado para cada documento basado en marcas del mundo es una tarea enorme, y el W3C era consciente de que llevaría muchos años llegar a buen término. Los miembros del W3C, conscientes de que no querían retrasar algunas de las características más obvias y demandadas mientras consideraban y debatían algunas de las más esotéricas, tomaron la decisión de dividir CSS3 en varios módulos. Luego, diferentes autores podrían trabajar en cada uno de los módulos a diferentes ritmos, y el proceso de implementación y recomendación (que analizaré en breve) podría escalonarse. 

Esta es la razón por la que, en lugar de un documento de especificación CSS3 único y monolítico, tiene el módulo de interfaz de usuario básico CSS3, selectores de nivel 3, consultas de medios, etc. Algunos de estos módulos son revisiones de CSS2.1 y otros son de nueva creación, pero todos están bajo el nombre de CSS3.

Una de las pocas cosas que encuentro irritante (soy una persona tranquila) es que en muchos blogs escucharás a la gente quejarse: "Quiero usar CSS3, pero no estará listo en años". Esto es una tontería; Algunos módulos CSS3 ya tienen una implementación bastante estable en todos los navegadores modernos, y muchos más están a sólo unos meses de su horario de máxima audiencia. Si desea esperar hasta que todos los módulos estén implementados al 100 por ciento en todos los navegadores existentes, estará esperando una eternidad.

Así que CSS3 está aquí, y parte de él está listo para usar ahora mismo; solo debes tener en cuenta cómo lo usas.

**No hay CSS3**

A medida que CSS se ha vuelto modular, a cada módulo se le asigna un número de nivel para marcar cuántas revisiones ha pasado. Algunos de los módulos más maduros, como los Selectores, ya se encuentran en el Nivel 4; muchos de los módulos que aparecen en este libro, como las fuentes, están en el nivel 3; mientras que algunos módulos muy nuevos, como Flexbox, solo están en el nivel 1 o posiblemente pasen al nivel 2.

Lo que esto significa es que CSS es un estándar de vida: como mencioné anteriormente, no habrá más versiones monolíticas; cada módulo avanzará a su propio ritmo; y se agregarán nuevos módulos a medida que se alcancen nuevas funciones. CSS3 es simplemente una abreviatura conveniente para significar "funciones CSS desarrolladas desde CSS2.1". CSS4 nunca existirá. Con el tiempo, la numeración desaparecerá y solo tendremos CSS, con módulos en diferentes niveles.

¡Pero no nos dejemos disuadir! Continuaré refiriéndome a CSS3 en este libro en el sentido en que se definió anteriormente, como una abreviatura conveniente para las nuevas características de CSS. ¡Esta etiqueta facilita la comprensión y significa que no tengo que cambiar el título de este libro!

**Estado del módulo y proceso de recomendación**

A medida que avanzo en este libro y analizo cada uno de los diferentes módulos, a veces me referiré al estado de ese módulo. El estado lo establece el W3C e indica el progreso del módulo a través del proceso de recomendación; Sin embargo, tenga en cuenta que el estado no es necesariamente una indicación del grado de implementación de un módulo en cualquier navegador.

Cuando un documento propuesto se acepta por primera vez como parte de CSS3, su estado se denomina Borrador de trabajo. Este estado significa que el documento ha sido publicado y ahora está listo para ser revisado por la comunidad; en este caso, la comunidad está compuesta por fabricantes de navegadores, grupos de trabajo y otras partes interesadas. Un documento puede permanecer como borrador de trabajo durante un largo período y sufrir muchas revisiones. No todos los documentos superan este nivel de estado y un documento puede volver a este estado en muchas ocasiones.

## presentando la sintaxis

utilizo cierta convención sintáctica para demostrar cada una de las nuevas reglas y propiedades. Se parece a esto:
````
mi { propiedad: valor; }
````
En este ejemplo de código, el selector se representa con E. Por supuesto, en HTML, este selector no existe; Simplemente lo estoy usando para indicar que el selector es irrelevante; aquí se podría utilizar cualquier selector.

A continuación, tienes la propiedad en sí; En este caso, he usado una propiedad inventada, llamada propiedad. A continuación se muestra el valor de la propiedad. Para esto, uso un alias en cursiva para referirme al valor, que en este caso he llamado valor.

Si una propiedad acepta varios valores, enumeraré cada uno con un alias único.

Entonces, una nueva propiedad que requiere tres valores podría definirse así:

E { propiedad: primero segundo tercero; }


Presentando CSS3 5

Dicho todo esto, supongamos que tenemos una nueva propiedad llamada monos (siempre he querido una propiedad de monos), que acepta solo un valor único. Usando la sintaxis de este libro, lo presentaría así:
````
E { monos: valor; }
Y cuando llegara el momento de proporcionar un ejemplo práctico, podría mostrarlo con un valor válido (digamos, un valor numérico) como este:
mi { monos: 12; }
````


# Prefijos de proveedores


Cuando un módulo todavía está bajo revisión activa, muchas cosas están sujetas a cambios; la sintaxis de una propiedad puede revisarse o una propiedad puede eliminarse por completo. En ocasiones, incluso la redacción del proyecto en sí es quizás un poco confusa y abierta a interpretación.

Al mismo tiempo, los navegadores deben implementar estas funciones para que podamos ver cómo funcionan en la práctica. Pero considere las dificultades que ocurrirían si dos navegadores separados implementaran la misma propiedad pero la interpretaran de manera inconsistente: el resultado de su código aparecería de manera diferente (quizás radicalmente) en cada uno de los navegadores. Para evitar que esto suceda, cada uno de los proveedores de navegadores comenzó a anteponer un código corto al comienzo de las propiedades experimentales. Imaginemos que nuestra tan deseada propiedad monos se ha definido recientemente en una especificación y que todos los principales proveedores de navegadores han decidido implementarla para ver cómo funciona. En este caso, usaría el siguiente código:
````
E {

-moz-monkeys: value; /* Firefox */

-ms-monkeys: value; /* Internet Explorer */

-webkit-monkeys: value; /* Chrome/Safari */

}
````

La cantidad de repetición puede parecer algo innecesaria, pero la repetición es por nuestro propio bien; Lo último que desea es que todos los navegadores implementen la propiedad monos de manera diferente, lo que llevaría al caos total.

Aunque bien intencionado, el uso de prefijos de proveedores ha generado muchos problemas: los desarrolladores los usaron en sus sitios web de producción pero no los eliminaron más tarde cuando la implementación del navegador cambió. Esto, a su vez, significó que los proveedores de navegadores tienen que seguir admitiendo funciones experimentales para siempre para evitar roturas en los sitios web que las utilizan. Debido a esto, Chrome y Firefox ahora están dejando de usar propiedades prefijadas y prefieren implementar nuevas funciones que están deshabilitadas de forma predeterminada y que los desarrolladores deben habilitar hasta que sean lo suficientemente estables para un uso generalizado. Dicho esto, todavía existen muchas propiedades con prefijo y anotaré en el libro cuándo debes usarlas.
