# **3.1 Preguntas**

## **1. ¿Qué es un conflicto?**

Un conflicto es una situación que ocurre cuando Git no puede fusionar automáticamente los cambios de dos ramas porque hay modificaciones que entran en conflicto

## **¿Cuando ocurre?**

Ocurre cuando Git no puede fusionar automáticamente los cambios realizados en dos ramas diferentes del mismo repositorio.

## **¿Es bueno o malo?**

Es bueno ya que obligan a revisar cuidadosamente los cambios antes de fusionarlos. 

## **2. ¿Se puede evitar un conflicto?**

Si se puede evitar

## **¿Cómo?**

Manteniendo las ramas actualizadas

# **3.2 Ejercicio Práctico**

## **1. Crear un archivo nombre_apellido.txt dentro de la carpeta 3.conflicts.**

C:\Users\USUARIO\IESlaCa-uelaAWEB>mkdir Actividades/3.conflicts/Abel_Quevedo.txt

## **2. Crear una nueva branch suprema a partir de la branch master.**

C:\Users\USUARIO\IESlaCa-uelaAWEB>git checkout -b suprema
Switched to a new branch 'suprema'

## **3. Moverse a la branch suprema.**

C:\Users\USUARIO\IESlaCa-uelaAWEB>git checkout suprema
Switched to branch 'suprema'

## **4. Cambiar el contenido del archivo 3.conflicts/milanesa.txt donde dice lomo por pollo.**

pan rallado
pollo

## **5. "Commitear" los cambios.**

C:\Users\USUARIO\IESlaCa-uelaAWEB>git add Actividades/3.conflicts/milanesa.txt

C:\Users\USUARIO\IESlaCa-uelaAWEB>git commit -m "Cambio de lomo a pollo"
[suprema cdda533] Cambio de lomo a pollo
 1 file changed, 1 insertion(+), 1 deletion(-)

## **6. Moverse a la branch master.**

C:\Users\USUARIO\IESlaCa-uelaAWEB>git checkout main
Switched to branch 'main'
Your branch is ahead of 'origin/main' by 11 commits.
  (use "git push" to publish your local commits)

## **7. Crear una nueva branch bife a partir de la branch master.**

C:\Users\USUARIO\IESlaCa-uelaAWEB>git checkout -b bife
Switched to a new branch 'bife'

## **8. Moverse a la branch bife.**

C:\Users\USUARIO\IESlaCa-uelaAWEB>git checkout bife
Switched to branch 'bife'

## **9. Cambiar el contenido del archivo 3.conflicts/milanesa.txt donde dice lomo por bife.**

pan rallado
bife

C:\Users\USUARIO\IESlaCa-uelaAWEB>git add Actividades/3.conflicts/milanesa.txt

C:\Users\USUARIO\IESlaCa-uelaAWEB>git commit -m "Cambio de pollo a bife"
[bife 92513df] Cambio de pollo a bife
 1 file changed, 1 insertion(+), 1 deletion(-)

## **10. Haga un git diff master suprema y un git diff master bife. ¿Qué observa?**

C:\Users\USUARIO\IESlaCa-uelaAWEB>git diff main suprema
diff --git a/Actividades/3.conflicts/milanesa.txt b/Actividades/3.conflicts/milanesa.txt
index 5255304..1c57c4d 100644
--- a/Actividades/3.conflicts/milanesa.txt
+++ b/Actividades/3.conflicts/milanesa.txt
@@ -1,2 +1,2 @@
 pan rallado
-lomo
\ No newline at end of file
+pollo
\ No newline at end of file

C:\Users\USUARIO\IESlaCa-uelaAWEB>git diff main bife
diff --git a/Actividades/3.conflicts/milanesa.txt b/Actividades/3.conflicts/milanesa.txt
index 5255304..1712737 100644
--- a/Actividades/3.conflicts/milanesa.txt
+++ b/Actividades/3.conflicts/milanesa.txt
@@ -1,2 +1,2 @@
 pan rallado
-lomo
\ No newline at end of file
+bife
\ No newline at end of file

## **11. Moverse a la branch master. Corra un git status, ¿qué observa?**

C:\Users\USUARIO\IESlaCa-uelaAWEB>git checkout main
Switched to branch 'main'
Your branch is ahead of 'origin/main' by 11 commits.
  (use "git push" to publish your local commits)

C:\Users\USUARIO\IESlaCa-uelaAWEB>git status
On branch main
Your branch is ahead of 'origin/main' by 11 commits.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean

## **12. Ejecute git merge bife.**

C:\Users\USUARIO\IESlaCa-uelaAWEB>git merge bife
Updating 9637782..92513df
Fast-forward
 Actividades/3.conflicts/milanesa.txt | 2 +-
 1 file changed, 1 insertion(+), 1 deletion(-)

 ## **¿Funcionó?**

 Si

 ## **13. Ejecute git merge suprema.**

 C:\Users\USUARIO\IESlaCa-uelaAWEB>git merge suprema
Auto-merging Actividades/3.conflicts/milanesa.txt
CONFLICT (content): Merge conflict in Actividades/3.conflicts/milanesa.txt
Automatic merge failed; fix conflicts and then commit the result.

## **¿Fucionó?**

No, porque hay un conflicto

## **14. Ejecute git status. Que observa?**

C:\Users\USUARIO\IESlaCa-uelaAWEB>git status
On branch main
Your branch is ahead of 'origin/main' by 12 commits.
  (use "git push" to publish your local commits)

You have unmerged paths.
  (fix conflicts and run "git commit")
  (use "git merge --abort" to abort the merge)

Unmerged paths:
  (use "git add <file>..." to mark resolution)
        both modified:   Actividades/3.conflicts/milanesa.txt

no changes added to commit (use "git add" and/or "git commit -a")

## **15. Vea el contenido del archivo 3.conflicts/milanesa.txt. ¿Qué observa?**

pan rallado
<<<<<<< HEAD
bife
=======
pollo
>>>>>>> suprema

## **16. Aborte el merge.**

C:\Users\USUARIO\IESlaCa-uelaAWEB>git merge --abort

## **17. Vuelva a ejecutar git merge suprema.**

C:\Users\USUARIO\IESlaCa-uelaAWEB>git merge suprema
Auto-merging Actividades/3.conflicts/milanesa.txt
CONFLICT (content): Merge conflict in Actividades/3.conflicts/milanesa.txt
Automatic merge failed; fix conflicts and then commit the result.

## **18. Resuelva el conflicto manualmente.**

milanesa.txt

pan rallado
bife
pollo

C:\Users\USUARIO\IESlaCa-uelaAWEB>git add Actividades/3.conflicts/milanesa.txt

C:\Users\USUARIO\IESlaCa-uelaAWEB>git merge suprema
fatal: You have not concluded your merge (MERGE_HEAD exists).
Please, commit your changes before you merge.

C:\Users\USUARIO\IESlaCa-uelaAWEB>git commit -m "Hago un merge con la rama suprema"
[main 843fa03] Hago un merge con la rama suprema

C:\Users\USUARIO\IESlaCa-uelaAWEB>git graph
*   843fa03 (HEAD -> main) Hago un merge con la rama suprema
|\
| * cdda533 (suprema) Cambio de lomo a pollo
* | 92513df (bife) Cambio de pollo a bife
|/

C:\Users\USUARIO\IESlaCa-uelaAWEB>git status
On branch main
Your branch is ahead of 'origin/main' by 14 commits.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean
