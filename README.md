# Git-Basic-Commands
Práctica de Curso Profesional de Git y GitHub


# Let's begin

![Begin](https://user-images.githubusercontent.com/58926113/178091091-a7eecc5a-fcc4-422b-9fc9-611fc7e52382.gif)

![](https://sandynolasco.github.io/Sandynolasco/imgall/blob/main/Begin.gif)

![](https://img.shields.io/github/issues/Sandynolasco/Git-Basic-Commands) ![](https://img.shields.io/github/forks/Sandynolasco/Git-Basic-Commands) ![](https://img.shields.io/github/stars/Sandynolasco/Git-Basic-Commands) 
![](https://github.com/Sandynolasco/Git-Basic-Commands/issues/2#issue-1301125192)


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
### Quotes

> "Today is still, yesterday never again"



### Terminal Commands / Comandos de la Terminal

| Command | Description | Descripción |
| ------------------------ | ----------- | ----------- |
| `cd [directoryrute]` | To change directory | Cambia el directorio |
| `mkdir [carpetname]` | Make directory | Crea una nueva carpeta |
| `ls -al` | List information about the files a [hide files]| Lista los archivos del directorio, incluye archivos ocultos |
| `clear` | Clear the terminal screen | Limpia la Terminal |
| `touch [Name file]` | Create a empty file | Crea un archivo vacio |
| `rm [Name file]` | Remove files | Elimina un archivo |
| `pwd` | Print name of current/working directory | Muestra el directorio donde nos encontramos |
| `mv` | Move (rename) files | Mueve o renombra archivos |
| `cat [Name file]` | Concatenate files and print on the standard output | Vista previa del contenido del archivo |
| `sudo` | Execute a command as another user | Ejecuta un commando como administrador |
| `history` |  Last commands entered| Ultimos comandos ingresados |
| `Guardar y salir de vi` || Esc pausa y ingresar shif + z + z [para guardar y salir de “vi”] |
| `Escribir en vi` || Space + i [para poder empezar a escribir en “vi”] |
| `rm -rf [repo.git]` | Remove the temporary local repository | Elimina un repositorio local ó |
| `rm -f -r ~/Projects/MyProject.git` | | Eliminará un repositorio Git de línea de comandos completo |


### Config Git / Configuración de Git

| Command | Description | Descripción |
| ------------------------ | ----------- | ----------- |
| `git config --global user.name "name-example"` | Add a user name | Añade un nombre de usuario |
| `git config --global user.email user@example.com` | Add a email for user | Añade un correo del usuario |
| `git config --list` | List all setings | Muestra todas las configuraciones  |
| `git config --global color.ui true` | Configure text editor | Configurar el editor del texto |


### Config SSH Keys / Configuración de Credenciales SSH

| Command | Description | Descripción |
| ------------------------ | ----------- | ----------- |
| `ssh-keygen -t rsa -b 4096 -C "Email"` | Generate SSH key | Generar credencial SSH |
| `eval $(ssh-agent -s)` | Verify ssh agent | Verifica la existencia del servidor de credenciales SSH |
| `ssh-add ~/.ssh/id_rsa` | Add SSH key to your workspace | Agrega la credencial SSH al entorno de trabajo |
| `ssh-keygen -t rsa -b 4096 -C "correo@ejemploc.com"` | Generate an SSH key. The email must be the same as the one found on Github | Crea una llave SSH. El correo debe de ser el mismo que se encuentra en Github |
| `ls -al ~/.ssh` | Verifies if SHH key exists | Verifica si hay claves SSH presentes. Comprueba la lista de directorio para ver si ya tiene una clave SSH pública. 
Predeterminadamente, los nombres de archivo de las llaves públicas compatibles para GitHub son una de las siguientes: id_rsa.pub id_ecdsa.pub id_ed25519.pub |
| `ls -al ~/.ssh` | Verify if exist keys SSH | ¿Cómo verificar si ya existen llaves SSH? |




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
| `git status` | Check status repository | Verifica el estatus del repositorio. `untracked files` son archivos que están en nuestro Working Directory, lo que aparezca en rojo es lo que se ha modificado y hay que pasarlo al Staging. `changes to be comitted` son los archivos que se encuentran en el staging area, aparecen en verde. Se puede ver el tipo de rama: on branch master, commits, rastreo o procesamiento de filas:untracked files |
| ​🌏​🌲​🌳​💻​`git add`|  |  |
| `git add [Name file]` | Add a file to the staging area | Añade un archivo al area de preparación |
| `git add .` | Add all new and changed files to the staging area | Añade todos los archivos al area de preparación |
| `git add -A` | Add all files to the staging area. It's the same that add . | Añade todos los archivos al area de preparación. = add |
| `git add - n [Name file]` | Simulating add a file | Simula el agregado de un [archivo] |
| ​🌏​🌲​🌳​💻​`git commit`|  |  |
| `git commit -m "[commit message]"` | Add changes from stagging area to repository | Añade los archivos del área de stagging al repositorio |
| `git commit -a "[commit message]"` | The command to automatically stage files that have been modified and deleted, but new files you have not told Git about are not affected | El comando para organizar automáticamente los archivos que se han modificado y eliminado, pero los archivos nuevos que no le has dicho a Git no se ven afectados |
| `git commit -am "[commit message]"` | Add files from stagging area to repository and commit | Añande los cambios del stagging area al repositorio y hace commit |
| `git commit -- amend --no-edit "[commit message]"` | Add changed files at the earlier commit, you have modified some files that you want to commit in a singular snapshot, but you have forgotten to add one of the files the first time around, Add --no-edit flag to modify your commit without changing the commit message. As a result, the wrong commit will be replaced by the right one | Añade los cambios al anterior commit. Si se escribe un mensaje este sobreescribe el anterior.|
| ​🌏​🌲​🌳​💻​`git rm`|  |  |
| `git rm -r [Name file]` | Remove a file (or folder)... | Elimina archivos o carpetas del área de stagging sin eliminar el historial del sistema de versiones|
| `git rm --cached [Name file]` | Removes files or folders from the staging area and from the next commit, but keeps them on the hard drive | Elimina archivos o carpetas del área de stagging y del proximo commit, pero los mantiene en disco duro |
| `git rm -force ` | Delete files from git and hard drive |  Elimina los archivos del git y del disco duro |
| ​🌏​🌲​🌳​💻​`git reset`|  It allows you to go back in time without being able to go back to the future | Permite volver en el tiempo sin poder volver al futuro |
| `git reset -soft [sha1]` | We delete all Git history and logs but keep any changes we have in Staging, so we can apply the latest updates to a new commit. --- The history is deleted but the files of the stagging area are kept to be able to apply changes to the last commit | Borramos todo el historial y los registros de Git pero guardamos los cambios que tengamos en Staging, así podemos aplicar las últimas actualizaciones a un nuevo commit. --- Se borra el historial pero se mantiene los archivos del area de stagging para poder apolicar cambios al ultimo commit |
| `git reset -mixed [sha1]` | Delete all the information from the staging area and from the commits | Borra toda la información del área de stagging y de los commits |
| `git reset -hard [sha1]` | Delete all the changes even from the working directory go back to the commit [SHA-1] Where the SHA-1 is the commit identifier --- Delete all the information from the staging area and from the commits | Elimina todos los cambios incluso del working directory  regresa hasta el commit del [SHA-1] Donde el SHA-1 es el identificador del commit --- Borra toda la infromacion del area de stagging y de los commits |
| `git reset -HEAD` | Move changes from Stagging to Unstaged. The latest changes are kept, the repository still has the file only with the changes made in commit. This command does not remove any files or delete commits from git. In short: This is the command to get files out of the staging area. Not to delete them or anything, just so that the latest changes to these files don't get pushed to the last commit, unless we change our mind and staging them back with git add of course | Mueve cambios de Stagging a Unstaged. Se conservan los ultimos cambios, el repositorio sigue teniendo el archivo solo con los cambios hechos en commit. Este comando no elimina ningún archivo ni borra commits del git. En resumen: Este es el comando para sacar archivos del área de staging. No para borrarlos ni nada de eso, solo para que los últimos cambios de estos archivos no se envíen al último commit, a menos que cambiemos de opinión y los incluyamos de nuevo en staging con git add, por supuesto |


### Branching & Merging / Ramas y Fusionar

| Command | Description | Descripción |
| ------------------------ | ----------- | ----------- |
| ​🌏​🌲​🌳​💻​`git branch` |  |  |
| `git branch ` | List branches (the asterisk denotes the current branch) | Lista todas las ramas locales |
| `git branch [branch name]` | Create a new branch | Crea una nueva rama [branch name] |
| `git branch -l`| List all branches| lista las ramas |
| `git branch -r` | Show all remote branches | Muestra todas las ramas remotas |
| `git branch -a` | Show all branches both local and remote | Muestra todas las ramas tanto locales como remotas |
| `git branch -d [branch name]`| Delete a branch| Elimina el branch [nombre]. Esto solo funciona si el branch no tiene ningún commit |
| `git branch -D [branch name]`| Force deletion of a branch regardless of whether it has commits | Fuerza la eliminación de una rama sin importar si tiene commits |
| `git branch -m [branch name inicial] [branch name nuevo]` | Rename branch [initial name] to [new name] | Renombra el branch [nombre inicial] por [nuevo nombre] |
| ​🌏​🌲​🌳​💻​`git show` |  |  |
| `git show-branch --all` | List all branches local | Lista todas las ramas en local |
| ​🌏​🌲​🌳​💻​`git checkout` |  |  |
| `git checkout ` | Bring changes made | Trae cambios realizados git checkout opera sobre tres entidades distintas: archivos, confirmaciones y ramas |
| `git checkout [branch name]` | Switch to the branch last checked out | Te permite desplazarte entre las ramas creadas por git branch |
| `git checkout -b [branch name] origin/[branch name]` | Clone a remote branch and switch to it | Clona una rama remota y cambia a ella |
| `git checkout -b [branch name]` | Create a new branch and switch to it | Crea una rama y hace checkout y cambia a ella directamente |
| `git checkout -- [Name file]` | Discard changes to a file | Descarta los cambios de un archivo |
| `git checkout [sha1]`| Go to the point in time of that commit without deleting subsequent changes to the selected tag |  Ir al momento del tiempo de ese commit sin borrar los cambios posteriores al tag seleccionado |
| `git chechout [sha1] [archivo]` | Go to the moment in time of that commit of a specific file |  Ir al momento del tiempo de ese commit de un archivo específico |
| ​🌏​🌲​🌳​💻​ `git merge` |  |  |
| `git merge [source branch] [target branch]` | Merge a branch into a target branch | Fusiona una rama a una rama determinada |
| `git merge [branch 
name]` | Mixed the branch wit actual |mezcla el branch [branch] con el branch actual |
| ​🌏​🌲​🌳​💻​ others |  |
| `git rebase [branch name]`| Merge the [branch] with the current branch. It's like merge but without creating forks. To make it work well, first rebase the branch with the Changes we want to modify and then rebase the final branch, write the history of the repository, change the history of where the branch started and should only be used locally. | Mezcla el [branch] con el branch actual. Es como el merge pero sin crear bifurcaciones. Para que funcione bien, primero se hace rebase a la rama con losCambios que queremos modificar y luego rebase a la rama final , eescribe la historia del repositorio, cambia la historia de donde comenzó la rama y solo debe ser usado de manera local. |
| ​🌏​🌲​🌳​💻​ `git clean` |  |
| `git clean`| Delete files that are not under version control. For it to work you need to use one of the flags: | Elimina los archivos que no están bajo el control de versión. Para que funcione es necesario usar alguno de los flags:|
| `git clean n`| It does not remove anything, it only shows you the files that it is going to delete | No remueve nada, solo te muestra los archivos que va a eliminar |
| `git clean f`| Delete the files that are not versioned | Elimina los archivos que no se encuentran versionados |


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
| `git push [origin] [master]` | Push to local repository to remote | Envia al repositorio local al remoto |
| `git push --all origin` | Push to all branches and tags | Push a todos los branch y tags |
| `git push --u rama main` | Push to all branches | Push a todos los branch |
| `git push --mirror [url]` | This will get all the branches and tags that are available in the upstream repository and will replicate those into the new location. Warning: Don’t use git push --mirror in repositories that weren’t cloned by --mirror as well. It’ll overwrite the remote repository with your local references (and your local branches). This is not what we want. Read the next section to discover what to do in these cases. Also git clone --mirror is preferred over git clone --bare because the former also clones git notes and some other attributes |  |
| ​🌏​🌲​🌳​💻​`git fetch` |  |  |
| `git fetch [nombre] [branch name]` | He only brings them but he doesn't mix it | Solo los trae pero no lo mezcla |
| ​🌏​🌲​🌳​💻​`git merge` |  |  |
| `git merge [origin/master] --allow-unrelated-histories` | Merge the fetch with the local repository, fetch the version from the remote repository, and merge to create a commit with the files from both parties | Hace un merge del fetch con el repositorio local, traer la versión del repositorio remoto y hacer merge para crear un commit con los archivos de ambas partes |
| ​🌏​🌲​🌳​💻​`git pull` |  |  |
| `git pull [origin] [master]` | Do a feth and merge, do git fetch + git merge, fetch whatever is on the web, push local repository to remote | Hace un feth y fusiona, hace git fetch + git merge, me trae lo que haya en la web, envia el repositorio local al remoto |
| `git pull --all origin` | Push to all branches and tags | Push a todos los branch y tags |


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
| `git show [tag]` | Shows the latest changes that have been made to the commit | Muestra los últimos cambios que se han hecho en el commit |


### Collaborative Commands / Comandos Colaborativos

| Command | Description | Descripción |
| ------------------------ | ----------- | ----------- |
| ​🌏​🌲​🌳​💻​`git shortlog` |  |  |
| `git shortlog -sn`| Shows how many commits each team member has made | Muestra cuantos commit han hecho cada miembros del equipo |
| `git shortlog -sn --all`| Shows how many commits each team member has made up to those that have been removed | Muestra cuantos commit han hecho cada miembros del equipo hasta los que han sido eliminado |
| `git shortlog -sn --all --no-merge`| Shows how many commits each member has made removing the deleted ones without the merges | Muestra cuantos commit han hecho cada miembros quitando los eliminados sin los merges |
| ​🌏​🌲​🌳​💻​`git blame` |  |  |
| `git blame [archivo]`|  Show who did what line by line | Muestra quien hizo cada cosa línea por línea |
| `git blame [archivo] -L[línea_inicial],[línea_final]`| It shows who did what line by line by telling you which line to watch from. Example `L35.50|` | Muestra quién hizo cada cosa línea por línea indicándole desde qué línea ver. Ejemplo `L35,50|`
| `git [comando] --help` | Shows how functions the command | Muestra cómo funciona el comando |

### Others / Otros

| Command | Description | Descripción |
| ------------------------ | ----------- | ----------- |
| `alias [name=] "command"` | Create a shorcut for a command | Crea un alias para llamar a un comando |
| `git grep -n [word]` | Search words in the proyect | Busca la palabra especificada en todo el proyecto |  |
| `git reflog` | Git saves all the changes even if you decide to delete them, when you delete a change what you are doing is only updating the tip of the branch, to manage these tips there is a mechanism called reference records or reflogs | Git guarda todos los cambios aunque decidas borrarlos, al borrar un cambio lo que estás haciendo sólo es actualizar la punta del branch, para gestionar éstas puntas existe un mecanismo llamado registros de referencia o reflogs |
| ​🌏​🌲​🌳​💻​`git stash` |  |  |
| `git stash` | Stash changes in a dirty working directory | Es un limbo como el staging area. Te permite cambiar de branch sin hacer commit |
| `git stash list`| See the list of stash | Ver la lista de los stash |
| `git stash pop`| Apply the latest stash to the current branch | Aplica el ultimo stash a la rama actual |
| `git stash branch [brach]`| Move the stash to the [branch] | Mueve el stash al [branch] |
| `git stash drop stash@{numero}`| Remove the stash | Elimina el stash |
| `git stash apply stash@{numero}`| Apply the stash | Aplica el stash |
| `git stash clear` | Remove all stashed entries | Remove all stashed entries |
| ​🌏​🌲​🌳​💻​`git cherry` |  |  |
| `git cherry pick [sha1]` | Move commit from another branch to active branch | Mover el commit [sha1] de otro branch al branch actual, Es un comando que permite tomar uno o varios commits de otra rama sin tener que hacer un merge completo |


## Interesting Links / Enlaces Interesantes

| Command |
| ------------------------ | 
| Si quieres un mes adicional en tu suscripcion DE PLATZI, accesa aquí: https://platzi.com/r/sandynolasco |
| https://www.w3docs.com/learn-git/git-commit-amend.html |
| https://marklodato.github.io/visual-git-guide/index-es.html |
| https://diego.com.es/ramas-y-uniones-en-git |
| https://sourcelevel.io/blog/how-to-properly-mirror-a-git-repository |
| http://rogerdudler.github.io/git-guide/index.es.html |
| https://pandao.github.io/editor.md/en.html#Features |
| https://git-scm.com/ |
| https://platzi.com/cursos/git-github/ |
| Apuntes a detalle del curso de Platzi: https://wise-diagram-6de.notion.site/Curso-Profesional-de-Git-y-GitHub-c693f9c2bc2345eab096c0bc23001d01 |
| https://learngitbranching.js.org/?NODEMO=&locale=es_ES |

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
