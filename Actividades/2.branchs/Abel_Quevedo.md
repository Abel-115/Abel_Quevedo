# 2.1. Preguntas

## **1. ¿Qué es un branch?**

Un branch es una rama de desarrollo, una versión separada del código principal que permite trabajar en nuevas características o correcciones sin afectar el código principal

## **2. ¿Por qué pueden ser útiles los branches?**

Porque te permiten desarrollar características, corregir errores, o experimentar con seguridad las ideas nuevas en un área contenida de tu repositorio.

## **3. ¿Cómo se crea una branch?**

git branch <nombre_rama>

## **4. ¿Cómo se cambia a una branch?**

git checkout <nombre_rama>

## **5. ¿Cómo se elimina una branch?**

git branch -d <nombre_rama>

## **6. ¿Cómo se crea una branch y se cambia a ella en un solo paso?**

git checkout -b <nombre_rama>

## **7. ¿Qué es un merge?**

Es el proceso de integrar los cambios de una rama experimental o de desarrollo en la rama principal para que estén disponibles para la producción. 

## **8. ¿Cómo se realiza un merge?**

git merge <nombre_rama_a_combinar>

## **9. ¿Que es un tag?**

Es una palabra o frase corta que se usa para categorizar o describir contenido, como un artículo, una imagen, un video o cualquier otro tipo de dato.

## **10. ¿Cómo se crea un tag?**

git tag <nombre_de_la_etiqueta>

# 2.2 Ejercicio Práctico

## **1. Crear una branch experimento.**

C:\Users\USUARIO\IESlaCa-uelaAWEB>git branch experimento

## **2. Moverse a la branch experimento.**

C:\Users\USUARIO\IESlaCa-uelaAWEB>git checkout experimento
Switched to branch 'experimento'

## **3. Verificar que se encuentra en la branch experimento.**

C:\Users\USUARIO\IESlaCa-uelaAWEB>git branch
* experimento
  main
  rama-local

## **4. Agregarle el condimento albahaca arriba del queso al archivo 2.branchs/pizza.txt y "commitee" los cambios.**

C:\Users\USUARIO\IESlaCa-uelaAWEB>git add Actividades/2.branchs/pizza.txt

C:\Users\USUARIO\IESlaCa-uelaAWEB>git commit -m "Agrego un ingrediente extra"
[experimento 4bce0be] Agrego un ingrediente extra
 1 file changed, 1 insertion(+)

 ## **5. Agregarle el condimento oregano arriba de la albahaca al archivo 2.branchs/pizza.txt y "commitee" los cambios.**

 C:\Users\USUARIO\IESlaCa-uelaAWEB>git add Actividades/2.branchs/pizza.txt

C:\Users\USUARIO\IESlaCa-uelaAWEB>git commit -m "Agrego oregano"
[experimento 6b5eaa2] Agrego oregano
 1 file changed, 1 insertion(+)

 ## **6. Correr el comando git graph y observar el resultado. ¿Qué observa?**

 C:\Users\USUARIO\IESlaCa-uelaAWEB>git graph
* 6b5eaa2 (HEAD -> experimento) Agrego oregano
* 4bce0be Agrego un ingrediente extra

## **7. Vuelva a la branch master.**

C:\Users\USUARIO\IESlaCa-uelaAWEB>git checkout main
Switched to branch 'main'
Your branch is ahead of 'origin/main' by 5 commits.
  (use "git push" to publish your local commits)

## **8. Crear una branch anana.**

C:\Users\USUARIO\IESlaCa-uelaAWEB>git checkout -b anana
Switched to a new branch 'anana'

## **9. Agregarle el condimento anana debajo del queso al archivo 2.branchs/pizza.txt y "commitee" los cambios.**

C:\Users\USUARIO\IESlaCa-uelaAWEB>git add Actividades/2.branchs/pizza.txt

C:\Users\USUARIO\IESlaCa-uelaAWEB>git commit -m "Agrego el condimento anana debajo del queso"
[anana 1376e34] Agrego el condimento anana debajo del queso
 1 file changed, 1 insertion(+)

 ## **10. Correr el comando git graph y observar el resultado. ¿Qué observa?**

 C:\Users\USUARIO\IESlaCa-uelaAWEB>git graph
* 1376e34 (HEAD -> anana) Agrego el condimento anana debajo del queso
| * 6b5eaa2 (experimento) Agrego oregano
| * 4bce0be Agrego un ingrediente extra
|/

## **11. Vuelva a la branch master.**

C:\Users\USUARIO\IESlaCa-uelaAWEB>git checkout main
Switched to branch 'main'
Your branch is ahead of 'origin/main' by 5 commits.
  (use "git push" to publish your local commits)

## **12. Agregue el condimento cebolla debajo de la salsa al archivo 2.branchs/pizza.txt y "commitee" los cambios.**

C:\Users\USUARIO\IESlaCa-uelaAWEB>git add Actividades/2.branchs/pizza.txt

