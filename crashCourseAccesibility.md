### Hablemos de las leyes qua acobijan la accesibildad web

La accesbilidad suele asociarse con derechos fundamentales o el derecho a diferentes servicios, por tanto, diferentes paises han creado leyes para mejorar el acceso de las personas con diferentes discapacidades o limitación de recursos a páginas o aplicaciones de toda índole, a continuación se nombran algunas:

- Section 508 of Rehabilitation Act - Estados Unidos
- Directive (EU) 2016/2102 - Unión Europea
- Ley 1618 de 2013 - Colombia

Muchas de las leyes abogan por cumplir mínimamente con el estándar intermedio (AA) de la WCAG.

### Hablemos de por qué nos importa la accesibilidad

Hay diferentes aspectos por los cuales nos importa la accesibilidad en nuestros sitios web, algunos de ellos son:

- Muchas personas están utilizando nuestros sitios web's
- 20% de las personas a nivel mundial cuentan con un tipo de discapacidad, y 62% de ellos no lo comentan en público.

### POUR Principal

La WCAG aboga por cumpir principios básicos para mejorar nuestra accesibilidad en la web (ver figura), dichos principios son:

- Perceptible (referente a la visión y la audición)
- Operable (Hace referencia a limitaciones o discapacidades motoras)
- Understandable (Hace referencia a discapacidades cognitivas)
- Robust (Este aplica tanto para discapacidades motoras como cognitivas)

(Poner aquí figura pour-image.png)

Ahora, una forma de resumir la manera de mejorar nuestros sitios web atacando los principios anteriores:

- Hacer nuestra web accesible por medio del teclado
- Dejar suficiente tiempo en aniamaciones o notificaciones para que la persona pueda percibirlas
- Verificar tamaños de letra y contrastes de colores
- Hacer nuestra página web navegable por diferentes tecnologías asistivas, para este punto puedes apoyarte en el árbol de accesibilidad.
- Tener texto alternativo para contenido no textual, ejemplo: Imagénes, audios y videos. Para los videos y los audios se espera que los textos alternativos (caption) sean automáticos.
- Lista tu contenido programáticamente, utiliza correctamente las jerarquías de los haedings y usa el HTML semántico para dar la mejor experiancia de navegación.
- No uses una característica para demostrar un cambio en tus elementos web, por ejemplo no utilices sólo colores para mostrar que señalas un botón, ya que hay personas con discapacidades visuales que no le permiten percibir este cambio. Por tanto, utiliza colores, cambio de tamaño del componente o el texto para demotrar dicha interacción.
- Permite a los usuarios elegir la orientación de tu web, debido hay hay personas que acceden desde diferentes dispositivos, y se les facilita acceder al contenido cambiando la orientación del mismo.
- Ayuda a los usuarios a autocompletar inputs o entradas comunes, ya que personas con discapacidades cognitivas no siempre sabrán cómo utilizar estos componentes.
- Asegurate de que el contraste del color para el texto que utilizas sobre fondos o imágenes posea un mínimo de 4.5:1.
- Valida que el contraste de los colores que utilizas para imagénes informativas (UI) tengan un contraste mínimo de 3:1.
- Asegurate que el texto de tu aplicación puede aumentarse hasta en un 200%.
- Valida que tus elementos que poseen hover también posean un focus.
- Asegurate de no tener trampas de teclado,en otras palabras, que al navegar con el teclado nos encontremos con elementos que eviten que podamos seguir navegando con el teclado.
- Habilita el tiempo ajutable, esto cuenta tanto para notificaciones, expiraciones de sesión,etc. Por tanto se recomienda que se pueda ajustar este tiempo a 10 veces la unidad por defecto, se pueda apagar el límite de tempo o en caso de las expiraciones de sesión se genere una notificación 20 segundos antes de finalizarla, así los usuarios no perderán datos o progreso en la app.
- Permite que tus usuarios posean controles de pausa, stop y ocualtar en contenido que posea movimiento.
- Elimina contenido que posea más de tres flashes por segundo, esto para personas que sufren de epilepcia.
- Crea bloques de Bypass en contenidos que se repiten en diferentes páginas, un ejemplo de esto es el uso de Skip links y Skip buttons en el menú (header), pero recuerda que debes contar con estos mecanismos en el footer, menús laterales, etc.
- Asegurate de que cada página de tu web posea una etiqueta h1, que además contenga una descripción simple de lo que se puede encontrar en la página web.
- Los links poseen una descripción clara de lo que hacen.
- Verifica que poseas opciones al drag and drop de documentos u otras interacciopnes, debido que hay personas que no pueden usar muy bien su mouse, o al hacerlo pueden activar otros recursos que les puede causar molestias.
- Asegurate de poseer diferentes maneras de encontrar una página en tu sitio, por ejemplo: barras de bpusqueda, tabal de contenidos, mapa del sitio, barras de navegación, etc. Así puedes facilitarle a las personas el encontrar tu contenido. Sin emebargo, este consejo no cuenta cuando la página es el resultado de una acción o el paso de un proceso que se esté realizando.
- El focus que le añadas a tue elementos deben ser visibles y claros.
- Asegurate de que tu página posea un lenguaje asignado, así los lectores de pantalla pueden ser configurados adecuadamente.
- Si utilizas palabras o frases en otro lenguaje, asegurate de que se puede establecer dicho lenguaje por medio de programación.
- Asegurate de que los inputs de tus formularios posean una cambio cuando tienen un foco.
- Recuerda establecer mecanismos para reversar, confirmar o corregir submissions de cualquier formulario, o de procesos que tengan que ver con información legal, datos o información financiera.

Nota importante:
Las herramientas automáticas para evaluar la accesibilidad no son recomendables para evaluar el contraste de nuestros colores, por tanto, la mejor manera de evaluar este contraste es de manera manual.
