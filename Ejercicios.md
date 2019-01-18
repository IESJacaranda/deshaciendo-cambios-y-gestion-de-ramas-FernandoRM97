1. Tienes que modificar la escena 5 de Hamlet en el fichero scene-5.txt. En dicha escena Hamlet encuentra al fantasma de su padre. Añade este texto al fichero:
> Ghost: 
> My hour is almost come,
> When I to sulphurous and tormenting flames
> Must render up myself.

Después de haber inicializado el repositorio y haber entrado en la carpeta donde están todos los archivos.
Con nano scene-5.txt entramos en el contenido del archivo y lo modificamos con nos dice el enunciado.

2. Añade scene-5.txt al área de preparación.

git add scene-5.txt 

3. Haz un commit con los cambios con un buen mensaje de commit.

git commit scene.5.txt -m "Añadiendo los cambios del guión de la escena 5 del fantasma"

4. Modifica las palabras del fantasma. Aquí tienes una sugerencia divertida:
> Ghost: 
> My hour is almost come,
> When I to sulphurous and tormenting balloons
> Must render up myself.

nano scene-5.txt 
Cambiamos la palabra flames por balloons

5. Devuelve el fichero al estado del último commit.

git reset --hard

6. Cambia el nombre de LARRY por LAERTES en los ficheros scene-3.txt y scene-7.txt.

nano scene-3.txt
Modificamos el nombre
nano scene-7.txt
Modificamos el nombre

7. Añade los ficheros al área de preparación usando un único comando git.

git add *

8. Vamos a cometer un error a propósito. Borra cualquier línea del fichero scene-2.txt.

nano scene-2.txt
Borramos cualquier linea.

9. Añade scene-2.txt al área de preparación.

git add scene-2.txt

10. Comprueba el estado del repositorio. 

git status

11. Devuelve scene-2.txt al directorio de trabajo.

git reset HEAD scene.2-txt

12. Haz un commit para guardar los cambios realizados en el nombre de Larry por Laertes.

git commit -m "Cambiando el nombre LARRY por larry de los guiones"

13. Busca el primer commit que has hecho y vuelve a dicho commit. Indica como has buscado el commit anterior y como has vuelto a él.

git log --oneline

14. Crea una nueva rama llamada **reinventando_hamlet**

git branch reinventando_hamlet

15. Cámbiate a dicha rama

git checkout reinventando_hamlet

16. Mejora la escena 2 como creas conveniente.

nano scene-2.txt
Le he añadido una linea de texto mas al rey

17. Haz un commit con los cambios con un mensaje adecuado.

git commit scene-2.txt -m "Añadiendo cambios al guión del rey en la escena 2"

18. Vuelve a la rama master.

git checkout master

19. Elimina la rama **reinventando_hamlet**

git branch -d reinventando_hamlet
Pide que si estamos seguros le añadamos al código -D
git branch -D reinventando_hamlet

20. Crea una nueva rama, modifica algo en la rama master, haz commit y llévate los cambios a la rama que has creado.

git branch hamlet_v2
Voy a modificar la scene-2.txt cambiando el contenido de la primera línea
nano scene-2.txt
git add scene-2.txt
git commit scene-2.txt -m "Cambiando el guion de la escena 2"
git push
git checkout hamlet_v2
git pull origin master

21. Provoca un conflicto entre la rama master y la rama que has creado (indica lo que has hecho). Une la rama a la rama master resolviendo el conflicto.

Ponemos un contenido alternativo a la línea que modificamos antes en la rama master, así creando el conflicto. 
git checkout master
git merge hamlet_v2
Nos salta un conflicto, para solucionarlo lo que he hecho es abrir el nano y modificar el archivo.
nano scene-2.txt
Y conflicto resuelto.



