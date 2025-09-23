# DespliegueDeAplicaciones

Transacciones. Proceso que ocurre todo de golpe, en la misma operación (si falla se hace rollback):
Son trasacciones atómicas
Commit --> Afirmación de que queremos subir el codigo/cambios. Confirmar todos los cambios
Rollback --> Cuando falla una transacción, volver todo al paso anterior del inicio de la operación.

Repositorio --> Contenedor de carpetas, donde es posible compartir y trabajar en grupo con más gente, existen roles que afectan a la modificación, etc...

<<<Comandos>>> (Entra examen)
git init Inicializa un nuevo repositorio

Vamos a la carpeta y cambiamos para ver elementos ocultos

git clone <url> Clona un repositorio remoto
git status Muestra estado de los archivos
git add <archivo> Añade archivo al área de preparación
git commit -m "mensaje" Crea un commit con mensaje
git log --oneline Historial de commits breve
git diff Muestra cambios sin confirmar entre commits
git branch Lista las ramas
git checkout <rama> Cambia de rama
git checkout -b <nueva> Crea y cambia a una nueva rama
git merge <rama> Fusiona rama en la actual
git pull Actualiza con cambios del remoto
git push Envía commits locales al remoto
git remote -v Muestra los remotos configurados
git rm Elimina archivos

Como la maquina gestiona los estados en los que puede estar un fichero: (vista maquina)

directorio local de archivos en disco duro --> Working directory
fotografia de lo que tiene el proximo commit, lo que qued acuando le damos a add --> staging area(index ó cached
esta almacenado en el repositorio local--> localrepo

vista Git:

untracked --> existen en el area de trabajo pero no para git
staged --> Cambios confirmados añadidos en el siguiente commit
commited --> Archivos guardados en el ultimo commit y que no se han modificado desde entonces
modified --> Cambios no rastreados por el commit, se han modificado desde el último commit

git rm --> usa el modificador --cached para referirse a la staged area
git restore --> usa el modificador --staged ara referirse a la staged area
git diff --> usa el modificador --cached o --staged ara referirse a la staged area

# Hacer esquema de la pagina 1 del pdf que tiene 8 que explica como mueve los estados

rama master es donde se guarda cuando hacemos un commit
rama origin/master es el repositorio remoto
git fech copia lo que hay en un repositorio remoto a una rama local


Usando git status -s
La M verde en el primer espacio es modified en staged
La M rojo en el segundo espacio es modified en el workspace
La MM(verde y roja) quiere decir que hay un cambio en staged listo para subir y que otro cambio esta en el workspace

# Borrado de commits

Cuando se borra un commit simplemente accedemos al commit anterior

git reset --hard hash --> Vuelve al commit anterior borrando todos los posteriores pero modificando el área de trabajo al dejar ahi los ficheros del commit y vacia el staged area

git reset --soft hash --> Vuelve al commit anterior borrando todos los posteriores pero no modifica el área de trabajo y no modifica el staged area

git reset --mixed hash --> Vuelve al commit anterior borrando todos los posteriores pero no modifica el área de trabajo y vacia el staged area

git reset --soft HEAD-1 --> Vuelve al penultimo commit sin modificar staged ni el area de trabajo

Una vez subido un commit a GitHub es mala practica borrar un commit pero en caso de hacer algo se puede usar __git revert HEAD-1__ --> Crea un commit que revierte los ultimos cambios, el anterior commit sigue existiendo pero no se borra, simplemente es un commit que deshace ese trabajo.

La opcion --no commit en un git revert --no-commit HEAD-1 nos permite ver que cambia, para decidir que hacer.

Si no estamos de acuerdo podemos usar git restore --worktree --staged fichero

En caso de conflicto se soluciona en el fichero