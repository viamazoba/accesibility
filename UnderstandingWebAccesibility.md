## Tecnologías asistivas

Las tecnologías asistivas más comunes son:

- Lectores de pantalla
- Software de reconocimiento de voz
- magnificadores de pantalla (screen magnifiers)
- Dispositivos de entrada alternativos (alternative input devices): Estos son botones u otro tipo de dispositivos que ayudan a personas con movilidad reducida a realizar acciones con el mínimo esfuerzo o mivimiento.

## Árbol de accesibilidad

Este es un objeto en forma de árbol, el cual es la traducción de nuestro código en información importante para los dispositivos asistivos. En la imagen a continuación se muestra cómo podemos acceder al árbol de accesibilidad en chrome:

(Aquí va accesibility-tree3.png)

Se debe tener en cuenta que este arbol de accesibilidad toma información tanto de etiquetas que tienen un sentido semántico en HTML (ver figura XX) , como buttons, sections, header, nav, etc. Como de atributos como arias que brindan descripciones más detalladas para elementos sin significado semántico en HTML como son las etiquetas divs. En la gifura XXX se muestra un buen uso del sentido semántico de HTML para el árbol de accesibilidad, ya que dos elementos pueden verse de igual forma, pero para el árbol de accesibilidad no serán lo mismo.

(Aquí va accesibility-tree2.png) --> Esta es para la figura XX
(poner aquí good-use-html.png) --> Esta es para figura XXX

## ¿Cómo podemos testear la accesibilidad de nuestro sitio?

Podemos probar nuestro sitio con las siguientes herramientas:

1. Usando tecnologías asistivas
2. Usando checkquadores de contraste para validar los colores de nuestra aplicación
3. Herramientas automatizadas como: lighthouse (chrome), accesibility inspector (firefox) o software como aXe
4. Asistentes de inteligencia artificial, por ejemplo ChatGPT para verificar nuestro código o contrastes de colores

A continuación se muestra cómo encontrar lighthouse en chrome:

(Poner aquí find-chrome.png)

### Aquí se habla de los criterios de aceptación del WCAG (A, AA y AAA) para dar un ejemplo con el contraste, peinsalo para agregar dicha sección cerca de esta

## Hablemos del contraste en los colores

Para hablar del contraste en los colores, y por tanto saber si dos colores pueden ser combinados para dar un grado de accesibilidad en un fondo y un color de texto, se suele hablar del nivel de contraste. Para entender este concepto piensa que el nivel de contraste del color negro consigo mismo es de 1:1, mientras que el contraste del negro con el blanco presenta el mayor contraste que se puede tener que es de 1:21 como se muestra en la imagen a continuación:

(Colocar aquí color-contrast.png)

Así, un ejemplo claro del nivel de **aceptivilidad del WCAG** para el contraste puede ser el siguiente:

(poner aquí aceptability-contrast-example.png)

Para evaluar el contraste podemos utilizar diferentes sitios web's que nos indican el nivel de contraste entre dos colores como https://webaim.org/resources/contrastchecker/, pero también google chrome nos permite visualizar este nivel de contraste como se muestra a continuación:

(Poner aquí contrast-chrome.png)

_hint_
Para poder cumplir los criterios de aceptación en el contraste se deben cumplir los siguientes requriemientos:

- Para el criterio de aceptación AA se espera que el mínimo contraste sea 4.5:1, y para textos que posean un tamaños mayor o igual a 24px, se espera que el contraste sea mínimo de 3:1.

- Para el criterio AAA se espera que el contraste mínimo sea de 7:1, y para textos mayores e iguales a 24px el nivel de contraste sea mínimo de 4.5:1.

## Hablemos de las imágenes

Para agregar un texto alternativo a las imágenes en la web solemos utilizar el atributo **alt**, sin embargo, hay diferentes consideraciones además de utilizar esta etiqueta que debemos considerar, por ejemplo:

- Al escribir el texto, que va en el atributo **alt** de la imagen, debemos ser lo más concizos posible. Ya que la idea no es dejar que un lector de pantalla inhiba la fluidez de la navegación de un usuario (ver imagen a continuación):

(Colocar aquí image-description.png)

