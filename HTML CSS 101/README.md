# HTML & CSS 101

https://www.freecodecamp.org/learn/responsive-web-design/

## HTML BASICO

### Tags mas usado

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

## CSS BASICO

El atributo style se puede agregar a los elementos html para modificar su estilo. Ten en cuenta que cuando va en linea igual se usa `;` para separar propiedades.

    <h1 class="clase1 clase2" >
Las clases son estilos reutilizables que se pueden usar en el html.

### Tipos de selectores

Los selectores permiten seleccionar que elementos se desea modificar, los tipos son:
- `body` se pueden usar tags para dar estilos en el archivo css
- `.` se usa en el archivo css para referenciar las clases
- `#` se usa para referenciar un id
- `[type='radio']` referencia a un atributo de un elemento

### Propiedades mas usadas

    color: red;
Da color al texto.

    font-size: 30px;
Tamaño del texto.

    font-family: helvetica;
Elige el tipo de fuente para el texto. Se pueden agregar con `,` varios tipos de fuentes, esto sirve en el caso de que la fuente no se encuentre disponible pase a la siguiente. Ademas sirve en el caso de que no encuentre un caracter determinado, lo busca en la siguiente fuente.
   
    width: 100px;
Indica el tamaño del elemeto, suele ser usado para imagenes.

    border-color / border-width / border-style/ border-radius
Crea un borde alrededor del elemento.

    backgroud-color: black;
Da color al fondo.

    padding top right bottom left
Controla el espacionentre el contenido del elemento y su borde.

    margin top right bottom left
Controla el espacio entre el borde de un elemento y los que lo rodean. Si se pone un valor negativo, el elemento crecera.

### Fuentes 

 <link href="https://fonts.googleapis.com/css?family=Lobster" rel="stylesheet" type="text/css">
Puedes usar fuentes de la web, referenciando su URL. [Google fonts](https://fonts.google.com/) es una fuente muy usada. Este tag suele ir denntro del tag head.

### Unidades

Las distintas unidades nos permiten definir el tamaño o espacio de un item. Por ejemplo, `px` es una unidad de longitud referida a pixels.

Los dos tipos principales de longitud son: Abosulto y relativo.

Las unidades absolutas refieren a unidades fisicas como `in` o `mm`.

Las unidades relativas, como `em` o `rem` refieren a otro valor de longitud. por ejemplo, `em` esta basado en el tamaño de la fuente del elemento. 

### Jerarquia de estilos

Los estilos de los elementos padres suelen heredarse a los hijos. En el caso que el selector directamente referencie a un elemento hijo, este hace que cambie el estilo. Ademas si este elemento tiene dos clases que lo refieren, se tendra en cuenta el estilo del ultimo selector. Si se usa el id del elemento este sera el que se tome como referencia para el estilo. Si el estilo esta en linea del html este tomara prioridad.

    color: red !important ; 
Da prioridad a la propiedad para el elemento. Esta no cambia aunque se declare con otros selectores, incluyendo el estilo en linea.

### Variables

    --penguin-skin: black;
Las variables permiten cambiar las propiedades del los estilos al instante, solo cambiando un valor. Se tiene que declara como si fuera una propiedad dentro de un selector. Se usa de la siguiente manera:
    
        background: var(--penguin-skin, black);
La segunda opcion dentro de la variable, en este caso `black`, sirve en caso la variable sea invalida. Tambien se suele declarar antes valores genericos antes de las varibles para exploradores que no soporten variables.

Las variables suele ser definidas en el elemento `:root`. Este es un pseudo-class selector que refiere a la raiz del documento, usualmente el elemento html. Las variables definidas ene este selector estan disponibles globalmente.

El valor de la variable se puede modificar en un selector.

Las variables pueden ayudarte a usar media queries. Por ejemlpo, cuando la pantalla es mas grande o pequeña que tu media query break point, puedes cambiar el valor y se aplicara el estilo donde se use.

## Diseño Visual

El diseño visual es una combinacion de tipografia, graficos, animacion, layout de la pagina, y mas para ayudar a enviar un mensaje unico.

### Tags Usados

    <u>
Da estilo de subrayado al texto.

    <em>
Da estilo de cursiva.

    <s>
Da estilo de tachado.

    <hr>
Crea una raya horizontal.

### Propiedades usadas

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
- blur-radius
- spread-radius (opcional)
- color (opcional)

Se pueden crear varias sombras agregando comas.

    opacity: 0.5;
Agrega opacidad al elemento puede ir de 0 a 1.

    text-transform: lowercase;
Tansforma el texto. lowercase (minusculas), uppercase(mayusculas), capitalize (la primera letra mayuscula), initial(la inicial), inherit(hereda del padre) y none.

    line-height: 25px;
Da el espaciado entre lineas del texto.

    a:hover {}
Este selector permite modificar el anchor cuando esta en el estado indicado.

### Cambiar la posicion de elementos

    position: relative;
Permite especificar como mover elementos relativamente a su posicion por default. Al cambiar el elemento de su posicion, el resto de elementos se comporta como si este estuviera en su posicion por default.

    bottom: 10px:
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

### Colors