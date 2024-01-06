PREGUNTA: 
Qué comando utilice en el paso 11?  Por qué ?

git reset --hard HEAD~1

Porque este comando permite realizar dos funciones: revertir el commit y regresar al punto como estaba mi working copy con anterioridad al commit

PREGUNTA: 
Qué comando o comandos utilice en el paso 12?  Por qué ?

git reflog

git reset --hard 602bb39

Usé git reflog para buscar el identificador del commit que tenía que rehacer y luego con usé git reset --hard (más el identificador de tal commit) para rehacer nuevamente el commit, más el working copy.

PREGUNTA:
El merge del paso 13 causó algún conflicto ?  NO. Por qué ?

Entiendo que no hubo conflictos, porque los cambios realizados en el archivo git-nuestro.md fueron exclusivos de la rama styled y no se realizaron cambios en la mismas líneas de ese archivo en la rama main.

PREGUNTA:
En el merge del paso 19, causó algún conflicto ? Sí.  Por qué ?

Entiendo que hubo conflictos porque se produjeron cambios con diferentes contenidos en el archivo git-nuestro-md en ambas ramas, en líneas que coincidían.

PREGUNTA:
En el merge del paso 21, causó algún conflicto ? NO.  Por qué ?

Porque en el archivo git-nuestro.md, entre esas dos ramas, en lass misma líneas no tengo diferente contenidos.

PREGUNTA:
Qué comando utilizaste  en el paso 25 ?

git log --graph --oneline

PREGUNTA:
El merge del paso 26, podría ser fast forward?  Sí. Por qué ?
Entiendo que sí, porque desde el punto de bifurcación donde se creó la rama "title", la rama "main" no ha tenido nuevos commits.

PREGUNTA:
Qué comando o comandos utilizaste en el paso 27 ?
primero usé git log para obtener el identificador del commit con el cual había registrado previamente el merge, entonces con dicho idenfificador utilicé un segundo comando, que fue el siguiente:
git reset --soft ae51d75b51bc537bfb0259ead95978f9436560a2

PREGUNTA:
Qué comando o comandos utilizaste en el paso 28 ?
git reset --hard ae51d75b51bc537bfb0259ead95978f9436560a2

PREGUNTA:
Qué comando o comandos utilizaste en el paso 29 ?
git branch -d title
git add .    
git commit -m "Eliminación de la rama title"

PREGUNTA:
Qué comando o comandos utilizaste en el paso 30 ?
Primero usé un git log para obtener el identificador del commit donde se registró el merge title en main.
Luego ejecuté git reset --hard  ae51d75b51bc537bfb0259ead95978f9436560a2

PREGUNTA:
Qué comando o comandos utilizaste en el paso 32 ?
Primero usé un git log para obtener el identificador del commit inicial
Luego ejecuté git reset --hard fa2c8e9f0f247ff8c3dd931d11eecb7393e0ae00

PREGUNTA:
Qué comando o comandos utilizaste en el paso 33 ?
Primero usé un git reflog para obtener el identificador del commit donde se creó el título para el poema:
Luego ejecuté git reset --hard 13e192c















