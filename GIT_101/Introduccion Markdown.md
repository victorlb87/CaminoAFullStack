# ​Guia markdown  

​Revisar siguiente contenido: 
[x] ​-​ https://www.markdownguide.org/  ✅
[ ] ​-​ https://dave.autonoma.ca/blog/2019/05/22/typesetting-markdown-part-1/ ❎
[x] ​-​ https://docs.gitlab.com/ee/user/markdown.html 
[x] - https://docs.github.com/es/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax
 

Lista de Herramientas y otros recursos
​- https://github.com/mundimark/awesome-markdown 
- https://docs.github.com/es/get-started/writing-on-github/working-with-advanced-formatting

------
## Los Usos mas comunes

"#" para poner titulos y con mas # se hacen los subtitulos 
## Ejemplo

">" par poner citas
>Esto es una cita

"-,*" para hacer una lista desordenada
- item1
* item2

"1." para hacer lista numeradas
1. item3

"   -item3" para anidar con espacio
1. item 4
    - item5

"___" linea para separar texto
___ 

Horizontal Lines
     * * *   /  -------  / - - -

"**" para hacer texto cursiva  y doble para negrita
*texto en cursiva*
**texto en negrita**

"~~" para hacer texto tachado
~~texto tachado~~

"[](wwwxx"titulo")" para agregar texto con hipervinculos
[google](www.google.com)

"<>" para agregar link con texto
<www.google.com>

"![](xxxxxx"titulo")" para agregar imagenes con viculos.

![imagen google](https://www.google.com.mx/images/branding/googlelogo/1x/googlelogo_color_272x92dp.png "google")

Link
[ ejemplo] [id]
[id]: www.google.com " Titulo opcional "

se puede usar el texto del link sin necesidad del id, también se puede referenciar directorios:

     [I'm a relative reference to a repository file](../blob/master/LICENSE)

Para imagenes se puede usar de la misma forma que link solo que con ! adelante.

4 espacios o `` para agregar una linea que refiera a codigo

    HTML

los Titulos `h1` se usa en HTML `h1` 
 
"~~~" para agregar bastante codigo
~~~html
Linea de codigo 1 
Linea de codigo 2
Linea de codigo 3
~~~~

"\" para anular markdown

"||" para generar tabla separado por tab

|asd    |asd    |asd    |
|-------|-------|-------|
|123    |123    |rtger  |
|vv |vsdvb  |dfbbdf |

Footnotes

Here is a simple footnote[^1].  
[^1]: My reference.

Youtube Video
```html
<a href="http://www.youtube.com/watch?feature=player_embedded&v=YOUTUBE_VIDEO_ID_HERE
" target="_blank"><img src="http://img.youtube.com/vi/YOUTUBE_VIDEO_ID_HERE/0.jpg" 
alt="IMAGE ALT TEXT HERE" width="240" height="180" border="10" /></a>
```
o en puro markdown   
       [![IMAGE ALT TEXT HERE](http://img.youtube.com/vi/YOUTUBE_VIDEO_ID_HERE/0.jpg)](http://www.youtube.com/watch?v=YOUTUBE_VIDEO_ID_HERE)

-------------
## GITHUB

<!-- GITHUB MARKDOWN -->

Para hacer checklist (solo funciona en GITHUB)

* [x] Task 1
* [ ] Task 2
* [ ] Task 3
* [ ] Task 4

Se pueden usar emojis, hay lista en la pagina de github :smiley: :monkey:

------------------
### Colores

You can write a color in the formats: HEX, RGB, or HSL.
HEX: `#RGB[A]` or `#RRGGBB[AA]` 
RGB: `RGB[A](R, G, B[, A])` 
HSL: `HSL[A](H, S, L[, A])`

por ejemplo:
- `#F00`
- `#F00A`

-------------
### Diagrams and flowcharts

You can generate diagrams and flowcharts from text by using Mermaid or PlantUML.
You can also use Kroki to create a wide variety of diagrams.

--------------
### Math

Math written in LaTeX syntax is rendered with KaTeX.
Math written between dollar signs $ is rendered inline with the text. Math written in a code block with the language declared as math is rendered on a separate line:

------------------
### Table of contents

A table of contents is an unordered list that links to subheadings in the document. You can add a table of contents to issues and merge requests, but you can't add one to notes or comments. Add either the [[_TOC_]]

------------------------
### Enlaces relativos

Puedes definir enlaces relativos y rutas de imagen en los archivos representados para ayudar a que los lectores naveguen hasta otros archivos de tu repositorio.

Un enlace relativo es un enlace que es relativo al archivo actual. Por ejemplo, si tienes un archivo README en la raíz de tu repositorio y tienes otro archivo en docs/CONTRIBUTING.md, el enlace relativo a CONTRIBUTING.md en tu archivo README podría verse así:

[Contribution guidelines for this project](docs/CONTRIBUTING.md)
