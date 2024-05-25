# accesibility

La accesibilidad es la práctica continua de asegurarnos que todo lo que creamos para la web se puede usar, interpretar y operar por una variedad de personas en una variedad de situaciones.

Nota: Cuando estés buscándo recursos de accesibilidad es útil buscar con el numerónimo **a11y**, pues es una manera de resumir la palabra accesibility (ver imagen):

(Colocar imagen de accesibilidad)

Importancia de la accesibilidad

- Se estima que alrededor del 20% de la población mundial cuenta con alguna discapacidad, así que aplicar la accesibilidad es casi un llamado moral para los desarrolladores.

- Para mejorar la usabilidad y versatilidad de nuestros proyectos. Por ejemplo, el modo de vibración nació para las personas que no pueden escuchar, pero ahora lo utilizamos para variedad de situaciones.

- En algunos paises por ley debe ser aplicada.

### Ver también

(Colocar noticias de demandas)

## Criterios para hacer una web accesible

La WCAG (Web Content Accessibility Guidelines) nos da las diferentes pautas o check list que debemos considerar para hacer una aplicación accesible. Esta guía fue creada por la W3C (World Wide Web Consortium), la cuál es una organización que genera diferentes estándares que utilizamos en la web, donde se generó la iniciativa WAI (Web Accesibility Iniciative) que tiene como meta asegurar la accesibilidad web.
Ten presente que actualmente vamos en la versión 2.2, pero ya se encuentra en desarrollo la versión 3.0, además que WCAG tiene 12 criterios para implementar la accesibilidad, los cuales tienen tres nieveles de conformidad:

### Criterios de conformidad de la WCAG

- A: Este es el nivel básico, y por tanto el que requiere la menor inversión.
- AA: Nivel intermedio de implementación.
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

Hay personas que pueden contar con discapacidad visual como: Visión borrosa, Protanopia, Deuteranopia y Acromatopsia. Estas discapaciades impiden la visualización de ciertos colores o formas, por tanto se pueden utilizar herramientas como **rendering** de chrome, el cual nos permite simular diferentes tipos de discapacidad visual. Para acceder a esta herramienta: Busca en la barra que nos aparece en el navegador (console, elements, network, etc.) vamos a más opciones y buscamos rendering cómo se muetra en la imagen a continuación:

(colocar aquí imagen de rendering)

_hint_
La idea es no utilizar sólo colores para mostrar algo importante o una interacción, ya que puedes utilizar animaciones para mejorar la navegación.

Screen reader es una extensión de chrome que nos sirve para simular cómo una persona con discapacidad visual puede navegar, ya que esta extensión lee las acciones que realizamos.

Pruebas con teclado
El teclado es muy importante, ya que sirve como base para muchas tecnologías asistivas, sin embargo en web debemos tener mucho cuidado con elementos que disponemos para mostrar información, ya que sólo etiquetas de link y de formulario se pueden acceder desde el teclado, por ello si deseas colocarle acceso por teclado a un elemento diferente a estos debes programarlo.
