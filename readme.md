# Módulo 1: git, gitHub, SourceTree

## Ejercicio 1

**¿Qué comando utilizaste en el paso 11?** - *Deshacer el último commit (perdiendo los cambios realizados en el working copy)*

`git reset --hard HEAD~1`

**¿Por qué?**

El comando que se usa para movernos entre commits es `git reset`. El modificador `--hard` lo usarmos para deshacer el working copy. El otro modificador usado, `HEAD~1` lo usamos para indicar que queremos deshacer solo un commit.

-------
**¿Qué comando o comandos utilizaste en el paso 12?** - *Rehacer el último commit (el que acabamos de deshacer)*

`git reset --hard ff33f01e0800c3b756898c77adeb4430be9289b0`

**¿Por qué?**

Una vez más usamos `git reset` movernos entre commits. El valor hexadecimal el número de commit al que nos queremos mover.

-------
**El merge del paso 13, ¿Causó algún conflicto?** - *Hacer un merge con ‘master’ (styled absorbe a master)*

No

**¿Por qué?**

Al crear la rama styled, tanto master como styled son iguales (tienen los mismos nodos). Posteriormente hemos hecho commits en la rama styled (añadiendo nuevos nodos) pero al hacer el merge de master en styled no hay nodos nuevos en master que añadir a styled.

-------
**El merge del paso 19, ¿Causó algún conflicto?** - *Hacer un merge de “htmlify” en “styled” (styled absorbe a htmlify)*

Sí

**¿Por qué?**

Tanto styled como htmlify parten del mismo nodo de master. A partir y en las dos ramas se han hecho modificaciones del mismo fichero. Al mezclar htmlify en styled incorporamos los útlimos cambios en styled por lo que hay que decidir con que cambios nos quedamos.

-------
**El merge del paso 21, ¿Causó algún conflicto?** - *Desde “master”, hacer un merge con “styled”*

No

**¿Por qué?**

Desde que la rama styled se creo no han habido modificaciones en la rama master, por lo que la rama master absorve todos los cambios que hay en styled sin problemas/conflictos.

-------
**¿Qué comando o comandos utilizaste en el paso 25?** - *Dibujar el diagrama*

`git log --graph --decorat`

**El merge del paso 26, ¿Podría ser fast forward?** - *Hacer un merge “no fast-forward” de “title” en “master” (master absorbe a title)*

Si

**¿Por qué?**

La rama master no ha sido modificada después de crear la rama title y de realizar en ella cambios.

-------
**¿Qué comando o comandos utilizaste en el paso 27?** - *Deshacer el merge (sin perder los cambios del working copy)*

`git reset 06b1e78`

-------
**¿Qué comando o comandos utilizaste en el paso 28?** - *Descartar los cambios*

`git stash`

-------
**¿Qué comando o comandos utilizaste en el paso 29?** - *Eliminar la rama “title”*

`git branch -D title`

-------
**¿Qué comando o comandos utilizaste en el paso 30?** - *Rehacer el merge que hemos deshecho*

`git reset a93819d`

-------
**¿Qué comando o comandos usaste en el paso 32?** - *Volver al commit inicial cuando se creó el poema*

`git reset --hard 392968b`

-------
**¿Qué comando o comandos usaste en el punto 33?** - *Volver al estado final, cuando pusimos título al poema*

`git reset --hard 06b1e78`