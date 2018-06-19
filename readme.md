# Cuestionario ejercicio 1 gitHub

- ¿Qué comando utilizaste en el paso 11? ¿Por qué?

**git reset --hard HEAD~1**
Con reset le indico al puntero de la rama en la que estoy (styled) que apunte a  HEAD~1,esto es, al primer ascendiente inmediato a donde apunta HEAD (que apunta a styled) que es el commit en el cual 
estoy (resumiendo voy al commit padre inmediato de la rama en la que estoy). Con modificador --hard además le indico que no conservo el work copy que tenia sino que recupere el del commit al que me desplazo.


- ¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?

**git reflog**
Para ver el identificador del commit que ha quedado detached en la rama styled.

**git reset --hard *(identidicador detached)* **
Para indicar al puntero de la rama en la que estoy (styled) que apunte al commit detached, recuperando tambien el work copy del commit al que me desplazo.


- El merge del paso 13, ¿Causó algún conﬂicto? ¿Por qué?

No ha causado ningun conflicto ya que la todos los commits de la rama que quiero absorber (master) son comunes (ya estan absorbidos por styled).


- El merge del paso 19, ¿Causó algún conﬂicto? ¿Por qué?

Sí ha causado conflicto. Porque la rama que voy a absorver (htmlify) tiene cambios en las mismas lineas del mismo fichero que tengo en la rama desde donde absorbo (styled). Ha hecho un merge no fast 
forward creando un commit.


- El merge del paso 21, ¿Causó algún conﬂicto? ¿Por qué?

No ha causado conflicto. Hace un merge fast forward (cambio el puntero master al commit donde apunta styled) al no quedar fuera ningun commit de la rama styled, así que automaticamente basta con avanzar 
el puntero a donde apunta styled.


- ¿Qué comando o comandos utilizaste en el paso 25?

**git log --graph**
Tambien puedo pintar con git log --graph --decorate --pretty=oneline por ejemplo, para ver el dibujo con los punteros y con la informacion mas resumida. Tambien lo hago con un alias que designé para 
esta tarea.


- El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?

Si podria ser fast forward. Porque avanzando el puntero master hasta title no dejamos fuera ningun commit, todos son comunes.


- ¿Qué comando o comandos utilizaste en el paso 27?

**git reset HEAD~1**


- ¿Qué comando o comandos utilizaste en el paso 28?

**git checkout git-nuestro.md**


- ¿Qué comando o comandos utilizaste en el paso 29?

**git branch -D title**


- ¿Qué comando o comandos utilizaste en el paso 30?

**git reflog *(busco identificador del commit donde hicimos merge con title)* **

**git reset --hard *(identificador)* **


- ¿Qué comando o comandos usaste en el paso 32?

**git log *(busco identificador del primer commit)* **
**git reset --hard *(indentificador)* **


- ¿Qué comando o comandos usaste en el punto 33?

**git reflog *(busco identificador del commit donde hice merge a la rama title)* **
**git reset --hard *(identificador)* **
