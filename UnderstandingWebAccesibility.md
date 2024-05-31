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
