## Comandos GIT
* Para conocer la versión de GIT instalada

```batch
git --version
```
<br>

* Para la ayuda

```batch
git help
```
<br>

* Para cambiar el nombre de usuario de la variable global

```batch
git config --global user.name "José Antonio Cabrera"
```
<br>

* Para cambiar el email de la variable global

```batch
git config --global user.email "joseantoniocabreraalarcon@gmail.com"
```
<br>

* Para visualizar el fichero de configuración global

```batch
git config --global -e
```
<br>

* Para inicializar el repositorio

```batch
git init
```
<br>

* Para obtener el estado actual de la rama

```batch
git status
```
<br>

* Para añadir un fichero al stage

```batch
git add <nombre_fichero>
```
<br>

* Para añadir todos los ficheros al stage

```batch
git add .
```
<br>

* Para solventar el problema de los saltos de línea

```batch
git config core.autocrlf true
```
<br>

* Para quitar un fichero del stage

```batch
git reset <nombre_fichero>
```
<br>

* Para realizar un commit

```batch
git commit -m "<mensaje_del_comit>"
```
<br>

* Recuperar el estado del último commit

```batch
git checkout -- .
```
<br>
* Devuelve el nombre de las ramas y marca con asterisco la actual

```batch
git branch
```
<br>

* Cambiar nombre de la rama

```batch
git branch -m <nombre_actual> <nombre_nuevo>
```
<br>

* Para cambiar el nombre de la rama creada en la inicialización

```batch
git config --global init.defaultBranch <nombre_rama_inicial>
```
<br>

* Para añadir al stage y hacer un commit. (Sólo los ficheros que ya tienen seguimiento)

```batch
git commit -am "<mensaje_del_comit>"
```
<br>

* Para ver los logs del repositorios.

```batch
git log
```
<br>

* Crear alias

```batch
git config --global alias.<alias> "<comando_sin_git>"
```
<br>

* Cambiar el texto del último commit

```batch
git commit --amend -m "<nuevo_mensaje_del_comit>"
```
<br>

* quitar el comit n antes del HEAD/hashcommit indicado manteniendo los cambios (--soft).

```batch
git reset --soft HEAD^<n>
```
<br>

* Volver al estado del commit indicado por el hash manteniendo los cambios posteriores en los archivos.
```batch
git reset --mixed <hash>
```
<br>

* Volver al estado del commit indicado por el hash destruyendo los cambios posteriores.
```batch
git reset --hard <hash>
```
<br>

* Para ver el historial de cambios (incluso los reset realizados)

```batch
git reflog
```
<br>

* Mover archivo de la ruta A a la B

```batch
git mv <pathA> <pathB>
```
<br>

* Renombrar archivo

```batch
git mv <nombre_old> <nombre_new>
```
<br>

* Borrar un archivo

```batch
git rm <nombre_Archivo>
```
<br>

* Crear una rama nueva

```batch
git branch <nombre_rama_nueva>
```
<br>

* Moverse a una rama

```batch
git checkout <nombre_rama>
```
<br>

* Trae todos los cambios nuevos de la rama <nombre_rama> a la rama actual.

```batch
git merge <nombre_rama>
```
<br>

* Eliminar una rama 

```batch
git branch -d <nombre_rama_nueva>
```
<br>

* Fuerza la eliminación de una rama cuando tiene cambios sin commit.

```batch
git branch -d <nombre_rama_nueva> -f
```
<br>

* Para crear una rama y momverse a ella con un solo comando

```batch
git checkout -b <nombre_rama_nueva>
```
<br>

* Crear tag

```batch
git tag <nombre_tag>
```
<br>

* Ver todos los tags

```batch
git tag
```
<br>

* Borrar tags

```batch
git tag -d <nombre_tag>
```
<br>

* Crea tag con número de versión

```batch
git tag -a v1.0.0 <hash> -m "Version 1.0.0 lista"
```
<br>

* Mostrar más información de una etiqueta

```batch
git show <tag>
```
<br>

* Crear un stash

```batch
git stash
```
<br>

* Listar los stash

```batch
git stash list
```
<br>

* Recuperar el último stash

```batch
git stash pop
```
<br>

* Borrar todos los stash

```batch
git stash clear
```
<br>

* Recuperar un stash en concreto

```batch
git stash apply 2
```
<br>

* Borrar una entrada de stash

```batch
git stash drop 0
```
<br>

* Crear un stash con etiqueta

```batch
git stash save "<etiqueta>" 
```
<br>

* Listar stash con más información

```batch
git stash list --stat
```
<br>

* Para hacer el rabse de una rama desde la que me encuentro

```batch
git rebase <rama>
```
<br>

* Rebase interactivo de los últimos 4 commit

```batch
git rebase -i HEAD~4
```
<br>

* Eliminar los cambios hechos después del último commit del archivo

```batch
git checkout -- <nombre_archivo>
```
<br>

* Para continuar con un rebase cuando entra en proceso manual

```batch
git rebase --continue
```
<br>

* Subir los tags al origen remoto

```batch
git push --tags
```
<br>

* Traer los datos desde el origen

```batch
git pull
```
<br>

* PAra ver el path del repositorio

```batch
git remote -v
```
<br>

* PAra configurar la estrategia del pull a fast-foward only

```batch
git config --global pull.ff only
```
<br>

* Abortar rebase interactivo

```batch
git rebase --abort
```
<br>

* Para actualizar las referencias

```batch
git fetch
```
<br>

* PAra descargar las ramas de otras personas.

```batch
git pull --all
```
<br>

* Ver todas las ramas locales y del repositorio

```batch
git branch -a
```
<br>

* Eliminmar ramas que no existan en el repositorio.

```batch
remote prune origin
```
<br>

* Actrualizar rama origen (incluso borrado)

```batch
git push origin :<nombre_rama>
```
<br>

* Hace un commit que github interpreta y cierra el issue #5

```batch
git commit -am "Fixes #5: <comentario>"