# Git-Basic-Commands
Práctica de Curso Profesional de Git y GitHub


# Let's begin

![Begin](https://user-images.githubusercontent.com/58926113/178091091-a7eecc5a-fcc4-422b-9fc9-611fc7e52382.gif)

![](https://sandynolasco.github.io/Sandynolasco/imgall/blob/main/Begin.gif)

![](https://img.shields.io/github/issues/Sandynolasco/Git-Basic-Commands) ![](https://img.shields.io/github/forks/Sandynolasco/Git-Basic-Commands) ![](https://img.shields.io/github/stars/Sandynolasco/Git-Basic-Commands)




**Práctica de Curso Profesional de Git y GitHub**

### Table of Contents
A list of commonly used Git and Terminal commands;
 
- Terminal Commands / Comandos de la Terminal
- Config Git / Configuración de Git
- Config SSH Keys / Configuración de Credenciales SSH
- Creating Projects / Creación de proyectos
- Basic Snapshotting / Snapshooting Básico
- Branching & Merging / Ramas y Fusionar
- Sharing & Updating Projects of Remote Repositories / Compartir y - actualizar proyectos de repositorios remotos (Github)
- Inspection & Comparison / Inspeccion y Comparación
- Collaborative Commands / Comandos Colaborativos
- Others / Otros
- Interesting Links / Enlaces Interesantes
- Errors / Errores (Github)


-------------
###Quotes

> "Today is still, yesterday never again"


### Terminal Commands / Comandos de la Terminal

| Command | Description | Descripción |
| ------------------------ | ----------- | ----------- |
| `cd [directoryrute]` | To change directory | Cambia el directorio |
| `mkdir [carpetname]` | Make directory | Crea una nueva carpeta |
| `ls -al` | List information about the files a [hide files]| Lista los archivos del directorio, incluye archivos ocultos |
| `clear` | Clear the terminal screen | Limpia la Terminal |
| `Touch [Name file]` | Create a empty file | Crea un archivo vacio |
| `rm [Name file]` | Remove files | Elimina un archivo |
| `pwd` | Print name of current/working directory | Muestra el directorio donde nos encontramos |
| `mv` | Move (rename) files | Mueve o renombra archivos |
| `cat [Name file]` | Concatenate files and print on the standard output | Vista previa del contenido del archivo |
| `sudo` | Execute a command as another user | Ejecuta un commando como administrador |
| `history` |  | Ultimos comandos que he ingresado |
| `Guardar y salir de vi` || Esc pausa y ingresar shif + z + z [para guardar y salir de “vi”] |
| `Escribir en vi` || Space + i [para poder empezar a escribir en “vi”] |
| `rm -rf [repo.git]` | Remove the temporary local repository | Elimina un repositorio local ó |
| `rm -f -r ~/Projects/MyProject.git` | | Eliminará un repositorio Git de línea de comandos completo |


### Config Git / Configuración de Git

| Command | Description | Descripción |
| ------------------------ | ----------- | ----------- |
| `git config --global user.name "name-example"` | Add a user name | Añade un nombre de usuario |
| `git config --global user.email user@example.com` | Add a email for user | Añade un correo del usuario |
| `git config --list` | List all setings | Muestra todas las configuraciones |
| `git config --global color.ui true` | Configure text editor | Configurar el editor del texto |


### Config SSH Keys / Configuración de Credenciales SSH

| Command | Description | Descripción |
| ------------------------ | ----------- | ----------- |
| `ssh-keygen -t rsa -b 4096 -C "Email"` | Generate SSH key | Generar credencial SSH |
| `eval $(ssh-agent -s)` | Verify ssh agent | Verifica la existencia del servidor de credenciales SSH |
| `ssh-add [rute]` | Add SSH key to your workspace | Agrega la credencial SSH al entorno de trabajo |
| `ssh-keygen -t rsa -b 4096 -C "correo@ejemploc.com"` | Generate an SSH key. The email must be the same as the one found on Github | Crea una llave SSH. El correo debe de ser el mismo que se encuentra en Github |


### Creating Projects / Creación de proyectos

| Command | Description | Descripción |
| ------------------------ | ----------- | ----------- |
| `git init [Repository name]` | Initialize a local Git repository and create a carpet| Inicia un repositorio local de Git y crea la carpeta, si se desea eliminar el repositorio, solo hay que eliminar la carpeta oculta .git |
| ​🌏​🌲​🌳​💻​`git clone` |  |  |
| `git clone [html site path]` | Bring the remote repository to the computer | Trae el repositorio a la computadora |
| `git clone --bare [html site path]`| Bring the remote repository to the computer | Trae el repositorio remoto a la computadora |


### Basic Snapshotting / Snapshooting Básico

| Command | Description | Descripción |
| ------------------------ | ----------- | ----------- |
| `git status` | Check status repository | Verifica el estatus del repositorio. `untracked files` son archivos que están en nuestro Working Directory, lo que aparezca en rojo es lo que se ha modificado y hay que pasarlo al Staging. `changes to be comitted` son los archivos que se encuentran en el staging area, aparecen en verde |
| ​🌏​🌲​🌳​💻​`git add`|  |  |
| `git add [Name file]` | Add a file to the staging area | Añade un archivo al area de preparación |
| `git add .` | Add all new and changed files to the staging area | Añade todos los archivos al area de preparación |
| `git add -A` | Add all files to the staging area. It's the same that add . | Añade todos los archivos al area de preparación. = add |
| `git add - n [Name file]` | Simulating add a file | Simula el agregado de un [archivo] |
| ​🌏​🌲​🌳​💻​`git commit`|  |  |
| `git commit -m "[commit message]"` | Add changes from stagging area to repository | Añade los archivos del área de stagging al repositorio |
| `git commit -am "[commit message]"` | Add files from stagging area to repository and commit | Añande los cambios del stagging area al repositorio y hace commit |
| `git commit --amend "[commit message]"` | Add changed files at the earlier commit | Añade los cambios al anterior commit. Si se escribe un mensaje este sobreescribe el anterior.|
| ​🌏​🌲​🌳​💻​`git rm`|  |  |
| `git rm -r [Name file]` | Remove a file (or folder)... | Elimina archivos o carpetas del área de stagging sin eliminar el historial del sistema de versiones|
| `git rm --cached [Name file]` |  | Elimina archivos o carpetas del área de stagging y del proximo commit, pero los mantiene en disco duro |
| `git rm -force ` |  |  Elimina los archivos del git y del disco duro |
| ​🌏​🌲​🌳​💻​`git reset`|  | Permite volver en el tiempo sin poder volver al futuro |
| `git reset -soft [sha1]` | | Borrar todos los commits posteriores a [sha1]. Este comando resetea el HEAD al [sha1] mas no modifica ningún archivo. Quedan en el stagging para un commit posterior,  elimina los cambios hasta el staging area --- Se borra el historial pero se mantiene los archivos del area de stagging para poder apolicar cambios al ultimo commit |
| `git reset -mixed [sha1]` | | Borra toda la información del área de stagging y de los commits |
| `git reset -hard [sha1]` | | Elimina todos los cambios incluso del working directory  regresa hasta el commit del [SHA-1] Donde el SHA-1 es el identificador del commit --- Borra toda la infromacion del area de stagging y de los commits |
| `git reset -HEAD` | | Mueve cambios de Stagging a Unstaged. Se conservan los ultimos cambios, el repositorio sigue teniendo el archivo solo con los cambios hechos en commit. Este comando no elimina ningún archivo ni borra commits del git |


### Branching & Merging / Ramas y Fusionar

| Command | Description | Descripción |
| ------------------------ | ----------- | ----------- |
| ​🌏​🌲​🌳​💻​`git branch` |  |  |
| `git branch ` | List branches (the asterisk denotes the current branch) | Lista todas las ramas locales |
| `git branch [branch name]` | Create a new branch | Crea una nueva rama [branch name] |
| `git branch -l`| List all branches| lista las ramas |
| `git branch -r` | | Muestra todas las ramas remotas |
| `git branch -a` | | Muestra todas las ramas tanto locales como remotas |
| `git branch -d [branch name]`| Delete a branch| Elimina el branch [nombre]. Esto solo funciona si el branch no tiene ningún commit |
| `git branch -D [branch name]`|| Fuerza la eliminación de una rama sin importar si tiene commits |
| `git branch -m [branch name inicial] [branch name nuevo]` | | Renombra el branch [nombre inicial] por [nuevo nombre] |
| ​🌏​🌲​🌳​💻​`git show` |  |  |
| `git show-branch --all` | List all branches local | Lista todas las ramas en local |
| ​🌏​🌲​🌳​💻​`git checkout` |  |  |
| `git checkout ` | Bring changes made | Trae cambios realizados git checkout opera sobre tres entidades distintas: archivos, confirmaciones y ramas |
| `git checkout [branch name]` | Switch to the branch last checked out | Te permite desplazarte entre las ramas creadas por git branch |
| `git checkout -b [branch name] origin/[branch name]` | Clone a remote branch and switch to it | Clona una rama remota y cambia a ella |
| `git checkout -b [branch name]` | Create a new branch and switch to it | Crea una rama y hace checkout y cambia a ella directamente |
| `git checkout -- [Name file]` | Discard changes to a file | Descarta los cambios de un archivo |
| `git checkout [sha1]`| |  Ir al momento del tiempo de ese commit |
| `git chechout [sha1] [archivo]` | |  Ir al momento del tiempo de ese commit de un archivo específico |
| ​🌏​🌲​🌳​💻​ `git merge` |  |  |
| `git merge [source branch] [target branch]` | Merge a branch into a target branch | Fusiona una rama a una rama determinada |
| `git merge [branch name]` | Mixed the branch wit actual |mezcla el branch [branch] con el branch actual |
| ​🌏​🌲​🌳​💻​ others |  |
| `git rebase [branch name]`| | Mezcla el [branch] con el branch actual. Es como el merge pero sin crear bifurcaciones. Para que funcione bien, primero se hace rebase a la rama con losCambios que queremos modificar y luego rebase a la rama final  |
| ​🌏​🌲​🌳​💻​ `git clean` |  |
| `git clean`| | Elimina los archivos que no están bajo el control de versión. Para que funcione es necesario usar alguno de los flags:|
| `git clean n`| | No remueve nada, solo te muestra los archivos que va a eliminar |
| `git clean f`| | Elimina los archivos que no se encuentran versionados |


### Sharing & Updating Projects of Remote Repositories / Compartir y actualizar proyectos de repositorios remotos (Github)

| Command | Description | Descripción |
| ------------------------ | ----------- | ----------- |
| ​🌏​🌲​🌳​💻​`git fork` |  |  |
| `fork` || Hace una copia de un repositorio externo a nuestra cuenta |
| ​🌏​🌲​🌳​💻​`git remote` |  |  |
| `git remote add origin ssh://git@github.com/[username]/[repository-name].git` | Add a remote repository | Conecta un repositorio remoto con uno local. Por defecto el nombre es origin |
| `git remote -v` | List remote connections | Lista las conexiones remotas |
| `git remote set-url [branch name] [url]` | Change the url | Cambia la url del repositorio |
| `git remote add [nombre] [ruta]` | Connect a remote repository with a local one. By default the name is origin | Conecta un repositorio remoto con uno local. Por defecto el nombre es origin |
| `git remote remove [nombre]` | Remove remote conexion | Remueve una conexión remota |
| ​🌏​🌲​🌳​💻​`git push` |  |  |
| `git push origin [branch name]` | Push a branch to your remote repository | Envia el repositorio local a remoto |
| `git push origin --delete [branch name]` | Delete a remote branch | Elimina un repositorio remoto |
| `git push --tags` | Push tags to your repository | Envia los tags al repositorio remoto |
| `git push origin :refs/tags/[name]` | Delete a tag from GitHub | Elimina un tag dentro de GitHub |
| `git push --set-upstream origin main` | Push to GitHub | Sube a GitHub |
| `git push [origin] [master]` | | Envia al repositorio local al remoto
| `git push --all origin` | | Push a todos los branch y tags |
| `git push --u rama main` | | Push a todos los branch |
| `git push --mirror [url]` | This will get all the branches and tags that are available in the upstream repository and will replicate those into the new location. Warning: Don’t use git push --mirror in repositories that weren’t cloned by --mirror as well. It’ll overwrite the remote repository with your local references (and your local branches). This is not what we want. Read the next section to discover what to do in these cases. Also git clone --mirror is preferred over git clone --bare because the former also clones git notes and some other attributes |  |
| ​🌏​🌲​🌳​💻​`git fetch` |  |  |
| `git fetch [nombre] [branch name]` | | Solo los trae pero no lo mezcla |
| ​🌏​🌲​🌳​💻​`git merge` |  |  |
| `git merge [origin/master] --allow-unrelated-histories` | | Hace un merge del fetch con el repositorio local |
| ​🌏​🌲​🌳​💻​`git pull` |  |  |
| `git pull [origin] [master]` | | Hace un feth y fusiona, hace git fetch + git merge, me trae lo que haya en la web, envia el repositorio local al remoto |
| `git pull --all origin` || Push a todos los branch y tags |


### Inspection & Comparison / Inspeccion y Comparación

| Command | Description | Descripción |
| ------------------------ | ----------- | ----------- |
| ​🌏​🌲​🌳​💻​`git log` |  |  |
| `git log` | View changes | Muestra los cambios en el repositorio |
| `git log --summary` | View changes (detailed) | Muestra los cambios en el repositorio detalladamente |
| `git log --stat` | Explain the number of lines that were changed and shows you that it was changed in the content  | Explica el número de líneas que se cambiaron y te muestra que se cambió en el contenido |
| `git log -online` | Resume  | Resumido | 
| `git log -graph` | See the branches  | Ver las ramificaciones | 
| `git log [number]` | See the last [number] commitments | Ver los ultimos [numero] commits |
| `git log --author="Name Author"` | Shows an author's logs  |  Muestra los logs de un autor |
| `git log --all --graph --decorate --oneline` | View changes (Max-detailed) | Muestra todos los cambios del repositorio detallada y graficamente |
| `git relog [number]` |  Show full git log, including removed branches  | Muestra el log completo de git, incluido ramas eliminados |
| `gitk` | Open GUI | Abre una interfaz grafica con el historial del repositorio |
| ​🌏​🌲​🌳​💻​`git diff` |  |  |
| `git diff [sha1 del commit]` | Preview changes before merging | Muestra la diferencias del commit [sha1] |
| `git diff [sha1-1] [sha1-2]` | Preview changes before merging | diferencia entre la version 1 vs la version 2 |
| ​🌏​🌲​🌳​💻​`git tag` |  |  |
| `git tag -a [tag] -m ["message"]` | Add tag with a comment at least commit | Agrega el tag con un comentario al ultimo commit |
| `git tag -a [tag] -m "message" [id/hashtag]` | Create a tag for a commit | Crea un tag de un commit en especifico |
| `git tag [tag] [sha1 del commit]` | Add one tag a particular commit | Agrega un tag a un commit en particular  |
| `git tag -l` | List tags | Lista todos los tags  |
| `git tag -d [tag]` | Delete a tag | Elimina un tag en específico |
| `git tag -f -a [nuevo tag] [sha1 del commit]` | Rename sdasdasdasd | Renombra el tag del commit pero deja el anterior tag.  |
| ​🌏​🌲​🌳​💻​`git show` |  |  |
| `git show-ref --tags` | List all tags | Lista los tags existentes |
| `git show` | Shows the latest changes that have been made to the commit | Muestra los últimos cambios que se han hecho en el commit |


### Collaborative Commands / Comandos Colaborativos

| Command | Description | Descripción |
| ------------------------ | ----------- | ----------- |
| ​🌏​🌲​🌳​💻​`git shortlog` |  |  |
| `git shortlog -sn`| | Muestra cuantos commit han hecho cada miembros del equipo |
| `git shortlog -sn --all`| | Muestra cuantos commit han hecho cada miembros del equipo hasta los que han sido eliminado |
| `git shortlog -sn --all --no-merge`| | Muestra cuantos commit han hecho cada miembros quitando los eliminados sin los merges |
| ​🌏​🌲​🌳​💻​`git blame` |  |  |
| `git blame [archivo]`|  | Muestra quien hizo cada cosa línea por línea |
| `git blame [archivo] -L[línea_inicial],[línea_final]`| | Muestra quién hizo cada cosa línea por línea indicándole desde qué línea ver. Ejemplo `L35,50|`
| `git [comando] --help` | Shows how functions the command | Muestra cómo funciona el comando |


### Others / Otros

| Command | Description | Descripción |
| ------------------------ | ----------- | ----------- |
| `alias [name=] "command"` | Create a shorcut for a command | Crea un alias para llamar a un comando |
| `git grep -n [word]` | |Search words in the proyect | Busca la palabra especificada en todo el proyecto |
| ​🌏​🌲​🌳​💻​`git stash` |  |  |
| `git stash` | Stash changes in a dirty working directory | Es un limbo como el staging area. Te permite cambiar de branch sin hacer commit |
| `git stash list`| | Ver la lista de los stash |
| `git stash pop`| | Aplica el ultimo stash a la rama actual |
| `git stash branch [brach]`| | Mueve el stash al [branch]|
| `git stash drop stash@{numero}`| | Elimina el stash |
| `git stash apply stash@{numero}`| | Aplica el stash |
| `git stash clear` | Remove all stashed entries ||
| ​🌏​🌲​🌳​💻​`git cherry` |  |  |
| `git cherry pick [sha1]` | Move commit from another branch to active branch | Mover el commit [sha1] de otro branch al branch actual |

## Interesting Links / Enlaces Interesantes

| Command |
| ------------------------ | 
| Si quieres un mes adicional en tu suscripcion DE PLATZI, accesa aquí: https://platzi.com/r/sandynolasco |
| https://marklodato.github.io/visual-git-guide/index-es.html |
| https://diego.com.es/ramas-y-uniones-en-git |
| https://sourcelevel.io/blog/how-to-properly-mirror-a-git-repository |
| http://rogerdudler.github.io/git-guide/index.es.html |
| https://pandao.github.io/editor.md/en.html#Features |
| https://git-scm.com/ |
| https://platzi.com/cursos/git-github/ |
| Apuntes a detalle del curso de Platzi: https://wise-diagram-6de.notion.site/Curso-Profesional-de-Git-y-GitHub-c693f9c2bc2345eab096c0bc23001d01 |


## Errors / Errores (Github)

Secuencia de error:
git init
git add file1.csv
git commit -m "First commit"
git remote add origin <Github url from Quick Setup page>
git push -u origin main
And I got the following errors:
error: src refspec main does not match any
error: failed to push some refs to <url>|

Solucion:

Solution A - if you want to name the branch master
Run git push -u origin master instead of git push -u origin main

Or Solution B - if you want to name the branch main
Run git checkout -B main before git push -u origin main

Otros:
git remote add origin git@github.com:Sandynolasco/Git-Basic-Commands.git
git push --mirror https://github.com/Sandynolasco/Git-Basic-Commands.git
git push -f origin master:main : Which master is my local branch and main is my remote branch. I think this happened because Github renamed master to main.


*Comandos para trabajar en Git y GitHub*
