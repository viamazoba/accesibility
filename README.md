# Accesibility

La accesibilidad es la práctica continua de asegurarnos que todo lo que creamos para la web se puede usar, interpretar y operar por una variedad de personas en una variedad de situaciones.

Nota: Cuando estés buscándo recursos de accesibilidad es útil buscar con el numerónimo **a11y**, pues es una manera de resumir la palabra accesibility (ver imagen):

(Colocar imagen de accesibilidad)

Importancia de la accesibilidad

- Se estima que alrededor del 20% de la población mundial cuenta con alguna discapacidad, así que aplicar la accesibilidad es casi un llamado moral para los desarrolladores.

- Para mejorar la usabilidad y versatilidad de nuestros proyectos. Por ejemplo, el modo de vibración nació para las personas que no pueden escuchar, pero ahora lo utilizamos para variedad de situaciones.

- En algunos paises por ley debe ser aplicada.

### Ver también

(Colocar noticias de demandas)
https://www.cnbc.com/2019/10/07/dominos-supreme-court.html

## Criterios para hacer una web accesible

La WCAG (Web Content Accessibility Guidelines) nos da las diferentes pautas o check list que debemos considerar para hacer una aplicación accesible. Esta guía fue creada por la W3C (World Wide Web Consortium), la cuál es una organización que genera diferentes estándares que utilizamos en la web, donde se generó la iniciativa WAI (Web Accesibility Iniciative) que tiene como meta asegurar la accesibilidad web.
Ten presente que actualmente vamos en la versión 2.2, pero ya se encuentra en desarrollo la versión 3.0, además que WCAG tiene 12 criterios para implementar la accesibilidad, los cuales tienen tres nieveles de conformidad:

### Criterios de conformidad de la WCAG

- A: Este es el nivel básico, y por tanto el que requiere la menor inversión. Se considera que a este nivel el sitio casi no cuenta con accesibilidad.
- AA: Nivel intermedio de implementación, ya se considera que el sitio es accesible.
- AAA: Este es el mayor nivel de implementación, y por tanto, el que mayor nivel de incversión requerida. Este nivel lo suelen implementar entes gubernamentales, universidades o servicios escenciales de la vida cotidiana.

Dentro de los niveles anteriores vamos a encontrar los siguientes principios:

1. Perceptible
   Este principio se enfoca en asegurar que un contenido se pueda entender de diferentes maneras:

_hint_

- Generar alternativas textuales para contenido no textual, por ejemplo subtítulos para imágenes o videos.

2. Operable
   Este principio hace enfasis en que nuestra aplicación sea fácil de usar y se pueda navegar de diferentes maneras: mouse y/o teclado.

_hint_

- Dar suficiente tiempo a los usuarios para leer y usar el contenido.
- No usar elementos brillantes o que se muevan muy rápido, ya que pueden provocar ataques, espamos o convulciones.
- Asegurarnos de una navegación simple, donde el usuario pueda determinar donde se encuentra en nuestro sitio.

3. Comprensible
   Este principio busca asegurar que personas con discapacidades cognitivas puedan encontrar patrones comunes para saber cómo usar la web, y personas sin tiempo puedan consultar algo rápidamente.

_hint_

- Tener en cuenta tamaños de texto y el color de fondo para generar un contraste adecuado.
- Hacer que las páginas operen de manera predecible.
- Dar instrucciones para evitar errores y oportunidades para corregirlos cuando ocurren.

4. Robusto
   Este principio busca que nuestras aplicaciones puedan funcionar en diferentes dispositivos móbiles, navegadores y dispositivos asistivos, además que posea un buen rendimiento para personas que no tienen buen acceso a internet.

Nota: La WCAG 2.0 cuenta con traducciones autorizadas, sin embargo la cantidad de autorizaciones para las versiones más recientes aún son pocas.

## Tecnologías asistivas