C:\Users\USUARIO\IESlaCa-uelaAWEB>git commit -m "Agrego cebolla debajo de la salsa"
[main 0dac357] Agrego cebolla debajo de la salsa
 1 file changed, 1 insertion(+)

 ## **13. Correr el comando git graph y observar el resultado. ¿Qué observa?**

 C:\Users\USUARIO\IESlaCa-uelaAWEB>git graph
* 0dac357 (HEAD -> main) Agrego cebolla debajo de la salsa
| * 1376e34 (anana) Agrego el condimento anana debajo del queso
|/
| * 6b5eaa2 (experimento) Agrego oregano
| * 4bce0be Agrego un ingrediente extra
|/

## **14. Haga un merge de la branch anana a la branch master.**

C:\Users\USUARIO\IESlaCa-uelaAWEB>git merge anana

C:\Users\USUARIO\IESlaCa-uelaAWEB>git commit -m "Hago un merge con la rama anana"
[main 197e1f7] Hago un merge con la rama anana

## **15. Correr el comando git graph y observar el resultado. ¿Qué observa?**

C:\Users\USUARIO\IESlaCa-uelaAWEB>git graph
*   197e1f7 (HEAD -> main) Hago un merge con la rama anana
|\
| * 1376e34 (anana) Agrego el condimento anana debajo del queso
* | 0dac357 Agrego cebolla debajo de la salsa
|/
| * 6b5eaa2 (experimento) Agrego oregano
| * 4bce0be Agrego un ingrediente extra
|/

## **16. ¿Qué branches están "mergeadas" a master?**

La branch anana.

## **17. Haga un merge de la branch experimento a la branch master.**

C:\Users\USUARIO\IESlaCa-uelaAWEB>git merge experimento

C:\Users\USUARIO\IESlaCa-uelaAWEB>git commit -m "Hago un merge con la rama experimento"
[main 9637782] Hago un merge con la rama experimento

## **18. Correr el comando git graph y observar el resultado. ¿Qué observa?**

C:\Users\USUARIO\IESlaCa-uelaAWEB>git graph
*   9637782 (HEAD -> main) Hago un merge con la rama experimento
|\
| * 6b5eaa2 (experimento) Agrego oregano
| * 4bce0be Agrego un ingrediente extra
* |   197e1f7 Hago un merge con la rama anana
|\ \
| * | 1376e34 (anana) Agrego el condimento anana debajo del queso
| |/
* / 0dac357 Agrego cebolla debajo de la salsa
|/

## **19. ¿Tuvo que hacer un merge manual, o git lo hizo automáticamente? ¿Por qué?**

Tuvo que hacer un merge manual, porque git esta en medio de un merge y requiere intervención manual.

## **20. ¿Qué branches están "mergeadas" a master?**

Las branchs anana y experimento.

## **21. Elimine la branch anana.**

C:\Users\USUARIO\IESlaCa-uelaAWEB>git branch -d anana
Deleted branch anana (was 1376e34).

## **22. Elimine la branch experimento.**

C:\Users\USUARIO\IESlaCa-uelaAWEB>git branch -d experimento
Deleted branch experimento (was 6b5eaa2).

## **23. ¿Qué branches están "mergeadas" a master?**

Ninguna branch, solo aparecen los commits.

## **24. Correr el comando git graph y observar el resultado. ¿Qué observa?**

C:\Users\USUARIO\IESlaCa-uelaAWEB>git graph
*   9637782 (HEAD -> main) Hago un merge con la rama experimento
|\
| * 6b5eaa2 Agrego oregano
| * 4bce0be Agrego un ingrediente extra
* |   197e1f7 Hago un merge con la rama anana
|\ \
| * | 1376e34 Agrego el condimento anana debajo del queso
| |/
* / 0dac357 Agrego cebolla debajo de la salsa
|/

## **25. Crear un tag pizza en el último commit.**

C:\Users\USUARIO\IESlaCa-uelaAWEB>git tag -a pizza -m "Receta de la pizza."

## **26. Ver los tags creados.**

C:\Users\USUARIO\IESlaCa-uelaAWEB>git tag
pizza

## **27. Ver el tag pizza.**

C:\Users\USUARIO\IESlaCa-uelaAWEB>git show pizza
tag pizza
Tagger: unknown <abelquevedomelgar@gmail.com>
Date:   Thu May 22 17:35:38 2025 +0200

Receta de la pizza.

commit 9637782afcd8f4bb6c3be3831b692fe5001ba817 (HEAD -> main, tag: pizza)
Merge: 197e1f7 6b5eaa2
Author: unknown <abelquevedomelgar@gmail.com>
Date:   Thu May 22 17:20:25 2025 +0200

    Hago un merge con la rama experimento

diff --cc Actividades/2.branchs/pizza.txt
index 961bd26,b523cb9..e605624
--- a/Actividades/2.branchs/pizza.txt
+++ b/Actividades/2.branchs/pizza.txt
@@@ -1,5 -1,5 +1,7 @@@
+ oregano
+ albahaca
  queso
 +anana
  salsa de tomate
 +cebolla
  masa de pizza
