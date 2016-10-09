

- **¿Qué comando utilizaste en el paso 11? ¿Por qué?**

git reset --hard HEAD~1

Porque si queremos perder los cambios del working copy, tenemos que hacer el reset con —hard

- **¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?**

Primero utilicé un “git reflog” para ver en qué punto había realizado el paso anterior (el anterior, obvio…), y para ver la referencia:
bash-3.2$ git reflog
e13303b HEAD@{0}: reset: moving to HEAD~1
99e3c27 HEAD@{1}: commit: Añadimos el archivo git-nuestro.md modificado-PUNTO 10
e13303b HEAD@{2}: checkout: moving from master to styled
e13303b HEAD@{3}: commit (initial): Añadimos git-nuestro.md al repositorio

Segundo, tomando la referencia del paso al que debo volver, utilizo:
git reset --hard 99e3c27

- **El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?** 

El merge no causó ningún conflicto. No debía causarlo, pues el fichero era el mismo.

- **El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?** 

Este sí que causó un conflicto, porque los ficheros de ambas ramas eran diferentes.

- **El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?** 

No causó ningún conflicto.

- **¿Qué comando o comandos utilizaste en el paso 25?**

git log --graph --decorate

- **El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?** 

Podríamos haberlo hecho, y haber incorporado igualmente los cambios realizados al archivo git-nuestro.md. No habríamos perdido nada.

- **¿Qué comando o comandos utilizaste en el paso 27?** 

git reset 6b3f76c	

- **¿Qué comando o comandos utilizaste en el paso 28?** 

*1) Volvemos al merge, primero un “git reflog” y luego un “git reset”:*
bash-3.2$ git reflog


git reset d9a57b0

*2) Deshacemos el merge pero esta vez descartando los cambios:*
git reset --hard 6b3f76c
HEAD is now at 6b3f76c Volvemos a hacer commit de git-nuestro.md - PUNTO 26

- **¿Qué comando o comandos utilizaste en el paso 29?** 

git branch -D title
git branch -D title
Deleted branch title (was f61f625).

- **¿Qué comando o comandos utilizaste en el paso 30?** 

git reset --hard d9a57b0
HEAD is now at d9a57b0 Merge branch 'title'

- **¿Qué comando o comandos usaste en el paso 32?** 

bash-3.2$ git reflog

bash-3.2$ git reset --hard e13303b
HEAD is now at e13303b Añadimos git-nuestro.md al repositorio

- **¿Qué comando o comandos usaste en el punto 33?** 

bash-3.2$ git reflog
 
bash-3.2$ git reset --hard f61f625
HEAD is now at f61f625 Añadimos título a git-nuestro.md - PUNTO 23