- Ten presente que no todas las imágenes de un sitio web necesitan la etiqueta alt, por ejemplo, las imágenes decorativas no lo requieren o las imágenes que van acompañadas con texto (en etiquetas HTML) que describen muy bien lo que tiene la imagen. Sin embargo, siempre se debe colocar el atributo **alt**, sólo que en este caso se coloca como un string vacío **(alt='')**, así el lector de pantalla sabe que debe saltar la imagen.

- Se recomienda que las descripciones que pongas a tus imágenes en el atributo **alt** terminen con un punto **(.)**, ya que esto hará que el lector de pantalla realice un breve descanso antes de continuar, así se hará maś entendible la lectura del contenido.

Recuerda que la accesibilidad en imágenes suele utilizarse para personas que poseen muy baja o nula visión, personas que apagan las imágenes de la web para optimizar su internet, pero también para los motores de búsqueda como google.

## Hablemos de los links

Para los links como para los botones que deseamos utilizar en nuestra web, además de utilizar su elemento semántico correcto (<a> o <button>), se deben tener presente una serie de recomendaciones:

### Links

- Estos elementos deben ser reconocibles en el texto, por tanto, se espera que posean un disitintivo no sólo de color, sino también de forma (tamaño, font, decoradores, etc.).
- Se espera que no posean un texto ambiguo que evite su entendimiento en el contexto, ejemplo de texto ambiguo: click aquí, más, continuar (ver imagen a continuación).

(Colocar aquí good-link-example.png)

- Se recomienda el uso de aria-labels para añadirle descripciones más detalladas a nuestros links en caso de que no se pueda realizar directamente sobre el texto o elemento que acogen o envuelven (revisar sección de Aria para complementar).

### Hablemos de los labels

Los labels son etiquetas muy usadas debido a su significado semántico para los formularios, sin embargo se deben tener presentes las siguientes puntos al implementar estas etiquetas:

- Cada etiqueta input debe poseer su respectivo label y placeholder, debido a que el label **no reemplaza** el placeholder del input, ya que el placeholder debe usarse como un ejemplo de cara al usuario del tipo de dato a digitar en el input (ver imagen a continuación).

(Colocar aquí label-input-placeholder.png)

- Debe asociarse siempre el label con su respectivo input mediante el atributo **for** del label y **id** del input, ya que al dar click o hacer foco sobre el label este foco se traslada al input, lo cual ayuda a una mejor navegación.

La última recomendación dada es válida para aquel elemento HTML al que se le pueda asociar una etiqueta label, por ejemplo: selects.

### Hablemos de los radio buttons

A los radio buttons pueden añadirsele etiquetas que expanden su sentido semnántico, y por tanto su accesibilidad, dichas etiquetas son:

- fieldset tag (<fieldset>) : Cuando un lector de pantalla encuentra esta etiqueta en el radio button, le especifica al usuario que ha entrado a un grupo de elementos relacionados.
- legend tag (<legend>): Funciona como el título o la descripción del grupo.

En la siguiente imagen se muestra cómo puede verse un radio button accesible:

(Poner aquí accesible-radio-button.png)

### Dato interesante

Se estima que alrededor del 96.5% de los sitios web tienen problemas de accesibilidad que se podrían prevenir conociendo los fundamentos.

### Hablemos de HTML Semnántico

Es importante usar las etiquetas adecuadas en cada una de nuestras páginas, ya que:

- Por defecto las etiquetas con sentido semántico como lo son nav, main, section y footer ayudan a que el lector de pantalla pueda ubicar con facilidad a las personas, puesto que comenta en que parte se está ubicando mientras navega.

- Otras etiquetas semánticas como botones, labels, links, etc. Poseen un comportamiento por defecto para la bevagación, ya que sobre estos elemento se puede hacer foco sin atributos adicionales y son facilmente reconocibles por un lector de pantalla.

- Recuerda que utilizar HTML semántico también ayuda a que los navegadores puedan reconocer más facilmente el contenido de tu página para ser posicionada en los resultados de búsqueda.

### Hablemos de listar nuestro contenido

Se recomienda utilizar las etiquetas **<li>** y **<ul>** en todos lo elementos que se puedan listar como los elementos del nav bar, elementos del footer, cards de los carruseles, etc. Ya que las tecnologías asistivas al encontrarse con estas etiquetas anuncian el principio y fin de la navegación de dichos elementos, lo que ayuda a que el usuario comprenda la cantidad de elementos que hay en la sección. Ten mucho cuidado con esto, ya que suele darsele este lugar a los divs, los cuales carecen de este sentido y usabilidad.

