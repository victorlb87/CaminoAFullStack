# HTML & CSS 101

https://www.freecodecamp.org/learn/responsive-web-design/

## **HTML BASICO**


### **Tags mas usado**


Un tag siempre va entre `<h1>` y cierra `</h1>`

    <h1> / <h2> / <h3>
Tag que indica un titulo, al cambiar el numero estamos agregando subtitulos.

    <p> </p> 
Tag que indica un parrafo.

    <!-- comentario -->
De esta manera se comenta en HTML y CSS, en vsc se puede usar `[ctrl] + k` y luego `[ctrl] + u`.  

    head, body,main, header, footer, nav, video, article, section
Estos tags dan estructura a el HTML y ayudan con el SEO (Search Engine Operation). Por ejemplo, el tag main permite a los SEO encontrar el contenido de tu pagina.

    <img src="" alt="">
Todas las imagenes deben tener un atributo alt para mejorar la accesibilidad dada por los screen readers. Si es solo decorativa se puede dejar el atributo en vacio.

    <a href="#" target="_self">vuelve al inicio</a>
a refiere a anchor, su usa para direccionar a webs. 
Si se direcciona a # te manda al inicio de la pagina, tambien podemos referirnos a algun id en especifico. El target refiere a como responde al hacer click, self abre el link en la misma pagina, _blank en una nueva. 

    atributo: id="header"
Se refiere solo a un elemento y tiene que ser unico.

    <ul>
Tag para agregar una lista con puntos.

    <li>
Tag para agregar elementos a una lista.

    <ol>
Tag para agregar una lista ordenada con numeros.

    <input type="text"  placeholder="texto" required>
Tag que agrega formularios. Type refiere al tipo de formulario. required hace que el formulario sea obligatorio antes de enviar. Placeholder refiere al texto que aparecera en el cuadro del formulario.

    <form action=""></form>
Permite enviar la informacion de un formulario a donde se desea.

    <button type="submit">Enviar</button>
Tag para crear un boton segun el type le damos funcionalidad. Tambien va dentro de form en este caso.

    <label for="victor"><input type="radio" value="victor" id="victor" name="pregunta" >Victor</label>
Tag para hacer un formulario de opciones. Dentro de label va el texto que acompaña al boton. El atributo name debe ser el mismo para todas las opciones. El atributo value es el valor que retorna al elegir ese valor. 

    <label for="victor"><input type="checkbox" value="victor" id="victor" name="pregunta" checked>Victor</label>
Cuando el tipo es Checkbox permite llenar varias opciones en el formulario. Al agregar checked los checkbox estaran marcados al inicio, en el caso de radio, funciona con uno solo del grupo.

    <div></div>
Tag para hacer divisiones.
___
## CSS BASICO


El atributo style se puede agregar a los elementos html para modificar su estilo. Ten en cuenta que cuando va en linea igual se usa `;` para separar propiedades.

    <h1 class="clase1 clase2" >
Las clases son estilos reutilizables que se pueden usar en el html.


### **Tipos de selectores**


Los selectores permiten seleccionar que elementos se desea modificar, los tipos son:
- `body` se pueden usar tags para dar estilos en el archivo css.
- `.` se usa en el archivo css para referenciar las clases.
- `#` se usa para referenciar un id.
- `[type='radio']` referencia a un atributo de un elemento.
- `a:hover` referencia al estado del tag.


### **Propiedades mas usadas**


    color: red;
Da color al texto.

    font-size: 30px;
Tamaño del texto.

    font-family: helvetica, serif, mosnospace;
Elige el tipo de fuente para el texto. Se pueden agregar con `,` varios tipos de fuentes, esto sirve en el caso de que la fuente no se encuentre disponible pase a la siguiente. Ademas sirve en el caso de que no encuentre un caracter determinado, lo busca en la siguiente fuente.
   
    width: 100px;
Indica el tamaño del elemeto, suele ser usado para imagenes.

    border-color / border-width / border-style/ border-radius
Crea un borde alrededor del elemento.**Investigar propiedad**

    backgroud-color: black;
Da color al fondo.

    padding top right bottom left
Controla el espacion entre el contenido del elemento y su borde.

    margin top right bottom left
Controla el espacio entre el borde de un elemento y los que lo rodean. Si se pone un valor negativo, el elemento crecera.


