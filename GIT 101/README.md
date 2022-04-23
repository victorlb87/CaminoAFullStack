# GIT BASICO

## GIT Workflow

![workflow](/imagenes/GIT1.png "Workflow")
![branch](/imagenes/GIT2.png "branch")


## GIT Comandos mas usados

    git init 
inicia el repo en la carpeta elegida

    git remote add origin git@githhub.com:victorlb87/repo.git
concecta un repo local con el remoto.

    git clone xxxx
Copia un repositorio en tu pc.

    git status
Muestra estatus de los archivos locales respecto al repo.

    git add xxx.txt
Agrega el archivo y cambios al commit. Se usa . para agregar todos los cambios.

    git commit -m "added file" -m "descripcion"
Salva el archivo en git. m se usa para agregar un mensaje al commit y un segundo para descripcion.

    ssh-keygen -t rsa -b 4096 -C "email@"
genera clave para el push

    git push xxx.txt
Sube el archivo a un repo remoto como github.

    git pull xxx.txt
Descarga cambios de un repo a tu pc.