Son alternativas a las existentes para mejorar nuestras habilidades para consumir el mundo que nos rodea. Entre las tecnologías asistivas para la web tenemos:

- Lectores de pantalla: Software que interpretan los sitios y los leen en voz alta.
- Extensiones que manipulan el CSS: Cambian los estilos del sitio para ayudar a las personas de forma visual, por ejemplo, manipular el tamaño del texto o el foco de un elemento.

_hint_

- La navegación por teclado es muy importante, ya que por medio de este muchas tecnologías asistivas se sirven para sus respectivas funcionalidades.

## Lighthouse

Es una herramienta que nos provee chrome para evaluar diferentes características de nuestras aplicaciones como SEO, accesibilidad, rendimiento, etc. Además nos permite evaluar dichas características tanto desktop como en mobile.
Para acceder a Lighthouse debes inspeccionar la página a evaluar y buscar entre las opciones (consola, elements, network, etc.) a lighthouse.

## Otras herramientas

### Enfermedades visuales

Hay personas que pueden contar con discapacidad visual como: Visión borrosa, Protanopia, Deuteranopia y Acromatopsia. Estas discapaciades impiden la visualización de ciertos colores o formas, por tanto se pueden utilizar herramientas como **rendering** de chrome, el cual nos permite simular diferentes tipos de discapacidad visual. Para acceder a esta herramienta: Busca en la barra que nos aparece en el navegador (console, elements, network, etc.) vamos a más opciones y buscamos rendering cómo se muestra en la imagen a continuación:

(colocar aquí imagen de rendering)

Otra herramienta que puedes utilizar para la web es una proporcionada por **userway** (colocar link), la cual puedes implementar en el front de tu aplicación de manera sencilla, y esta te ayudará cambiando los colores de manera automática en tu aplicación, además de generar ayudas para la lectura de tu contenido, como agrandar el tamaño de la letra o proveer elementos guía. Esta herramienta tiene una versión gratuita, pero con la versión paga tendrás muchas más funcionalidades.

_hint_
La idea es no utilizar sólo colores para mostrar algo importante o una interacción, ya que puedes utilizar animaciones para mejorar la navegación.

**Screen reader** es una extensión de chrome que nos sirve para simular cómo una persona con discapacidad visual puede navegar, ya que esta extensión lee las acciones que realizamos.

Nota: Los otros navegadores poseen otras herramientas para leer la pantalla en una página web, sin embargo chrome tiene las herramientas más actualizadas. Además, cada sistema operativo posee lectores de pantalla, por tanto debes consultar cómo activar tu lector de pantalla para realizar pruebas en tu web.

### Pruebas con teclado

El teclado es muy importante, ya que sirve como base para muchas tecnologías asistivas, sin embargo en web debemos tener mucho cuidado con elementos que disponemos para mostrar información, ya que sólo etiquetas de link y de formulario se pueden acceder desde el teclado (mediante tab), por ello si deseas colocarle acceso por teclado a un elemento diferente a estos debes programarlo con atrinutos como _tabindex_.

## Consideraciones para lectores de pantalla

1. Uso de HTML semántico: Le agrega significado a los elementos a nuestra página web pero de cara al navegador, así el navegador puede crear fácilmente un árbol de accesibilidad que le ayude con la lectura de la página. En la imagen que se muestra a continuación se muestra la manera de visualizar el árbol de aceesibilidad en chrome:
   (poner imagen de árbol de accesibilidad)

2. Consideraciones para las etiquetas HTML:

- atributo _alt_ para la etiqueta **img** es importante porque es la descripción de la imagen que el lector de pantalla va a utilizar.
- ARIA (Accesible Rich Internet Applications), es un conjunto de atributos especiales para accesibilidad que pueden añadirse a cualquier etiqueta, pero especialmente adaptado a HTML. Esta tiene tres atributos: roles, propiedades y estados.

### ARIA role

