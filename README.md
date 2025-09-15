# DespliegueDeAplicaciones

Transacciones.  Proceso que ocurre todo de golpe, en la misma operación (si falla se hace rollback):
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
git diff Muestra cambios sin confirmar
git branch Lista las ramas
git checkout <rama> Cambia de rama
git checkout -b <nueva> Crea y cambia a una nueva rama
git merge <rama> Fusiona rama en la actual
git pull Actualiza con cambios del remoto
git push Envía commits locales al remoto
git remote -v Muestra los remotos configurados
