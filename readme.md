## Preguntas y respuestas del ejercicio
- ¿Qué comando utilizaste en el paso 11? ¿Por qué?
git reset --hard HEAD~1
Porque con este comando paso el HEAD y el puntero de la rama style al commit anterior deshaciendo el commit sin dejar los cambios que realicé en el Working Area.

- ¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué? 
Primero: git reflog. Para obtener el identificador del commit al que quiero mover el HEAD y el puntero. Me fijo en que he llegado al commit al que estoy ahora tras haber hecho HEAD~1, por tanto su padre es el commit que me interesa. Copio el identificador del commit padre.
Segundo: git reset --hard c470208. Para mover el HEAD y el puntero de la rama style al commit donde estaban incluidos los cambios al commit-nuestro.md.

- El merge del paso 13, ¿Causó algún conflicto? ¿Por qué? 
Al intentar hacer este merge nos sale el mensaje “Already up to date” porque lo que nos pide el enunciado es que styled absorba a master, pero styled ya ha absorbido a master porque styled contiene todos los commits de master ya que ha sido creada a partir de master. Por tanto, no se genera un merge y no hay conflictos.

- El merge del paso 19, ¿Causó algún conflicto? ¿Por qué? 
Sí causó conflicto. Porque estábamos haciendo un merge de dos ramas que contenían commits que han hecho modificaciones al documento git-nuestro.md sobre las mismas filas.

- El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?
No genera conflicto. Porque las dos ramas están en una lista y lo único que sucede este que puntero de la rama master pasa a estar en el último commit de la rama styled.

- ¿Qué comando o comandos utilizaste en el paso 25?
git log --graph. Se ve como es una línea donde el puntero title está el último commit, todos los demás están en el penúltimo commit y el HEAD también. He hecho un dibujo, pero creo que no tengo forma de meterlo aquí sin tener que crear un espacio en internet con la imagen.

- El merge del paso 26, ¿Podría ser fast forward? ¿Por qué? 
Sí, porque como muestra el graffo, los commits de las dos ramas están dispuestos en forma de línea.

- ¿Qué comando o comandos utilizaste en el paso 27? 
git reset HEAD~1

- ¿Qué comando o comandos utilizaste en el paso 28? 
git checkout -- git-nuestro.md

- ¿Qué comando o comandos utilizaste en el paso 29?
git branch -D title

- ¿Qué comando o comandos utilizaste en el paso 30? 
Primero git reflog para copiar el identificador del commit que se generó tras hacer el merge no fast-forward. Luego,  git reset --hard 5f10274 para mover el HEAD y el puntero de la rama master al commit con el título.
Entiendo que así, he conseguido el propósito sin tener que volver a crear la rama style y hacer merge entre style y master.

- ¿Qué comando o comandos usaste en el paso 32?
No sé si se refiere a que vayamos con el HEAD únicamente o que nos quedemos solo con el commit inicial. En cualquier caso, en las dos opciones, primero buscaría el identificador del commit con git log y bajando hasta encontrarlo. Luego, si estamos en el primer caso, simplemente hacer checkout al commit. Si estamos en el segundo caso, hacer git reset --hard al commit.

- ¿Qué comando o comandos usaste en el punto 33?
La respuesta depende de la interpretación de la pregunta anterior. Si fuera la opción 1, volver a buscar el identificador utilizando git log y luego hacer git checkout al commit. Si fuera la opción 2, tendríamos que buscar el identificador del commit utilizando ref log y luego hacer git reset al commit.