### Hablemos del tamaño del texto apropiado

Se recomienda que para el tamaño del texto se utilice **rem**, debido a que con esta medida relativa las tecnologías asistivas y los navegadores pueden controlar el tamaño de los textos, y así poderlos agrandar o reducir según las necesidades de los usuarios.

### Hablemos de accesibilidad en los títulos

En la siguiente imagen se muestra que los títulos (heading) son los elementos más frecuentemente utilizados para la navegación por las tecnologías asistivas, por tanto es importante utilizar adecuadamente este tipo de etiquetas.

(Colocar aquí use-of-headings.png)

Las siguientes reglas son las que debemos seguir para utilizar las etiquetas de título adecuadamente:

- Los números de las etiquetas de los títulos (h1, h2, h3, etc.) deben ser consecutivos, lo que quiere decir que conforme hacemos scroll en nuestra página dicho número debe ir en aumento.

- Sólo debe existir una etiqueta **h1** por página, ya que esta etiqueta es la que dará un contexto a las personas al ser leidas por tecnologías asistivas.

- Aplica las etiquetas de título por estructura más que por estilos, ya que al final el estilo puede ser modificado mediante CSS.

### Hablemos de ARIA (Accessible Rich Internet Applications)

Estos son atributos que buscan dar mayor contexto al navegador, y por tanto a las tecnologías asistivas, para elementos en nuestra página web que no tienen una etiqueta HTML dedicada, por ejemplo: cards, acordiones, modales, etc. Sin embargo, se aconseja restringir su uso a este caso específico o cuando se requiere dar mayor contexto sobre un elemento, pero lo recomendable es priorizar elementos semánticos.

### Hablemos de ARIA live

Este atributo se utiliza para definir regiones que pueden cambiar dinámicamente, por ejemplo, cuando se aplican notificaciones a la aplicación por un formulario que se ha rellenado mal (ver imagen). Así, el ARIA live le permite a las tecnologías asistivas interrumpir lo que estaban haciendo al aparecer la notificación dinámica, y centrarse en ella.

(poner aquí use-cases-aria-live.png)

### Hablemos del focus programable

En el caso de las notificaciones o cuando se envía un formulario, se espera que el usuario tenga la forma de continuar la navegción de forma simple, y en ese caso se puede aplicar un foco automático a un elemento que lo devuelva a una página o contenido principal. Lo anterior se hace mediante JavaScript, y se busca mantener la lógica en el flujo de navegación. En la siguiente imagen se muestra un foco programable para volver a la página principal luego de llenar un formulario.

(poner aquí programmable-focus.png)

### Hablemos de JavaScript accesible

Lo que se debe tener en cuenta al utilizar los diferentes addEventListener con JavaScript es que las personas van a utilizar diferentes dispositivos para acceder a la web, entonces si se piensa utilizar **mouseover** y **mouseout**, también se debe pensar en su contra parte más accesible como **focus** y **blur** para deteminar las acciones, puesto que muchos dispositivos móviles y tecnologías asistivas no utilizan mouse en su navegación.

### Hablemos del Skip Navigation

Generalmente nuestros menú (header) tienden a tener mucha información de la navegación en nuestro sitio web (ver figura), sin embargo, muchas de las personas que ingresan por teclado no desean recorrer todo el menú para poder llegar al contenido principal de nuestro sitio, por tanto, solemos colocar elementos como lo son los Skip Navigation. Los cuales son elementos que con el primer tab nos pueden llevar al contenido principal (ver figura).

(Colocar aquí navigation.png)
(Colocar aquí navigation-with-skip.png)

Como viste anteriormente, los Skip Navigation tienden a ser elementos que aparecen o desaparecen de la pantalla y como desarrollador puedes utilizar diferentes propiedades para hacerlo, sin embargo, no todas son recomendables porque tieneden a hacer el elemento invisible para el árbol de accesibilidad, lo que hace que ciertas tecnologías asistivas omitan este elemento, en la siguiente figura se muestran algunas de dichas propiedades:

(Colocar aquí recommendation-skip-element.png)

Otra consideración que debes tener al aplicar al colocar un skip navigation es su aparición en pantalla, ya que las personas pueden tender a obviar este elemento al navegar, por ello se recomienda una aparición con transición para llamar la atención de las personas, por ejemplo: Hacer que el skip navigación tenga una transición de 2 a 3 segundos para su aparición completa.