### **Fuentes **


     <link href="https://fonts.googleapis.com/css?family=Lobster" rel="stylesheet" type="text/css">

Puedes usar fuentes de la web, referenciando su URL. [Google fonts](https://fonts.google.com/) es una fuente muy usada. Este tag suele ir denntro del tag head.


### **Unidades**

**Revisar en otra fuente**

Las distintas unidades nos permiten definir el tamaño o espacio de un item. Por ejemplo, `px` es una unidad de longitud referida a pixels.

Los dos tipos principales de longitud son: Abosulto y relativo.

Las unidades absolutas refieren a unidades fisicas como `in` o `mm`.

Las unidades relativas, como `em` o `rem` refieren a otro valor de longitud. por ejemplo, `em` esta basado en el tamaño de la fuente del elemento. 


### **Jerarquia de estilos**


Los estilos de los elementos padres suelen heredarse a los hijos. En el caso que el selector directamente referencie a un elemento hijo, este hace que cambie el estilo. Ademas si este elemento tiene dos clases que lo refieren, se tendra en cuenta el estilo del ultimo selector. Si se usa el id del elemento este sera el que se tome como referencia para el estilo. Si el estilo esta en linea del html este tomara prioridad.

    color: red !important ; 
Da prioridad a la propiedad para el elemento. Esta no cambia aunque se declare con otros selectores, incluyendo el estilo en linea.


### **Variables**


    --penguin-skin: black;
Las variables permiten cambiar las propiedades del los estilos al instante, solo cambiando un valor. Se tiene que declara como si fuera una propiedad dentro de un selector. Se usa de la siguiente manera:
    
        background: var(--penguin-skin, black);
La segunda opcion dentro de la variable, en este caso `black`, sirve en caso la variable sea invalida. Tambien se suele declarar antes valores genericos antes de las varibles para exploradores que no soporten variables.

Las variables suele ser definidas en el elemento `:root`. Este es un pseudo-class selector que refiere a la raiz del documento, usualmente el elemento html. Las variables definidas ene este selector estan disponibles globalmente.

El valor de la variable se puede modificar en un selector.

Las variables pueden ayudarte a usar media queries. Por ejemlpo, cuando la pantalla es mas grande o pequeña que tu media query break point, puedes cambiar el valor y se aplicara el estilo donde se use.


## **Diseño Visual**


El diseño visual es una combinacion de tipografia, graficos, animacion, layout de la pagina, y mas para ayudar a enviar un mensaje unico.


### **Tags Usados**


    <u>
Da estilo de subrayado al texto.

    <em>
Da estilo de cursiva.

    <s>
Da estilo de tachado.

    <hr>
Crea una raya horizontal.


### **Propiedades usadas**


    text-align: center;
Alinea el texto segun el valor.

    width: 10px;
Especifica el ancho del elemento.

    height: 10px;
Alto del elemento.

    font-weight: bold; o en html: <strong> 
Da estilo negrita al texto. Ademas se le puede dar un valor de unidades para indicar el grosor.

    text-decoration: underline; o en html: <u>
Da estilo de subrayado al texto.

    font-style: italic; o en html: <em>
Da estilo de cursiva.

    text-decoration: line-through; o en html: <s>
Da estilo de tachado.

    background-color: rgba(45, 45, 45, 0.1);
Cuando se usa el `rgba()` podemos indicar la opacidad del color que varia de 0 a 1.

    font-size: 10px;
Cambia el tamaño del texto.

    box-shadow: 0 10px 20px rgba(0,0,0,0.19), 0 6px 6px rgba(0,0,0,0.23);
Aplica una sombra o mas al elemento. Los valores a indicar son: 
- offset-x (how far to push the shadow horizontally from the element)
- offset-y (how far to push the shadow vertically from the element)
- blur-radius (opcional)
- spread-radius (opcional)
- color 

Se pueden crear varias sombras agregando comas.

    opacity: 0.5;
Agrega opacidad al elemento puede ir de 0 a 1.

    text-transform: lowercase;
Tansforma el texto. lowercase (minusculas), uppercase(mayusculas), capitalize (la primera letra mayuscula), initial(la inicial), inherit(hereda del padre) y none.

    line-height: 25px;
Da el espaciado entre lineas del texto.

    a:hover {}
Este selector permite modificar el anchor cuando esta en el estado indicado.


### **Cambiar la posicion de elementos**


    position: relative;
Permite especificar como mover elementos relativamente a su posicion por default. Al cambiar el elemento de su posicion, el resto de elementos se comporta como si este estuviera en su posicion por default.

    bottom: 10px;
Lo aleja 10px del fondo. de la misma manera se usa `top`, `left` y `right`.

    position: absolute;
Bloque el elemento en su lugar respecto a su contenedor padre. Esto remueve el elemento del flow de la pagina, ya que es ignorado por el resto. Las propiedades son `top`, `bottom`,`left` y `right`..Si se te olvida poner una regla de posicion a un item padre, el explorador seguira buscando hasta llegar al tag `body`.

    position: fixed;
Es un posicion absoluta que bloquea el elemento relativamente a la ventana del explorador. Tambien remueve el elemento del flow de la pagina y los otros elementos no se dan cuenta donde esta posicionado. El elemento nose movera aun cuando el usuaria haga scroll.

    float: left; o float: right;
Elementos flotantes son removidos del flow de la pagina y son empujados a la izquierda o derecha de sus padres.

    z-index: 1;
Especifica el orden de como los elemntos estan uno encima de otro. El numero debe ser un entero. Mientras mayor sea el valor, mayor prioridad para que vaya arriba.

    margin: auto;
De esta manera se puede usar el margen para centrarlo.


### **Colors**

**Investigar sobre teoria de color**

**Investigar sobre colores terciarios**

    hsl()
Este valor usa el concepto de rueda de colores, donde el angulo del color en el circulo es de 0 a 360. Saturation es la cantidad de gris en el color. Lightness es la cantidad de blanco o negro en un color, 100% siendo blanco.

    background: linear-gradient(90deg, red, yellow, rgb(204, 204, 255));
El primer argumento la direccion donde la transicion de color comienza. En este caso 90deg indica que la gradiente va de izquierda a derecha. 45deg hace la direccion de la esquina inferior izquierda a la superio derecha y los siguientes argumentos refiere a los colores usados.

    repeating-linear-gradient(90deg,yellow 0px,blue 40px, green 40px,red 80px);
Este atributo es similar al anterior, solo que se repite. Se aceptan una variedad de valores.

    background: url();
El valor url permite usar una imagen de fondo.

### **Formas de elementos**

    transform: scale(2);
Se usan esta propiedad junto con esta funcion para transformar la escala del elemento. La propiedad transform te permite modificar el elemento de distintas maneras y cuando se usa con pseudo clases como :hover, permite añadir interactividad.

    transform: skewX(-32deg);
Este valor tuerce el elemento segun lo indicadoen el eje x.

    transform: skewY(-32deg);
Lo mismo que el anterior solo que en el eje y.

    ::before and ::after 
Son pseudo-elementos que son el primero y ultimo hijo respectivamente. 

```
.heart::before {
  content: "";
  background-color: yellow;
  border-radius: 25%;
  position: absolute;
  height: 50px;
  width: 70px;
  top: -50px;
  left: 5px;
}
```
Para que funciones estos pseudo-elementos, deben tener la propiedad content. Esta propiedad suele usarse para agregar photo o texto al elemento seleccionado. Cuando se usa para hacer figuras este se deja vacio como en el ejemplo.

### **Animacion**

Para animar elementos debes saber de las propiedades de animacion y la regla de @keyframes. Las propiedades controlan como se debe comportar y la regla de @keyframe controla que sucede durante la animacion. Hay 8 propiedades de animacion **(Investigar)** 

```
#anim {
  animation-name: colorful;
  animation-duration: 3s;
}

@keyframes colorful {
  0% {
    background-color: blue;
  }
  100% {
    background-color: yellow;
  }
}
```
`animation-name` fija el nombre de la anumacion que luego lo usa @keyframes.
`animation-duration` fija el tiempo de la animacion.
`@keyframes` especifica que pasa en la duracion de la animacion. Esto se hace dando propiedades para frames especificos con porcentajes variando de 0% a 100%.

    animation-fill-mode: forwards
Especifica el estilo aplicado a un elemento cuando la animacion acaba.

    animation-iteration-count: 3;
Especifica el numero de iteraciones, se puede usar `infinite`.

    animation-timing-function: ease;
Controla que tan rapido cambia el elemento en la animacion.

    animation-timing-function: cubic-bezier(x1,y1,x2,y2);
Este valor te permite definir los valores de `Xs` y `Ys`, de manera que dictaran la forma de la curva en la que la animacion seguira.  


## **Accesibilidad Aplicada**

Refiere a la UI(USer inferface).

    <img src="importantLogo.jpeg" alt="Company logo">
El atributo alt describe el contenido de la imagen, esto ayuda en el caso de que la pagina no carga o no puede ser vista por un usuario. Los motores de busqueda tambien lo usan para entender que incluye la imagen en los resultados de busqueda.

Por especificacion HTML5, este atributo es obligatorio. En el caso que la imagen sea decorativa este atributo puede ir vacio.

    <h1> / h2 / . .. / h6
Los heading pueden ser leidos por los screen readers sin leeer el resto de la pagina, dandole un resumen del contenido al usuario.

    main, header, footer, nav, article, and section, among others.
Tags que dan accesibilidad. Estos son similares a `div`. Sin embargo, el tag puede indicar el tipo de informacion contenida, que añade significado semantico al contenido.

    <main>
Este elemento es usado para el contenido principal de la pagina y debe haber unos solo por pagina. Esto es para indicar el topico principal de la pagina. No debe contener elementos comunes tipo navegacion o banners.

    <article>
Es un elemento seccionador y es usado para envolver auto-contenido independiente. Suele usarse en blogs, foros o articulos de noticias.

    <section >
Es un tag nuevo en html5, sirve para agrupar tematicamente contenido. Cuando no hay relacion entre grupo de contenidos es mejor usar `div`.

    <div> > section > article
`<div>` - groups content `<section>` - groups related content `<article>` - groups independent, self-contained content

    <header >
Usado para añadir significado semantico y envuelve informacion introductora o links de navegacion para un tag padre y trabaja correctamente alrededor de contenido que es repetido en multiples paginas.

`header` comparte un embedded landmark feature al igual que `main`. Este se usa dentro de `body`.

    <nav>
Este tag se usa para contener los principales links de navegacion de tu pagina. Si hay links repetidos al final de la pagina no es necesario contenerlos en `nav`, se puede usar `footer`.

    <footer>
Es similar a nav y header. Mayormente, se usas para contener informacion copyright o links a documentos relacionados que van al final de la pagina.

```
<audio id="meowClip" controls>
  <source src="audio/meow.mp3" type="audio/mpeg">
  <source src="audio/meow.ogg" type="audio/ogg">
</audio>
```
El contenido de audio tambien necesita una alternativa de texto para mayor accesibilidad. Esto se puede realizar con texto cercano o un  link a la transcripcion.
Este tag soporta el atributo de control, de manera que muestra al explorador el default play, pause, otros controles y soporta la funcionalidad de teclado.

Note: Multimedia content usually has both visual and auditory components. It needs synchronized captions and a transcript so users with visual and/or auditory impairments can access it. Generally, a web developer is not responsible for creating the captions or transcript, but needs to know to include them.

```
<figure>
  <img src="roundhouseDestruction.jpeg" alt="Photo of Camper Cat executing a roundhouse kick">
  <br>
  <figcaption>
    Master Camper Cat demonstrates proper form of a roundhouse kick.
  </figcaption>
</figure>
```
`figure` y `figcaption` estos items envuelven una representacion visual con su subtitulo. 

    <label>
El tag envuelve el texto para un item de control especifico, usualmente el nombre o etiqueta de eleccion. El atributo `for` en `label` asocia la etiqueta a la forma de control y es usada por lectores de pantalla.

```
<form>
  <fieldset>
    <legend>Choose one of these three items:</legend>
    <input id="one" type="radio" name="items" value="one">
    <label for="one">Choice One</label><br>
    <input id="two" type="radio" name="items" value="two">
    <label for="two">Choice Two</label><br>
    <input id="three" type="radio" name="items" value="three">
    <label for="three">Choice Three</label>
  </fieldset>
</form>
```
El tag `fieldset` envuelve el grupo de radio buttons. Usualmente usa un tag `legend` para proveeer una descripcion al grupo. The fieldset wrapper and legend tag are not necessary when the choices are self-explanatory, like a gender selection.

```
<label for="input1">Enter a date:</label>
<input type="date" id="input1" name="input1">
```
`type="date"` es un atributo para ingresar fechas.

    <time datetime="2013-02-13">last Wednesday</time>
Este tag sirve para estandarizar el tieempo, el atributo `datetime` lleva un formato valido de la fecha. Esto ayuda a evitar confusion ya que establece una version del tiempo estandar. 

**Make Elements Only Visible to a Screen Reader by Using Custom CSS**

**CSS** puede ocultar elementos que deseas que solo sean leidos por screen readers.por ejemplo:
```
.sr-only {
  position: absolute;
  left: -10000px;
  width: 1px;
  height: 1px;
  top: auto;
  overflow: hidden;
}
```
Note: The following CSS approaches will NOT do the same thing:
`display: none;` or `visibility: hidden;` hides content for everyone, including screen reader users.
Zero values for pixel sizes, such as `width: 0px; height: 0px;` removes that element from the flow of your document, meaning screen readers will ignore it.

### **Contraste**

The Web Content Accessibility Guidelines (WCAG), recomienda al menos 4.5 a 1 ratio de contraste para verlo normal. El ratio es calculado comparando el valor de luminicidad de dos colores. Este varia de 1:1 para el mismo color a 21:1 para blanco contra negro. Hay varias herramientas para verificar esto.

Los colores son una gran parte del diseño visual pero presentan dos temas. Primero, los colores no solo deben ser la manera en que se presenta informacion importante ya que los screen readers no lo detectan. Segundo, el primer plano 
y el segundo plano deben contrastar para que personas daltonicas lo distingan.

In practice, the 4.5:1 contrast ratio can be reached by shading (adding black to) the darker color and tinting (adding white to) the lighter color. Darker shades on the color wheel are considered to be shades of blues, violets, magentas, and reds, whereas lighter tinted colors are oranges, yellows, greens, and blue-greens.

` **Colorblidness** ` 
Hay varias formas de colorblidness. La mas comun es una forma reducida de detectar verdes.

Note: Some online color picking tools include visual simulations of how colors appear for different types of colorblindness. These are great resources in addition to online contrast checking calculators.


### **Navecion de teclado**


    <button accesskey="b">Important Button</button>
`accesskey` ofrece una navegacion mas eficiente para usuarios de teclado. Este atributo se puede usar con cualquier elemento pero es mejor usado con elementos interactivos. Esto incluye links, botones y form controls. 

    <div tabindex="0">I need keyboard focus!</div>
El atributo `tabindex` tiene 3 funciones distintivas. Cuando esta en un tag, indica que nos podemos fijar en el elemento. El valor determina el comportamiento, puede ser un entero positivo, negativo o cero.

Algunos elementos, como links, autromaticamente reciben foco del teclado cuando un usuario hace tab por la pagina. Es en el mismo orden en el que estan en la fuente HTML. ESto puede usarse en elementos como div, span o p.Bonus - using tabindex also enables the CSS pseudo-class :focus to work on the p tag.

Note: A negative tabindex value (typically -1) indicates that an element is focusable, but is not reachable by the keyboard. This method is generally used to bring focus to content programmatically (like when a div used for a pop-up window is activated), and is beyond the scope of these challenges.

`tabindex` tambien especifica el orden de tab para los elementos, siendo el mayor valor 1 el cual toma prioridad, luego los valores positivos hasta que acaben y vuelve a los default con valor 0.


## **Principios de diseño de web responsive**


    @media (max-width: 100px) { /* CSS Rules */ }
    @media (min-height: 350px) { /* CSS Rules */ }
Media queries consisten de un tipo de media y si este coincide con el tipo de sidpositivo donde se muestra.

```
img {
  max-width: 100%;
  height: auto;
}
```
Para imagenes se puede usar porcentages para acomodarla o usar auto para mantener el tamaño de la imagen. En el ejemplo se define el ancho y el alto en auto para que tenga el aspect ratio original.

```
<style>
  img { height: 250px; width: 250px; }
</style>
<img src="coolPic500x500" alt="A most excellent picture">
```
Debido a la cantidad de pantallas con distintas densidades de pixel o en el caso de las mas modernas iMAC, retina display, algunas imagenes se pueden ver pixeleadas. La manera mas simple de solucionar este problema es definiendo su ancho y altura a la mitad del valor que la imagen original es.

### **Tipografia**
En vez de usar em o px para un texto, se pueden usar unidades viewport. Estas unidades, como los porcentajes, son unidades relativas. Estas son relativas a la dimension del viewport (ancho y alto) de un dispositivo, y los porcetajes son relativos a el elemento padre contenedor.

The four different viewport units are:

- vw (viewport width): 10vw would be 10% of the viewport's width.  
- vh (viewport height): 3vh would be 3% of the viewport's height.  
- vmin (viewport minimum): 70vmin would be 70% of the viewport's smaller dimension (height or width).  
- vmax (viewport maximum): 100vmax would be 100% of the viewport's bigger dimension (height or width).  

**!!investigar viewport**


## **CSS FLEXBOX**


    display: flex;
Esta propiedad permite usar otras propiedades de flex para hacer una pagina responsive.

    flex-direction: row/ row-reverse / column / column-reverse
Esta propiedad hace posible alinear cualquier hijo del elemento a columnas o filas. 

La propiedad `justify-content` tiene varias opciones para alinear y espaciar los items flex.

![flex alineamiento](https://www.w3.org/TR/css-flexbox-1/images/flex-direction-terms.svg)

    justify-content: center;
Alinea los items flex al centro del contenedor flex. Hay otros valores posible:
- `flex start` .- alinea items al inicio del contenedor. Este es el valor default
- `flex-end` .- alinea los items al final del contenedor.
- `space-bewteen` .- alinea los items en el centro del axis con espacio extra entre los items. El primer y ultimo items son empujados a los bordes del contenedor, el resto de espacio es distribuido equivalentemente entre el resto de items.
- `space-around` .- el espacio es distribuido alrededor de todos los items con la mitad de espacio en cada extremo del contenedor.
- `space-evenly` .- distribuye igualmente el espacio entre items con un espacio grande al final del contenedor.

    align-items: flex-start
Esta propiedad funciona similarmente a la anterior, usa el mismo axis. La diferencia esta en que esta propiedad usa el cross axis, en cambio `justify-content` usa el main axis para alinear elementos.
Cuando `flex-direction: row` le dice a CSS como empujar los items en la fila o para la parte baja del contenedor y para el valor `column` a la derecha o izquierda.

Los distintos valores son:
- `flex-start` .- alinea los items al inicio del contenedor. Para las filas estos es el top y para columnas a la izquierda.
- `flex-end` .- alinea los items al final del contenedor.
- `center` .- alinea los items al centro.
- `strech` .- estira los items para llenar el contenedor. Por ejemplo, los row items son estirados para llenar el top y bottom del contenedor. Este es el valor default.
- `baseline` .- alinea los items a su linea base, que refiere la la linea donde los textos establecen.

    flex-wrap: nowrap;
Por default, el contenedor flex, llenara todos los items juntos dentro. Usando esta propiedad le decimos a los iltes que se cubran. Los valores posibles son:

- nowrap .- no cubre los items.
- wrap .- cubre los items.
- wrap-reverse .- cubre los items en multiples lineas de abajo para arriba si estan en filas y de derecha para izquierda si estan en columnas.

    flex-shrink: 1;
Permite achicar el item si el contenedor es pequeño. Los items se achican cuando la suma del tamaño de todos los items es mayor a la del contenedor. Los valores son numeris y mayor el numero mas los achicara comparado a otros items.

    flex-grow: 1;
Es lo opuesto, controla como crecen los items cuando el contenedor crece.

    flex-basis:  10px;
Especifica el tamaño inicial del item antes que CSS haga modificaciones con flex-shrink o flex-grow. Las unidades usadas son px,em, %, etc.

    flex: 0 1 auto; (propiedad default)
Este es un shorcut para la 3 propiedades anteriores. El ordes es: `flex-grow`,`flex-shrink` y `flex-basis`. 

    order: 1;
Indica el orden en que apareceran los items en el contenedor.

    align-self: center;
Esta propiedad, permite ajustar los items individualmente, se usan los mismos valores que `align-items` y los reemplazara.


## **CSS GRID**


Es un nuevo concepto que permite crear responsive layouts. Funciona, convirtiendo una pagina html en una cuadricula, y permite colocar sus hijos dentro.

    display: grid;
Propiedad que convierte el elemento en cuadricula.

```
.container {
  display: grid;
  grid-template-columns: 50px 50px;
}
```
`grid-template-columns` agrega columnas a la cuadricula. En el ejemplo, hay 2 columnas de 50px, el valor de cada parammetro indica el ancho de cada una. `grid-templates-rows` funciona de manera analoga y pueden trabajar juntas.

**Use CSS Grid units to Change the Size of Columns and Rows**
Se pueden usa unidades absolutas y relativas como px y em para definir las columnas y filas. Se pueden usar las siguientes tambien:
- fr .- ajusta las filas o columnas a una fraccion del espacio disponible.
- auto .- ajusta el ancho o alto del contenido automaticamente.
- % .- ajusta el contenido respecto al porcentaje del ancho del contenedor.

    grid-template-columns: auto 50px 10% 2fr 1fr;
Este ejemplo, crea 5 columnas. La primera es ancha como su contenido, la segunda 50px, la tercera es el 10% del contenedor, las 2 ultimas dividen el espacio restante en 3 secciones, 2 de estas para la cuarta columna y una para la quinta.

    grid-column-gap: 10px;
Esta propiedad añade un espacio entre columnas. Para las filas se usa `grid-row-gap`.

    grid-gap: 10px;
Establece lo mismo que las anteriores, si se escribe un solo valor se establece el espacio para columnas y filas, si se dan 2 valores, usara el primero para las filas y el segundo para las columnas. 

![Grid3x3](/HTML_CSS_101/imagenes/grid3x3.png)

    grid-column: 1 / 3;
Indica donde quieres que el item inicie. En el ejemplo, indicara que el item empiece en la primera linea vertical comenzando desde la izquierda y se extienda hasta la tercera linea, consumiendo 2 columnas.

    grid-row: 1 / 3;
Funciona analogamente a `grid-column`.

    justify-self: stretch / start / center / end ;
Se pueden alinear el contenido de los items horizontalmente con esta propiedad. Por default esta propiedad tiene el valor `stretch`.

    align-self: stretch;
Con los mismos valores de la propiedad `justify-self`, esta propiedad permite alinear un item horizontalmente. 

    justify-items: stretch; horizontal
    align-items: stretch;   vertical
Alinea todos los items del contenedor.

```
grid-template-areas:
  "header header header"
  "advert content content"
  "advert footer footer";
```
Se puede agrupar las celdas en tu cuadricula juntas en una area y darles nombre. En el ejemplo, se agrupan las celdas en 4 areas; header, advert, content, and footer. Cada palabra representa una celda y cada "" representa una fila.

```
.item1 {
  grid-area: header;
}
```
Esta propiedad hace que los que tengan la clase indicadad ocupen el area llamada header.

```
item1 { grid-area: 1/1/2/4; }
grid-area: horizontal line to start at / vertical line to start at / horizontal line to end at / vertical line to end at;
```
`grid-area` tambien se puede usar de esta forma, indicando en que lineas comienza y que lineas termina.

```
grid-template-rows: repeat(100, 50px);
```
La funcion repeat, permite crear filas y columnas sin necesidad de especificar cada una.

```
grid-template-columns: repeat(2, 1fr 50px) 20px;
se traduce 
grid-template-columns: 1fr 50px 1fr 50px 20px;
```
Tambien se puede especificar que parte se repetira y cual se indicara individualmente.

    grid-template-columns: 100px minmax(50px, 200px);
El valor `minmax` permite limitar el tamaño del item cuando el grid contenedor cambia de tamaño. En el ejemplo, una columna es de 100px y la otra puede varias entre 50px y 200px.

    repeat(auto-fill, minmax(60px, 1fr));
La opcion auto-fill permite automaticamente insertar la filas y columnas posibles, del tamaño elegido, dentro del tamaño del contenedor. Cuando el contenedor cambia de tamaño esta funcion añade columnas de 60px y estirandolas hasta que se pueda insertar otra. 
Si tu contenedor no tiene espacio para los items en una fila los movera a otra.

    repeat(auto-fit, minmax(60px, 1fr));
`auto-fit` en vez de incluir celdas, este estira los items para cubrir los espacios nuevos.

**Use Media Queries to Create Responsive Layouts**

**Create Grids within Grids**