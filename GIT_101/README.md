# GIT BASICO

[x]https://www.youtube.com/watch?v=RGOj5yH7evk

Cheat sheet:
https://www.freecodecamp.org/news/git-cheat-sheet/

Formas de escribir commit:
https://github.com/angular/angular/blob/master/CONTRIBUTING.md#commit

Continuar lectura de el tutorial:
[ ] https://www.freecodecamp.org/news/learn-the-basics-of-git-in-under-10-minutes-da548267cc91/

[ ] Libro epub Pro GIT

Otros recursos: 
https://git-scm.com/docs/git-commit 

----------------

## GIT Workflow

![workflow](/GIT_101/imagenes/GIT1.png "Workflow")

## The Three States 

![workingtree](/GIT_101/imagenes/workingtree.png "Working tree")

Modified means that you have changed the file but have not committed it to your database yet. Staged means that you have marked a modified file in its current version to go into your next commit snapshot. Committed means that the data is safely stored in your local database. 

This leads us to the three main sections of a Git project: the working tree, the staging area, and the Git directory.

The basic Git workflow goes something like this:
1. You modify files in your workingtree.
2. You selectively stage just those changes you want to be part of your next commit, which adds only those changes to the staging area. 
3. You do a commit, which takes the files as they are in the staging area and stores that snapshot permanently to your Git directory. 

--------------

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
Salva el archivo en git -m se usa para agregar un mensaje al commit y un segundo para de descripcion. Si se escribe -a se agrega cambios de archivos modificados a la vez del commit.
La opción --amend te permite cambiar tu último commit. 

    ssh-keygen -t rsa -b 4096 -C "email@"
genera clave para el push

    git push 
Sube los archivos en commit a github.

    git pull 
Descarga cambios de un repo a tu pc.

---------------

## Branching
![branching](/GIT_101/imagenes/GIT2.png "branching")

    git checkout branch
Permite movernos en el arbol del git.

    git checkout -b namebranch
Crea un branch.

    git diff testbranch 
Muestra los cambios entre el branch y main

    git branch -d testbranch
Borra branch.

-------------

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

----------
## Formas de escribir commits 

Each commit message consists of a header, a body, and a footer.
```
 <header> 
 <BLANK LINE>
 <body>
 <BLANK LINE>
 <footer> 

```
The header is mandatory and must conform to the Commit Message Header format. 

The body is mandatory for all commits except for those of type "docs". When the body is present it must be at least 20 characters long and must conform to the Commit Message Body format. 

The footer is optional. The Commit Message Footer format describes what the footer is used for and the structure it must have. 

```
<type>(<scope>): <short summary>
  │       │             │
  │       │             └─⫸ Summary in present tense. Not capitalized. No period at the end.
  │       │
  │       └─⫸ Commit Scope: animations|bazel|benchpress|common|compiler|compiler-cli|core|
  │                          elements|forms|http|language-service|localize|platform-browser|
  │                          platform-browser-dynamic|platform-server|router|service-worker|
  │                          upgrade|zone.js|packaging|changelog|docs-infra|migrations|ngcc|ve|
  │                          devtools
  │
  └─⫸ Commit Type: build|ci|docs|feat|fix|perf|refactor|test
```

### Type

Must be one of the following: 
- build: Changes that affect the build system or external dependencies (example scopes: gulp, broccoli, npm) 
- ci: Changes to our Cl configuration files and scripts (examples: CircleCi, SauceLabs)
- docs: Documentation only changes 
- feat: A new feature /ADD : Se genera una nueva funcionalidad.
- fix: A bug fix 
- perf: A code change that improves performance 
- refactor: A code change that neither fixes a bug nor adds a feature
- test: Adding missing tests or correcting existing tests 

### Scope 

The scope should be the name of the npm package affected (as perceived by the person reading the changelog generated from commit messages). 

### Summary 
Use the summary field to provide a succinct description of the change:
 - use the imperative, present tense: "change" not "changed" nor "changes" 
 - don't capitalize the first letter 
 - no dot (.) at the end 

### Commit body
Just as in the summary, use the imperative, present tense: "fix" not "fixed" nor "fixes". 

Explain the motivation for the change in the commit message body. This commit message should explain why you are making the change. You can include a comparison of the previous behavior with the new behavior in order to illustrate the impact of the change. 

### Footer
The footer can contain information about breaking changes and deprecations and is also the place to reference GitHub issues, Jira tickets, and other PRS that this commit closes or is related to 