Los ARIA roles preparan al navegador o lectores de pantalla a indicar cuales son las interacciones que debería esperar, se usan en ocasiones especiales, en la mayoría de los casos se recomienda usar HTML semántico.

### ARIA properties

Comunican atributos que son escenciales para el comportamiento o significado de un elemento, pero que se suele comunicar visualmente, por ejemplo:

- Hay botones como los utilizados en los carruseles que son hechos con divs, por tanto el navegador ni un lector de pantalla sabe a que se refiere dicho elemento, así que al colocar un aria-label puedo establecer un nombre descriptivo.

### ARIA states

Comunican estados y cambios de estados en elementos que se suelen comunicar visualmente. Por ejemplo:

- Cuando presionas un check button para una persona con discapacidad visual no es posible ver dicho cambio al darle click al botón.
- Los carruseles suelen ocualtar cards, pero para un lector de pantalla siempre están todas las cards, por ello comunicará que todos los elementos están visibles.

Documentación para ARIA states y properties: https://www.w3.org/TR/wai-aria-1.0/states_and_properties

## Ayudas de CSS

Chrome al inspeccionar elementos te permite saber si el color que estás utilizando posee un contraste correcto, en la siguiente imagen se muestra donde verificar el contraste:

(colocar imagen de contraste)

_hint_
Existen herramientas como **swach** para los diseñadores para validar si los colores que se utilizan en tu sitio web poseen el contraste adecuado, lo puedes consultar aquí: https://www.swach.io/

## Iconos

Para la mayoria de personas no siempre es claro el significado de los iconos, por ello se recomienda colocar texto a los iconos para reconocerlos más facilmente. Esto es especialmente util para los iconos de redes sociales.

(colocar iconos con texto)

## Skip link

Este es un botón o enlace que se posiciona al principio de nuestra página para que las personas que ingresan por teclado tengan la posibilidad de ingresar al contenido principal sin tener que pasar por todo el menú de la página. Ya que podemos tener un menú demasiado extenso y puede ser tedioso navegar por este antes de llegar al contenido.

_hint_
El skip link es invisible, y sólo aparece al hacer focus y active, por ello en sus propiedades se establece dicho comportamiento.

## Estilos de focus y hover

Se recomienda dar propiedades CSS a los elementos, por ejemplo no dejar sin estilos el focus de los elementos, ya que normalmente se suelen olvidar, y las personas que ingresan por teclado solo tienen estar forma de saber si están sobre un elemento, debido a que no pueden visualizar el hover.

_hint_
Puedes utlizar otro tipo de propiedades como **focus-within** que te ayuda a dar focus sobre un elemento cuando se intenta dar foco a un elememento hijo.

## Uso de JavaScript para accesibilidad

La idea en la ccesibilidad es que puedas darle a todas las personas que ingresan a tu sitio una navegación similar independiente a como ingresen, ya sea por teclado, mouse o lector de pantalla. Por tanto, hay ciertos componentes en nuestro sitio que van a requerir un tratamiento más sofisticado con JavaScript, ya que con HTML y CSS puede que no sea sufuciente para dar un buen nivel de interacción. Ejemplo de lo anterior:

- El trabajar con carruseles debes utilizar aria-hidden y tabindex, además de eventListener para ocultar cards y solo visualizarlas cuando se presionen los botones establecidos para esta tarea.
- En ciertos componentes como modales se requiere que la persona pueda hacer tab sobre ellos, entonces requieren un tabindex, pero también requieren ser cerrados mediante la tecla scape, y para ellos podemos utilizar addEventListeners.
- Para formularios
  aria-hidden y tabindex

* cerrar modales mediante escape

aria-required para decirle a los lectores de pantalla que un valor es obligatorio en un formulario

aria-live: Se utilizan para establecer la prioridad con la que el lector de pantalla debe tratar a cambios a las regiones en vivo - los valores posibles son: off, politeo assertive. La configuración predeterminada es off. Este atributo es, con mucho, el más importante.
