**¿Qué comando utilizaste para el paso 11?¿Por qué?**

*Comando: git reset HEAD~1*

Al deshacer el último commit se va al commit padre del actual, esto lo hacemos con git reset HEAD~1, y al descartar los cambios que hemos realizado, hay que usar la opción --hard.

**¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?**

*Comando: git reset --hard HEAD@{1}* 
Porque al rehacer el commit, vamos al hijo del commit actual.

**El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?**

No causa ningún conflicto ya que la rama styled procede de la rama master, por lo tanto, styled incluye el trabajo de master por lo que devuelve Already up-to-date.

**El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?**

Causó conflicto, el commit al que apunta styled y el commit al que apunta htmlify son hijos del mismo commit, aparte que estos commits han modificado las mismas líneas del mismo archivo, y git no
sabe cual es el resultado que queremos mantener, por tanto, no puede hacer merge de la ramas. 

**El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?**

Sin conflicto, es un merge fast-forward, lo que hay que hacer es mover el puntero de la rama master al commit al que apunta la rama styled.

**¿Qué comando o comandos utilizaste en el paso 25?**

*Comandos: git config --global alias.graph "log --decorate --graph"
git graph*

El primer comando para crear un alias para el grafo, y el segundo para ejecutarlo. Las opciones --decorate sería para verlo con colores,etiquetas y ramas. La opción --graph para mostrar el árbol de commits.

**El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?**

Sí, porque master es el padre de title, están en la misma línea. Todo el trabajo de master está reflejado en la rama title.

**¿Qué comando o comandos utilizaste en el paso 27?**

*Comando: git reset HEAD~1*

No he utilizado la opción --hard para no perder los cambios en el working copy.

**¿Qué comando o comandos utilizaste en el paso 28?**

*Comando: git reset --hard HEAD*

Estoy en el commit que quiero, lo que hago es restaurar el working copy como estaba en el commit actual. 

**¿Qué comando o comandos utilizaste en el paso 29?**

*Comando: git branch -d title* 


**¿Qué comando o comandos utilizaste en el paso 30?**

*Comandos: git reflog y git reset --hard b7ee1e0* 

El primer comando para encontrar el commit donde hago el merge de master con title, y con el segundo comando accedo al commit dejando el working copy en el estado en el que estaba.

**¿Qué comando o comandos usaste en el paso 32?**

*Comandos: git log y git reset --hard fc12f246de71a2e5701ff3bc5c86ffa90a8b54d3* 

El primero lo uso para ver el listado de commits de master, y así puedo localizar el commit inicial, y el segundo es para moverme hasta donde está situado. Uso la opción --hard para dejar el working copy como estaba cuando se realizó el commit inicial.

**¿Qué comando o comandos usaste en el punto 33?**

*Comandos: git reflog git reset --hard c2c9d95*

El primero para el seguimiento de pasos hasta llegar al commit actual, y localizar el commit al que voy a moverme. Y el segundo para moverme a dicho paso, y dejando el working copy tal cual estaba.