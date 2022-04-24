# BASH

[ ] https://www.freecodecamp.org/news/command-line-for-beginners/

[x] como buscar https://www.freecodecamp.org/news/how-to-search-for-files-from-the-linux-command-line/

[ ] https://www.edx.org/es/course/linux-commands-shell-scripting?index=spanish_product&queryID=65e9fabbd0ade114a45dbe93af168d7c&position=1

## Comandos mas usados

    ls 
Lista contenidos en el directorio. Al agregar -a se muestran los ocultos.

    find /path/ -type f -name file-to-search
Busca archivo. Donde path es el directorio a buscar `.` es para indicar el actual directorio. -type el tipo. f es para archivos normales y ocultos se puede cambiar po d (directorio), l (symbolic como accesos directos), c (character devices) y b (block devices). Podemos usar `.*` como nombre para buscar archivos ocultos.

    clear
Limpia pantalla.

    pwd
Imprime directorio actual.

    cd desktop 
Cambia directorio al mencionado. `cd ..` cambia al directorio que contiene en el que estas. `cd` te lleva al home.

    mkdir nuevacarpeta
Crea un nuevo directorio.

    rmdir nuevacarpeta
Borra la carpeta.

    touch nuevo.txt
Crea nuevo archivo.

    rm nuevo.txt
Borra archivo.

    cp nuevo.txt carpeta1 o cp carpeta1 carpeta2
    cp test.txt copiatest.txt O cp test.txt ./testFolder/testCopy.txt
Copia un archivo o directorio. Si se desea hacer una copia del mismo archivo solo se elige el nuevo nombre del la copia .

    mv archivo.txt */destino/
Mueve el archivo a la carpeta elegida.

    head readme.md
Lee la primera linea de un archivo.

    tail readme.md
Lee la ultima linea de un archivo.

    command --help
Te da informacion del comando.

    [ctrl] + C
Cierra procesos.

    [ctrl] + [shift] + C / [ctrl] + [shift] + V
Copiar y pegar texto.

    exit
Cierra terminal.

    [Tab] o [Tab] + [Tab]
Autocompleta segun tu historial y 2 veces te muestra sugerencias

