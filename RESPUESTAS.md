## 1. ¿Qué es git?

#### `Git es un software de control de versiones diseñado por Linus Torvalds, pensando en la eficiencia y la confiabilidad del mantenimiento de versiones de aplicaciones cuando éstas tienen un gran número de archivos de código fuente.` 

## 2. ¿Por qué queremos utilizar git?

#### `El uso de esta herramienta es útil para cualquier lenguaje de programación y para cualquier equipo de desarrollo; así sea este equipo de una sola persona.`

## 3. ¿Qué es el bash que instala git?

#### `El git bash, es una herramienta de tipo consola que básicamente te permite manipular y gestionar todo el proceso a realizar con el proyecto.`

## 4. Describa los estados (working directory, staging area, repository)

* El directorio de trabajo ***working directory***, repositorio o carpeta donde creas y modificas tus archivos, en esta etapa tus archivos aún no están versionados.
* Se utiliza el comando ***git add nombre_archivo***, para enviar archivos al ***staging area*** que es una área intermedia donde se encuentra un archivo antes de confirmar los cambios.
* Finalmente con el comando ***git commit*** se confirman los cambios y el o los archivos pasan al ***git directory*** o repository que es donde está el archivo versionado.

## 5. Describa el flujo para crear un nuevo repositorio git.

* Debes crear una carpeta, ubicarte dentro de la carpeta desde Git Bash y escribir el comando ***git init***
* Posteriormente dentro de Git Bash pongo el comando cd .. <<"apretoEnter">> hasta llegar a la raíz que es el disco C, luego entro a la carpeta con el comando cd <<"nombreCarpeta">>, utilizo el comando ls -l para ver los archivos y finalmente ejecuto el comando git init para inicializar esa carpeta como un repositorio local.
* Con el comando ls -a puedes ver una carpeta oculta .git/, en esa carpeta se irán almacenando todos los cambios del repositorio <<"nombreCarpeta">>.

## 6. Describa el flujo para agregar un archivo simple al repositorio.

* Con el comando ***git add*** . añades todos los archivos que están en el directorio de trabajo (working directory) y que no han sido añadidos o que han sido añadidos pero que tuvieron alguna modificación después de añadirlos.

* Pero si quieres añadir un archivo en específico lo puedes hacer con el comando git add <<"nombre de archivo">>.

## 7. Describa el flujo para cambiar el archivo agregado y guardar los cambios en el repositorio.

* la letra ***`M`*** en color rojo quiere decir, que el archivo <<"nombre de archivo">> está añadido al stagin area pero ha sido modificado después de añadirlo, cabe recalcar que para que estos cambios sean añadidos al stagin area, se debe nuevamente ejecutar el comando git add <<"nombre de archivo">>

* Dicho esto los cambios que se confirman al repositorio (commit) son los que están actualmente en el stagin area al momento de hacer commit.

1. Iniciar un repositorio local con git init
2. Añadir archivos al staging area con git add . o git add <<"archivo">>
3. Confirmar los cambios en el repositorio con git commit -m ‘comentario’
4. Ver el estado de un archivo git status -s
5. Ver la diferencia entre archivos que están añadidos y los cambios que aún no están con git diff

## 8. ¿Cómo hago para ignorar un archivo o carpeta?

* Crear un archivo ***.gitignore*** antes de comenzar a trabajar es generalmente una buena idea, pues así evitas confirmar accidentalmente archivos que en realidad no quieres incluir en tu repositorio Git.

~~~
$ cat .gitignore
*.[oa]
*~
~~~

* La primera línea le indica a Git que ignore cualquier archivo que termine en `“.o”` o `“.a”` - archivos de objeto o librerías que pueden ser producto de compilar tu código. La segunda línea le indica a Git que ignore todos los archivos que terminen con una tilde `(~)`, la cual es usada por varios editores de texto como Emacs para marcar archivos temporales. También puedes incluir cosas como trazas, temporales, o pid directamente; documentación generada automáticamente; etc.

## 9. Explique qué es un `branch`. Dé un pequeño ejemplo de cómo haría uno.

* Dentro de nuestro sistema de control de versiones podemos ver el histórico de cambios como si de un árbol se tratase. De esta forma podemos ir abriendo ramas que parten bien de la rama principal (master) o de otra rama (branch).

~~~
   $ git branch nuevo-branch
~~~

~~~
    $ git checkout nuevo branch
~~~


## 10. ¿Qué hago con `git add .`?

* El comando ***git add*** añade un cambio del directorio de trabajo en el entorno de ensayo. Indica a Git que quieres incluir actualizaciones en un archivo concreto en la próxima confirmación. Sin embargo, ***git add*** no afecta al repositorio de manera significativa: en realidad, los cambios no se registran hasta que ejecutas ***git commit***.

* Junto con estos comandos, también necesitarás ***git status*** para ver el estado del directorio de trabajo y el entorno de ensayo.

## 11. ¿Cómo cambiamos de un branch a otro?

* Existe un atajo para crear una rama que aún no existe usando directamente el comando checkout que consiste en pasar el parámetro -b en la llamada.

1. $ git checkout -b nuevafuncionalidad.
2. $ git branch master * nuevafuncionalidad.
3. $ git branch -d nuevafuncionalidad.
4. $ git reset --hard HEAD.
5. $ git reset --head ORIG_HEAD.

## 12. Investigue qué es Markdown y responda todas las preguntas anteriores en este lenguaje (con el nombre de archivo RESPUESTAS.md). Súbalo al repositorio

### `Esta herramienta fue creada en 2004 por John Gruber, y se distribuye de manera gratuita bajo una licencia BSD.`

### `Aunque en realidad Markdown también se considera un lenguaje que tiene la finalidad de permitir crear contenido de una manera sencilla de escribir, y que en todo momento mantenga un diseño legible, así que para simplificar puedes considerar Markdown como un método de escritura.`

### `De cara al usuario final no hay ninguna diferencia, por ejemplo este artículo acerca de cómo funciona Transferwise está escrito en Markdown, y sin embargo ves que está perfectamente formateado.`

