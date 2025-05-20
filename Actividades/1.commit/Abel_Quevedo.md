# 1.1 Preguntas:

**1. ¿Cómo se inicializa un repositorio local?**

comando: git init.

**2. ¿Cómo hago para que un directorio deje de ser controlado por git?**

comando: git ignore <directorio>.

**3. Si agrego un archivo a un directorio que ya está siendo controlado por git, ¿está siendo controlado por git?**

Si.

**4. ¿Qué comando se utiliza para agregar un archivo al repositorio local?**

comando: git add <archivo>.

**5. ¿Cómo determino que archivos fueron modificados?**

comando: git status.

**6. ¿Qué comando se utiliza para hacer un commit?**

comando: git commit -m "comentario de los cambios".

**7. En sus propias palabras, ¿qué es un commit?**

Es un comando que confirma los cambios realizados.

# 1.2 Ejercicio Práctico:

**3. Antes de realizar cualquier acción con git, guarde el estado actual del directorio en el archivo nombre_apellido.txt. Para esto, se debe ejecutar el comando git status y copiar el resultado en el archivo nombre_apellido.txt.** 

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   Actividades/1.commit/sandwich.txt

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        Actividades/1.commit/Abel_Quevedo.txt

no changes added to commit (use "git add" and/or "git commit -a")

Explique que significa la salida del comando: Hay un archivo modificado y un archivo nuevo que hay que agregar y no hay nada listo para ser confirmado.

**5. Explique que cambio en la salida del comando git status luego de ejecutar el comando git add sandwich.txt.**

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   Actividades/1.commit/sandwich.txt

El archivo modificado ha sido agregado y no da error.

**7. Explique que cambio en la salida del comando git status luego de ejecutar el comando git commit -m "Agrego mi sandwich.txt".**

C:\Users\USUARIO\IESlaCa-uelaAWEB>git commit -m "Agrego mi sandwich.txt"
[main 427c1db] Agrego mi sandwich.txt
 1 file changed, 1 insertion(+), 2 deletions(-)

C:\Users\USUARIO\IESlaCa-uelaAWEB>git status
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

El archivo se ha modificado y esta esperando al push para ser publicado

**8. Agregar salsas de su preferencia a sandwich.txt y realizar un commit con el mensaje "Agrego salsas".**

C:\Users\USUARIO\IESlaCa-uelaAWEB>git commit -m "Agrego salsas"
[main cfedf46] Agrego salsas
 1 file changed, 1 insertion(+)

**9. Escriba la salida del comando git log en el archivo nombre_apellido.txt. Y explique que significa. ¿En qué orden aparecen los commits?**

git log muestra el historial de commits en un repositorio, el orden va del mas reciente al mas antiguo.

**10. Pruebe las variaciones del comando git log y explique que observa en cada una de ellas.**

**10.1. git log --oneline** 

Aparece el historial de commits resumidos en una sola linea.

**10.2. git log --stat**

Muestra información estadística sobre los cambios realizados en cada commit.

**11. Inspeccione diferencias entre los commits, use el comando git diff y explique que significa cada uno de los resultados.**

El comando diferencia la versión antigua y la actual de los commits.

**14. Renombrar el archivo sandwich2.txt a sandwich2_feo.txt. Para esto, se debe ejecutar el comando git mv sandwich2.txt sandwich2_feo.txt. Explique que cambio en la salida del comando git status luego de hacer un commit con esos cambios y de git log --oneline.**

Usando git status: 

On branch main
Your branch is ahead of 'origin/main' by 3 commits.
  (use "git push" to publish your local commits)

El commit esta a la espera del push

Usando git log --oneline:

f321ca8 (HEAD -> main) agregacion de archivo sandwich2.txt y cambio de nombre a sandwich2_feo.txt

Aparece el commit realizado

**15. Borre el archivo sandwich2_feo.txt. Para esto, se debe ejecutar el comando git rm sandwich2_feo.txt. Explique que cambio en la salida del comando git status luego de hacer un commit con esos cambios y de git log --oneline.**

Usando git status: 

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        deleted:    Actividades/1.commit/sandwich2_feo.txt

El git status indica que el archivo sandwich2_feo.txt ha sido eliminado

Después del commit:

Your branch is ahead of 'origin/main' by 4 commits.
  (use "git push" to publish your local commits)

Usando git log --oneline:

1d5d910 (HEAD -> main) Eliminacion de sandwich2_feo.txt

Aparece el commit realizado

**16. Inspeccione la bitácora usando git log --stat y explique lo que ve.**

Aparecen todos los cambios y commits realizados.
