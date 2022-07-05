# Git-Basic-Commands
Práctica de Curso Profesional de Git y GitHub
### Features

- A list of commonly used Git and Terminal commands; 
- Terminal Commands / Comandos de la Terminal;
- Config Git / Configuracion de Git;
- Config SSH Keys / Configuracion de Credenciales SSH;
- Creating Projects / Creacion de proyectos;
- Basic Snapshotting / Snapshooting Basico;
- Branching & Merging / Ramas y fusionar;
- Sharing & Updating Projects / Compartiendo y Repositorios Remotos
- Inspection & Comparison / Inspeccion y Comparacion
- Others / Otros

# Editor.md

![](https://pandao.github.io/editor.md/images/logos/editormd-logo-180x180.png)

![](https://img.shields.io/github/stars/pandao/editor.md.svg) ![](https://img.shields.io/github/release/pandao/editor.md.svg) ![](https://img.shields.io/github/issues/pandao/editor.md.svg) ![](https://img.shields.io/bower/v/editor.md.svg)


**Table of Contents**

[TOCM]

[TOC]

-------------
###Blockquotes

> "Today is still yesterday never again"


###Sequence Diagram
                    
```seq
Andrew->China: Says Hello 
Note right of China: China thinks\nabout it 
China-->Andrew: How are you? 
Andrew->>China: I am good thanks!
```
                    
```seq
Andrew->China: Says Hello 
Note right of China: China thinks\nabout it 
China-->Andrew: How are you? 
Andrew->>China: I am good thanks!
```

###End


### Terminal Commands / Comandos de la Terminal

| Command | Description | Descripción |
| ------- | ----------- | ------------ |
| `cd [rute]` | To change directory | Cambia el directorio |
| `mkdir [name]` | Make directory | Crea una nueva carpeta |
| `ls -al` | List information about the files | Lista los archivos del directorio |
| `clear` | clear the terminal screen | Limpia la Terminal |
| `Touch [name.txt]` | create a empty file | Crea un archivo vacio |
| `rm [file]` | remove files | Elimina un archivo |
| `rm -rf [dir]` | remove directories | Elimina una carpeta |
| `pwd` | Print name of current/working directory | Muestra el directorio donde nos encontramos |
| `mv` | move (rename) files | Mueve o renombra archivos |
| `cat [name.txt]` | Concatenate files and print on the standard output | Vista previa del contenido del archivo |
| `sudo` | execute a command as another user | Ejecuta un commando como administrador |

### Config Git / Configuracion de Git

| Command | Description | Descripción |
| ------- | ----------- | ------------ |
| `git config --global user.name "name-example"` | Add a user name | Añade un nombre de usuario |
| `git config --global user.email user@example.com` | Add a email for user | Añade un correo del usuario |
| `git config --list` | List all setings | Muestra todas las configuraciones |

### Config SSH Keys / Configuracion de Credenciales SSH

| Command | Description | Descripción |
| ------- | ----------- | ------------ |
| `ssh-keygen -t rsa -b 4096 -C "Email"` | Generate SSH key | Generar credencial SSH |
| `eval $(ssh-agent -s)` | Verify ssh agent | Verifica la existencia del servidor de credenciales SSH |
| `ssh-add [rute]` | Add SSH key to your workspace | Agrega la credencial SSH al entorno de trabajo |

### Creating Projects / Creacion de proyectos

| Command | Description | Descripción |
| ------- | ----------- | ------------ |
| `git init` | Initialize a local Git repository and create a carpet| Inicia un repositorio local de Git y crea la carpeta |
| `git clone [url]` | Create a local copy of a remote repository | Crea una copia local de un repositorio remoto |

### Basic Snapshotting / Snapshooting Basico

| Command | Description | Descripción |
| ------------------------ | ----------- | ----------- |
| `git status` | Check status repository | Verifica el estatus del repositorio |
| ​🌏​🌲​🌳​💻​`git add`|  |  |
| `git add [file-name.txt]` | Add a file to the staging area | Añade un archivo al area de preparación |
| `git add .` | Add all new and changed files to the staging area | Añade todos los archivos al area de preparación |
| `git add -A` | Add all files to the staging area. It's the same that add . | Añade todos los archivos al area de preparación. = add . |
| `git add - n [file-name.txt]` | Simulate adding a file | Simula el agregado de un [archivo] |
| ​🌏​🌲​🌳​💻​`git commit`|  |  |
| `git commit -m "[commit message]"` | Add changes from stagging area to repository | Añade los archivos del área de stagging al repositorio |
| `git commit -am "[commit message]"` |Add files from stagging area to repository and commit | Añande los cambios del stagging area al repositorio y hace commit |
| `git commit -amend "[commit message]"` | Add changed files at the earlier commit | Añade los cambios al anterior commit. Si se escribe un mensaje este sobreescribe el anterior.|
| ​🌏​🌲​🌳​💻​`git rm`|  |  |
| `git rm -r [file-name.txt]` | Remove a file (or folder) | Elimina archivos o carpetas La diferencia entre esto y simplemente borrar el archivo directamente es que se guarda en git un registro de eliminación. La diferencia entre esto y simplemente borrar el archivo directamente es que se guarda en git un registro de eliminación.|
| `git rm --cached` | Remove a file (or folder) from stagging area to working directory | Elimina archivos o carpetas del área de stagging al directorio de trabajo |
| `git rm -f ` | Remove a file (or folder) del stagging area and the working directory | Elimina archivos o carpetas del área de stagging y del directorio de trabajo |
| ​🌏​🌲​🌳​💻​`git reset` |  |  |
| `git reset --soft [sha1]` | Ammend the last commit | orrar todos los commits posteriores a [sha1]. Este comando resetea el HEAD al [sha1] mas no modifica ningún archivo. Quedan en el stagging para un commit posterior. |
| `git reset --mixed [sha1]` | Ammend the last commit | orrar todos los commits posteriores a [sha1]. Los archivos que salen del repositorio son pasados al working directory. |
| `git reset --hard [sha1]` | Ammend the last commit | elimina todos los cambios incluso del working directory. |
| `git reset HEAD` | Ammend the last commit | saca los archivos del staging area. Este comando no elimina ningún archivo ni borra commits del git. |

### Branching & Merging / Ramas y fusionar

| Command | Description | Descripción |
| ------- | ----------- | ----------- |
| ​🌏​🌲​🌳​💻​`git branch` |  |  |
| `git branch` | List branches (the asterisk denotes the current branch) | Lista todas las ramas |
| `git branch -a` | List all branches (local and remote) | Lista todas las ramas locales y remotas |
| `git branch [branch name]` | Create a new branch | Crea una nueva rama |
| `git branch -d [branch name]` | Delete a branch | Elimina una rama |
| `git branch [nombre]` | Create a new branches | Crear la rama [nombre]|
| `git branch -l`| list all branches| lista las ramas|
| `git branch -r` | |Muestra todas las ramas remotas|
| `git branch -a`| | Muestra todas las ramas tanto locales como remotas|
| `git branch -d [nombre]`|| elimina el branch [nombre]. Esto solo funciona si el branch no tiene ningún commit.|
| `git branch -D [nombre]`|| fuerza la eliminación de un branch sin importar si tiene commits|
| `git branch -m [nombre inicial] [nuevo nombre]` ||renombra el branch [nombre inicial] por [nuevo nombre]|
| ​🌏​🌲​🌳​💻​`git show` |  |  |
| `git show-branch --all` | List all branches local | Lista todas las ramas en local |
| ​🌏​🌲​🌳​💻​`git push` |  |  |
| `git push origin --delete [branch name]` | Delete a remote branch | Elimina una rama remota |
| 💧`git checkout` |  |  |
| `git checkout -b [branch name]` | Create a new branch and switch to it | Crea una nueva rama y cambia a ella |
| `git checkout -b [branch name] origin/[branch name]` | Clone a remote branch and switch to it | Clona una rama remota y cambia a ella |
| `git checkout [branch name]` | Switch to a branch | Cambiar a una rama determinada |
| `git checkout -` | Switch to the branch last checked out | Cambia a la ultima rama seleccionada |
| `git checkout -- [file-name.txt]` | Discard changes to a file | Descarta los cambios de un archivo |
| `git checkout [brach]` ||moverse al branch [branch]|
| `git chechout [sha1]`|| ir al momento del tiempo de ese commit|
| `git chechout [sha1] [archivo]` ||ir al momento del tiempo de ese commit de un archivo |específico.|
| `git checkout -b [nombre]` ||Crea un branch y se mueva al mismo|
| `git checkout -- [archivo]` ||Descarta todos los cambios del archivo|
| ​🌏​🌲​🌳​💻​`git merge` |  |  |
| `git merge [branch name]` | Merge a branch into the active branch | Fusiona una rama a la rama activa
| `git merge [source branch] [target branch]` | Merge a branch into a target branch | Fusiona una rama a una rama determinada |
| `git merge [branch]` | Mixed the branch wit actual |mezcla el branch [branch] con el branch actual
| ​🌏​🌲​🌳​💻​ | others |  |
| `git rebase [branch]`| |mezcla el [branch] con el branch actual. Es como el merge pero sin |crear bifurcaciones. Para que funcione bien, primero se hace rebase a la rama con los |cambios que queremos modificar y luego rebase a la rama final.
| `git stash` | Stash changes in a dirty working directory | |
| `git stash clear` | Remove all stashed entries ||
| `fork` | Copy a external repository | Copa un repositorio externo |

### Sharing & Updating Projects / Compartiendo y Repositorios Remotos

| Command | Description | Descripción |
| ------- | ----------- | ----------- |
| ​🌏​🌲​🌳​💻​`git push` |  |  |
| `git push origin [branch name]` | Push a branch to your remote repository | Envia el repositorio local a remoto |
| `git push origin --delete [branch name]` | Delete a remote branch | Elimina un repositorio remoto |
| `git push --tags` | Push tags to your repository | Envia los tags al repositorio remoto |
| `git push origin :refs/tags/[name]` | Delete a tag from GitHub | Elimina un tag dentro de GitHub |
| ​🌏​🌲​🌳​💻​`git pull` |  |  |
| `git pull` | Update local repository to the newest commit |
| `git pull origin [branch name]` | Pull changes from remote repository | Hace un feth y fusiona |
| `git pull [origin] [branch]` || hace un fetch mas merge, me trae lo que haya en la web |
| ​🌏​🌲​🌳​💻​`git remote` |  |  |
| `git remote add origin ssh://git@github.com/[username]/[repository-name].git` | Add a remote repository | Conecta un repositorio remoto con uno local. Por defecto el nombre es origin |
| `git remote -v` | list remote connections | Lista las conexiones remotas |
| `git remote set-url [branch name] [url]` | Change the url | Cambia la url del repositorio |
| `git remote remove [nombre]` ||remueve una conexión remota|
| ​🌏​🌲​🌳​💻​`git fetch` |  |  |
| `git fetch [nombre] [branch]` ||traer . Solo los trae pero no lo mezcla|
| ​🌏​🌲​🌳​💻​`git merge` |  |  |
| `git merge [origin/master] --allow-unrelated-histories` ||hace un merge del fetch con el repositorio local|
| ​🌏​🌲​🌳​💻​`git pull` |  |  |
| `git push [origin] [master]` || envia al repositorio local al remoto|
| `git push --all origin` ||push a todos los branch y tags|
| ​🌏​🌲​🌳​💻​`git clone` |  |  |
| `git clone [ruta]`     |  |trae el repositorio a la computadora|
| ​🌏​🌲​🌳​💻​`git fork` |  |  |
| `fork`    | |hace una copia de un repositorio externo a nuestra cuenta|
| ​🌏​🌲​🌳​💻​`git tags` |  |  |
| revisar`git -tags`   | | Enviar los tags|

### Inspection & Comparison / Inspeccion y Comparacion

| Command | Description | Descripción |
| ------- | ----------- | ----------- |
| `git log` | View changes | Muestra los cambios en el repositorio |
| `git log --summary` | View changes (detailed) | Muestra los cambios en el repositorio detalladamente |
| `git log --stat` | V  | Explica el número de líneas que se cambiaron y te muestra que se cambió en el contenido|
| `git log -online` | V  | Resumido | 
| `git log -graph` | V  | Ver las ramificaciones | 
| `git log [numero]` | V  | Ver los ultimos [numero] commits |
| `git log --author="Name Author"`` | V  |  nuestra los los logs de un autor |
| `git log -all --graph --decorate --oneline` | View changes (Max-detailed) | Muestra todos los cambios del repositorio detallada y graficamente |
| ​🌏​🌲​🌳​💻​`git diff` |  |  |
| `git diff [sha1 del commit]` | Preview changes before merging | Muestra la diferencias del commit [sha1] |
| `git diff [source branch] [target branch]` | Preview changes before merging | Compara los diferentes cambios |
| `git diff [sha1-1] [sha1-2]` | Preview changes before merging | diferencia entre la version 1 vs la version 2. |
| ​🌏​🌲​🌳​💻​`git tag` |  |  |
| `git tag -a [tag] -m ["comentario"]` | Add tag with a comment at least commit | Agrega el tag con un comentario al ultimo commit.  |
| `git tag -l` | List tags | Lista todos los tags.  |
| `git tag [tag] [sha1 del commit]` | Add one tag a particular commit | agrega un tag a un commit en particular  |
| `git tag -d [tag]` | Delete tad| Elimina el tag.  |
| `git tag -d [name]` | Delete a tag | Elimina un tag en especifico |
| `git tag -f -a [nuevo tag] [sha1 del commit]` | Rename sdasdasdasd | renombra el tag del commit pero deja el anterior tag.  |
| `git tag -a [name] -m "message" [id/hashtag]` | Create a tag for a commit | Crea un tag de un commit en especifico |
| `git relog [numero]` |  V  | muestra el log completo de git, incluido branches eliminados.|
| ​🌏​🌲​🌳​💻​`git show` |  |  |
| `git show` |  V  | muestra los últimos cambios que se han hecho en el commit.|
| `git show-ref --tags` | List all tags | Lista los tags existentes |


### Others / Otros

| Command | Description | Descripción |
| ------- | ----------- | ----------- |
| `alias [name=] "command"` | Create a shorcut for a command | Crea un alias para llamar a un comando |
| `gitk` | Open GUI | Abre una interfaz grafica |
| `git cherry.pick [id]` | |Take commit from other branches | Trae un commit especifico desde otra rama |
| `git grep -n [word]` | |Search words in the proyect | Busca la palabra especificada en todo el proyecto |
| `git relog [numero]` | V  | muestra el log completo de git, incluido branches eliminados. |
| ​🌏​🌲​🌳​💻​`git stash` |  |  |
| `git stash` | |es un limbo como el staging area. Te permite cambiar de branch sin hacer commit.|
| `git stash list`| |ver la lista de los stash.|
| `git stash pop`| |aplica el ultimo stash a la rama actual.|
| `git stash branch [brach]`| |mueve el stash al [branch]|
| `git stash drop stash@{numero}`| |elimina el stash.|
| `git stash apply stash@{numero}`| |aplica el stash.|
| ​🌏​🌲​🌳​💻​`git clean |  |  |
| `git clean`| |elimina los archivos que no están bajo el control de versión. Para que funcione es necesario usar alguno de los flags:|
| `git clean n`| |no remueve nada, solo te muestra los archivos que va a eliminar.|
| `git clean f`| |elimina los archivos que no se encuentran versionados.|
| ​🌏​🌲​🌳​💻​`git cherry` |  |  |
| `git cherry pick [sha1]`| |mover el commit [sha1] de otro branch al branch actual.|
| ​🌏​🌲​🌳​💻​`git shortlog` |  |  |
| `git shortlog -sn`| |muestra cuantos commit han hecho cada miembros del equipo.|
| `git shortlog -sn --all`| |muestra cuantos commit han hecho cada miembros del equipo hasta los que han sido eliminado|
| `git shortlog -sn --all --no-merge`| |muestra cuantos commit han hecho cada miembros quitando los eliminados sin los merges|
| ​🌏​🌲​🌳​💻​`git blame` |  |  |
| `git blame [archivo]`|  |muestra quien hizo cada cosa linea por linea|
| `git blame [archivo] -L[linea_inicial],[linea_final]`| |muestra quién hizo cada cosa linea por linea indicándole desde qué linea ver. Ejemplo `L35,50|`
| ​🌏​🌲​🌳​💻​`Others` |  |  |
| `git [comando] --help` | |muestra cómo funciona el comando.|

*Comandos para trabajar en Git y GiyHub*
