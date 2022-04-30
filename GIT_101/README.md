# GIT BASICO
[x]https://www.youtube.com/watch?v=RGOj5yH7evk

cheat sheet 
https://www.freecodecamp.org/news/git-cheat-sheet/

formas de escribir commit
https://github.com/angular/angular/blob/master/CONTRIBUTING.md#commit

continuar lectura de el tutorial
[ ] https://www.freecodecamp.org/news/learn-the-basics-of-git-in-under-10-minutes-da548267cc91/

[ ] Libro epub Pro GIT

## GIT Workflow

![workflow](/imagenes/GIT1.png "Workflow")

## GIT Comandos mas usados

    git init 
Inicia el repo en la carpeta elegida.

    git remote add origin git@githhub.com:victorlb87/repo.git
Concecta un repo local con el remoto.

    git remote -v
Muestra el repo que se esta usando.

    git branch -M main
Cambia el nombre de master a main.

    git push -u origin main
Conecta el nuevo repositorio a github.

    git clone xxxx
Copia un repositorio en tu pc.

    git status
Muestra estatus de los archivos locales respecto al repo.

    git add xxx.txt
Agrega el archivo y cambios al commit. Se usa . para agregar todos los cambios.

    git commit -m "added file" -m "descripcion"
Salva el archivo en git. m se usa para agregar un mensaje al commit y un segundo para de scripcion. Si se escribe -am se agrega cambios de archivos modificados a la vez del commit.

    ssh-keygen -t rsa -b 4096 -C "email@"
genera clave para el push

    git push 
Sube los archivos en commit a github.

    git pull 
Descarga cambios de un repo a tu pc.

## Branching
![branching](/imagenes/GIT2.png "branching")

    git checkout branch
Permite movernos en el arbol del git.

    git checkout -b namebranch
Crea un branch.

    git diff testbranch 
Muestra los cambios entre el branch y main

    git branch -d testbranch
Borra branch.

## Retroceder cambios

**RECORDAR** .gitignore contiene los archivos que git ignorara cuando revise modificaciones en el repositorio

    git reset o git reset archivo
Borra cambios

    git reset HEAD~1
Permite retroceder commits segun el nuemro que se indica, en el ejemplo se retrocede 1 commit. Tambien se puede elegir un commit del log para borrar los cambios del commit elegido.

    git log 
Muestra los commits.

    git reset --hard numerodecommit
Retrocede los cambios realizados al commit elegido.


