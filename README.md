# DATA SCIENCE TOOLKIT
## EJERCICIOS GIT, GITHUB Y MARKDOWN

Julián Gómez

![picture alt](https://dujk9xa5fr1wz.cloudfront.net/course/480x270/221696_d05a_4.jpg "DATA SCIENCE TOOLKIT") 

# 2.1 REPOSITORIO CAMPUSCIFF (I)
## 1. Crear un repositorio en vuestro GitHub llamado campusciff.

En la página web de github

![picture alt](/resources/Image1.png "Imagen1") 
![picture alt](/resources/Image2.png "Imagen2") 


##  2.2 REPOSITORIO CAMPUSCIFF (II)
### 1. Clonar vuestro repositorio en local.

```
MacBook-Pro-de-Julian:~ jgomez$ git clone git@github.com:CIFFjuliangomez/campusciff.git
Cloning into 'campusciff'...
remote: Counting objects: 3, done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (3/3), done.
Checking connectivity... done.
MacBook-Pro-de-Julian:~ jgomez$ cd campusciff
MacBook-Pro-de-Julian:campusciff jgomez$ ls -la
total 8
drwxr-xr-x   4 jgomez  staff   136  6 dic 19:44 .
drwxr-xr-x+ 42 jgomez  staff  1428  6 dic 19:44 ..
drwxr-xr-x  13 jgomez  staff   442  6 dic 19:44 .git
-rw-r--r--   1 jgomez  staff    49  6 dic 19:44 README.md
```
Al crear el repositorio remoto campusciff, ya incluimos el fichero README.md, por tanto durante la clonación del mismo ya hemos disponibilizado el fichero en nuestro repositorio local de trabajo.


##  2.3 README
### 1. Crear (si no lo habéis creado ya) en vuestro repositorio local un documento README.md. 
>Notas: en este documento tendreís que ir poniendo los comandos que habéis tenido que utilizar durante todos los ejercicios y las explicaciones y capturas de pantalla que consideréis necesarias.
  
  Ya creado al inicio :+1:
  
## 2.4 COMMIT INICIAL
#### 1. Añadir al README.md los comandos utilizados hasta ahora y hacer un commit inicial con el mensaje commit inicial.

```
MacBook-Pro-de-Julian:campusciff jgomez$ vim README.md
MacBook-Pro-de-Julian:campusciff jgomez$ git add .
MacBook-Pro-de-Julian:campusciff jgomez$ git commit -m "commit inicial: README.md actualizado"
[master 104cf1f] commit inicial: README.md actualizado
 1 file changed, 54 insertions(+), 2 deletions(-)
 rewrite README.md (100%)
MacBook-Pro-de-Julian:campusciff jgomez$ 
MacBook-Pro-de-Julian:campusciff jgomez$ git list
* 104cf1f (HEAD -> master) commit inicial: README.md actualizado
* 6c0e503 (origin/master, origin/HEAD) Initial commit
```

## 2.5 PUSH INICIAL
### 1. Subir los cambios al repositorio remoto.

```
MacBook-Pro-de-Julian:campusciff jgomez$ git push origin master
Counting objects: 3, done.
Delta compression using up to 8 threads.
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 1.24 KiB | 0 bytes/s, done.
Total 3 (delta 0), reused 0 (delta 0)
To git@github.com:CIFFjuliangomez/campusciff.git
   6c0e503..104cf1f  master -> master
MacBook-Pro-de-Julian:campusciff jgomez$
```



## 2.6 IGNORAR ARCHIVOS (2.6 IGNORAR ARCHIVOS (I)
### 1. Crear en el repositorio local un fichero llamado privado.txt.

```
MacBook-Pro-de-Julian:campusciff jgomez$ vim privado.txt
MacBook-Pro-de-Julian:campusciff jgomez$ 
```
### 2. Crear en el repositorio local una carpeta llamada privada.

```
MacBook-Pro-de-Julian:campusciff jgomez$ mkdir privada
MacBook-Pro-de-Julian:campusciff jgomez$ 
```
## 2.7 IGNORAR ARCHIVOS (II)
### 1. Realizar los cambios oportunos para que tanto el archivo como la carpeta sean ignorados por git.

```
MacBook-Pro-de-Julian:campusciff jgomez$ cat .gitignore
privado.txt
/privada
```

## 2.8 AÑADIR FICHERO 1.TXT
### 1. Añadir fichero 1.txt al repositorio local.
 
```
MacBook-Pro-de-Julian:campusciff jgomez$ vim 1.txt
MacBook-Pro-de-Julian:campusciff jgomez$ git add .
MacBook-Pro-de-Julian:campusciff jgomez$ git commit -m "añado fichero 1.txt"
[master 396ff5d] añado fichero 1.txt
 2 files changed, 3 insertions(+)
 create mode 100644 .gitignore
 create mode 100644 1.txt
```
 
## 2.9 CREAR EL TAG V0.1
### 1. Crear un tag v0.1.

```
MacBook-Pro-de-Julian:campusciff jgomez$ git tag -a V0.1 -m "versión V0.1"
MacBook-Pro-de-Julian:campusciff jgomez$ 
```

## 2.10 SUBIR EL TAG V0.1
### Subir los cambios al repositorio remoto.


git push --tag origin master  (Sustituir master por un nombre de rama si se desea crear una nueva rama en el servidor remoto)

```
MacBook-Pro-de-Julian:campusciff jgomez$ git push --tag origin master
Counting objects: 5, done.
Delta compression using up to 8 threads.
Compressing objects: 100% (3/3), done.
Writing objects: 100% (5/5), 511 bytes | 0 bytes/s, done.
Total 5 (delta 0), reused 0 (delta 0)
To git@github.com:CIFFjuliangomez/campusciff.git
   d079fdc..396ff5d  master -> master
 * [new tag]         V0.1 -> V0.1
MacBook-Pro-de-Julian:campusciff jgomez$ 
```

![picture alt](/resources/Image4.png "Imagen4") 




### 2.11 CREAR UNA RAMA V0.2
### 1. Crear una rama v0.2.
### 2. Posiciona tu carpeta de trabajo en esta rama.

Con un solo comando podemos hacerlo a la vez
```
MacBook-Pro-de-Julian:campusciff jgomez$ git checkout -b V0.2
Switched to a new branch 'V0.2'
```

comprobación

```
MacBook-Pro-de-Julian:campusciff jgomez$ git list
* bce32bd (HEAD -> V0.2, tag: V0.1, origin/master, origin/HEAD, master) Añadido 1.txt incial
* 104cf1f commit inicial: README.md actualizado
* 6c0e503 Initial commit
```

## 2.12 AÑADIR FICHERO 2.TXT
### Añadir un fichero 2.txt en la rama v0.2.

```
MacBook-Pro-de-Julian:campusciff jgomez$ vim 2.txt
MacBook-Pro-de-Julian:campusciff jgomez$ git add .
MacBook-Pro-de-Julian:campusciff jgomez$ git commit -m "añadido ficchero 2.txt en la rama V0.2."
[V0.2 01f9895] añadido ficchero 2.txt en la rama V0.2.
 1 file changed, 1 insertion(+)
 create mode 100644 2.txt
 ```
comprobación

```
MacBook-Pro-de-Julian:campusciff jgomez$ git list
* 01f9895 (HEAD -> V0.2) añadido ficchero 2.txt en la rama V0.2.
* bce32bd (tag: V0.1, origin/master, origin/HEAD, master) Añadido 1.txt incial
* 104cf1f commit inicial: README.md actualizado
* 6c0e503 Initial commit
```
 
 
## 2.13 CREAR RAMA REMOTA V0.2 
### 1. Subir los cambios al repositorio remoto.
```
MacBook-Pro-de-Julian:campusciff jgomez$ git push origin V0.2
Counting objects: 3, done.
Delta compression using up to 8 threads.
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 382 bytes | 0 bytes/s, done.
Total 3 (delta 0), reused 0 (delta 0)
To git@github.com:CIFFjuliangomez/campusciff.git
 * [new branch]      V0.2 -> V0.2
```


## 2.14 MERGE DIRECTO 
### Posicionarse en la rama master.

```
MacBook-Pro-de-Julian:campusciff jgomez$ git checkout master
Switched to branch 'master'
Your branch is up-to-date with 'origin/master'.
MacBook-Pro-de-Julian:campusciff jgomez$ ls -la
total 32
drwxr-xr-x   8 jgomez  staff  272  6 dic 11:24 .
drwxr-xr-x   4 jgomez  staff  136  6 dic 09:16 ..
drwxr-xr-x  16 jgomez  staff  544  6 dic 11:24 .git
-rw-r--r--   1 jgomez  staff   21  6 dic 09:51 .gitignore
-rw-r--r--   1 jgomez  staff   30  6 dic 09:53 1.txt
-rw-r--r--   1 jgomez  staff  907  6 dic 09:21 README.md
drwxr-xr-x   2 jgomez  staff   68  6 dic 09:39 privada
-rw-r--r--   1 jgomez  staff   49  6 dic 09:37 privado.txt
```

### 2. Hacer un merge de la rama v0.2 en la rama master.
```
MacBook-Pro-de-Julian:campusciff jgomez$ git branch
  V0.2
* master
MacBook-Pro-de-Julian:campusciff jgomez$ git merge v0.2 -m "Hago un merge de la master con la rama v0.2"
Merge made by the 'recursive' strategy.
 2.txt | 1 +
 1 file changed, 1 insertion(+)
 create mode 100644 2.txt
MacBook-Pro-de-Julian:campusciff jgomez$ ls -la
total 64
drwxr-xr-x   9 jgomez  staff    306  7 dic 21:12 .
drwxr-xr-x+ 42 jgomez  staff   1428  6 dic 23:18 ..
drwxr-xr-x  16 jgomez  staff    544  7 dic 21:12 .git
-rw-r--r--   1 jgomez  staff     21  6 dic 22:43 .gitignore
-rw-r--r--   1 jgomez  staff     11  6 dic 22:45 1.txt
-rw-r--r--   1 jgomez  staff     24  7 dic 21:12 2.txt
-rw-r--r--   1 jgomez  staff  14539  6 dic 22:51 README.md
drwxr-xr-x   2 jgomez  staff     68  6 dic 22:43 privada
-rw-r--r--   1 jgomez  staff     27  6 dic 22:41 privado.txt
MacBook-Pro-de-Julian:campusciff jgomez$ git merge V0.2
Updating 396ff5d..d290ef9
Fast-forward
 2.txt | 1 +
 1 file changed, 1 insertion(+)
 create mode 100644 2.txt
MacBook-Pro-de-Julian:campusciff jgomez$
MacBook-Pro-de-Julian:campusciff jgomez$ ls -la
total 40
drwxr-xr-x   9 jgomez  staff  306  6 dic 11:26 .
drwxr-xr-x   4 jgomez  staff  136  6 dic 09:16 ..
drwxr-xr-x  16 jgomez  staff  544  6 dic 11:26 .git
-rw-r--r--   1 jgomez  staff   21  6 dic 09:51 .gitignore
-rw-r--r--   1 jgomez  staff   30  6 dic 09:53 1.txt
-rw-r--r--   1 jgomez  staff   28  6 dic 11:26 2.txt
-rw-r--r--   1 jgomez  staff  907  6 dic 09:21 README.md
drwxr-xr-x   2 jgomez  staff   68  6 dic 09:39 privada
-rw-r--r--   1 jgomez  staff   49  6 dic 09:37 privado.txt
```

## 2.15 MERGE CON CONFLICTO (I)
###1. En la rama master poner Hola en el fichero 1.txt y hacer commit.
```
MacBook-Pro-de-Julian:campusciff jgomez$ vim 1.txt
MacBook-Pro-de-Julian:campusciff jgomez$ git add .
MacBook-Pro-de-Julian:campusciff jgomez$ git commit -m "Escribo Hola en 1.txt"
[master b2197ff] Escribo Hola en 1.txt
 1 file changed, 1 insertion(+), 1 deletion(-)
MacBook-Pro-de-Julian:campusciff jgomez$ cat 1.txt
Hola
```
## 2.16 MERGE CON CONFLICTO (II)
### 1. Posicionarse en la rama v0.2 y poner Adios en el fichero "1.txt" y hacer commit.

```
MMacBook-Pro-de-Julian:campusciff jgomez$ git checkout V0.2
Switched to branch 'V0.2'
MacBook-Pro-de-Julian:campusciff jgomez$ vim 1.txt
MacBook-Pro-de-Julian:campusciff jgomez$ git add .
MacBook-Pro-de-Julian:campusciff jgomez$ git commit -m "Escribo Adios en 1.txt"
[V0.2 d7c89a8] Escribo Adios en 1.txt
 1 file changed, 1 insertion(+), 1 deletion(-)
 
```


## 2.17 MERGE CON CONFLICTO (III)
### 1. Posicionarse de nuevo en la rama master y hacer un merge con la rama v0.2
```
MacBook-Pro-de-Julian:campusciff jgomez$ git checkout master
Switched to branch 'master'
Your branch is ahead of 'origin/master' by 3 commits.
  (use "git push" to publish your local commits)
MacBook-Pro-de-Julian:campusciff jgomez$ git merge V0.2 -m "Tratando de hacer el merge con conflicto con la rama V0.2"
Auto-merging 1.txt
CONFLICT (content): Merge conflict in 1.txt
Automatic merge failed; fix conflicts and then commit the result.
```


## 2.18 LISTADO DE RAMAS
### 1. Listar las ramas con merge y las ramas sin merge.
```
MacBook-Pro-de-Julian:campusciff jgomez$ git branch --merged
* master
MacBook-Pro-de-Julian:campusciff jgomez$ git branch --no-merged
  V0.2
```

## 2.19 ARREGLAR CONFLICTO
### 1. Arreglar el conflicto anterior y hacer un commit.
```
MacBook-Pro-de-Julian:campusciff jgomez$ cat 1.txt
<<<<<<< HEAD
Hola
=======
Adios
>>>>>>> V0.2
MacBook-Pro-de-Julian:campusciff jgomez$ vi 1.txt
```
Vuelvo a hacer el merge

```
MacBook-Pro-de-Julian:campusciff jgomez$ git add .
MacBook-Pro-de-Julian:campusciff jgomez$  git commit -m "Repetimos el merge con el conflicto en  1.txt resuelto" 
[master 6e3dcaa] Repetimos el merge con el conflicto en  1.txt resuelto
MacBook-Pro-de-Julian:campusciff jgomez$ git push origin master
Counting objects: 8, done.
Delta compression using up to 8 threads.
Compressing objects: 100% (6/6), done.
Writing objects: 100% (8/8), 962 bytes | 0 bytes/s, done.
Total 8 (delta 2), reused 0 (delta 0)
To git@github.com:CIFFjuliangomez/campusciff.git
   4d25374..6e3dcaa  master -> master
```

## 2.20 BORRAR RAMA
### 1. Crear un tag V0.2.2 Borrar la rama V0.2
```
MacBook-Pro-de-Julian:campusciff jgomez$ git tag V0.2
MacBook-Pro-de-Julian:campusciff jgomez$ git tag
V0.1
V0.2
MacBook-Pro-de-Julian:campusciff jgomez$ git branch
  V0.2
* master
```

Elimino la rama del repositorio local

```
MacBook-Pro-de-Julian:campusciff jgomez$ git branch -d V0.2  
Deleted branch V0.2 (was d7c89a8).
MacBook-Pro-de-Julian:campusciff jgomez$ git branch
* master
```
Subo los cambios y verifico el estado de todos los cambios y ramas

```
MacBook-Pro-de-Julian:campusciff jgomez$ git push origin master
Everything up-to-date
MacBook-Pro-de-Julian:campusciff jgomez$ git list
*   6e3dcaa (HEAD -> master, tag: V0.2, origin/master, origin/HEAD) Repetimos el merge con el conflicto en  1.txt resuelto
|\  
| * d7c89a8 Escribo Adios en 1.txt
* | b2197ff Escribo Hola en 1.txt
* |   35653f2 Hago un merge de la master con la rama v0.2
|\ \  
| |/  
| * 01f9895 (origin/V0.2) añadido ficchero 2.txt en la rama V0.2.
* |
|/  
* bce32bd (tag: V0.1) Añadido 1.txt incial
* 104cf1f commit inicial: README.md actualizado
* 6c0e503 Initial commit
MacBook-Pro-de-Julian:campusciff jgomez$ 
```
> git list es un alias que hemos creado para el comando    git log --oneline --decorate --graph --all

## 2.21 LISTADO DE CAMBIOS
### 1. Listar los distintos commits con sus ramas y sus tags.

```
MacBook-Pro-de-Julian:campusciff jgomez$ git log
commit 6e3dcaa44bc3529f55917a0f254ed53794e26c86
Merge: b2197ff d7c89a8
Author: jgomez <juliangomez@campusciff.net>
Date:   Mon Dec 7 22:13:34 2015 +0100

    Repetimos el merge con el conflicto en  1.txt resuelto

commit d7c89a8020c8e52e5aee8e242ddc40b0f3a55adf
Author: jgomez <juliangomez@campusciff.net>
Date:   Mon Dec 7 21:29:59 2015 +0100

    Escribo Adios en 1.txt

commit b2197ff0b61effccdb38c0b9e0227ba824bea0c6
Author: jgomez <juliangomez@campusciff.net>
Date:   Mon Dec 7 21:25:34 2015 +0100

    Escribo Hola en 1.txt

commit 35653f2e8575962e662776421763c7b373b5dde9
Merge: 4d25374 01f9895
Author: jgomez <juliangomez@campusciff.net>
Date:   Mon Dec 7 21:12:03 2015 +0100

    Hago un merge de la master con la rama v0.2

commit 01f989524d1f3cc9f2a7e461a478ac35ca581be1
Author: jgomez <juliangomez@campusciff.net>
Date:   Sun Dec 6 23:19:20 2015 +0100

    añadido ficchero 2.txt en la rama V0.2.

commit bce32bd47afb03d268576bf6e1fe1db4c818cc0a
Author: jgomez <juliangomez@campusciff.net>
Date:   Sun Dec 6 22:54:31 2015 +0100

    Añadido 1.txt incial

commit 104cf1f450e661fdee0659f4507309c4506623b9
Author: jgomez <juliangomez@campusciff.net>
Date:   Sun Dec 6 22:27:11 2015 +0100

    commit inicial: README.md actualizado

commit 6c0e5037112280454c8bb198852e30abb5e9782f
Author: Juián Gómez <juliangomez@campusciff.net>
Date:   Sun Dec 6 19:34:27 2015 +0100

    Initial commit
```


***


# PARTE DE GITHUB

## 2.22 CUENTA DE GITHUB
### 1. Poner una foto en vuestro perfil de GitHub.
### 2. Poner el doble factor de autentificación en vuestra cuenta de GitHub.
### 3. Añadir (si no lo habéis hecho ya) la clave pública que se corresponde a tu ordenador.
:+1:Hecho


## 2.23 USO SOCIAL DE GITHUB
### 1. Preguntar los nombres de usuario de GitHub de tus compañeros de clase, búscalos, y sigueles.
### 2. Seguir los repositorios campusciff del resto de tus compañeros.
### 3. Añadir una estrella a los repositorios campusciff del resto de tus compañeros.
:+1:Hecho


## 2.24 CREAR UNA TABLA
### 1. Crear una tabla de este estilo en el fichero README.md con la información de varios de tus compañeros de clase:

       
| NOMBRE 			| GITHUB 							|
| :----------------	|:----------------------------------|
| crisrodfra   		| <https://github.com/crisrodfra>   |
| ulisesojeda   	| <https://github.com/ulisesojeda>  |
| Alejandro Diaz	| <https://github.com/adiazgalache> |
| jaritgor   		| https://github.com/jaritgor   	|
| Pimateos   		| <https://github.com/Pimateos>   	|
| Carlos Paz   		| <https://github.com/cpazsantos>   |
| asuarezg   		| https://github.com/asuarezg   	|
| fjenriquez   		| https://github.com/fjenriquez   	|

			
				 
					       
## 2.25 COLABORADORES
### 1. Poner a github.com/asanzdiego como colaborador del repositorio campusciff

:+1: Hecho
![picture alt](/resources/Image5.png "Imagen5") 

## 2.26 CREAR UNA ORGANIZACIÓN
### 1. Crear una organización llamada campusciff-tunombredeusuariodegithub



## 2.27 CREAR EQUIPOS
### 1. Crear 2 equipos en la organización campusciff- tunombredeusuariodegithub, uno llamado administradores con más permisos y otro colaboradores con menos permisos.

:+1: Hecho


### 2. Meter a github.com/asanzdiego y a 2 de vuestros compañeros de clase en el equipo administradores.
:+1: Hecho
### 3. Meter a github.com/asanzdiego y a otros 2 de vuestros compañeros de clase en el equipo colaboradores.
:+1: Hecho


## 2.28 CREAR UN INDEX.HTML
### 1. Crear un index.html que se pueda ver como página web en la organización.

Se deben haber asignado permisos a los miembros del equipo para poder subir páginas (en este caso solo los administradores)

![picture alt](/resources/Image9.png "Imagen9") 


## 2.29 CREAR PULL-REQUESTS
### 1. Hacer 2 forks de 2 repositorios campusciff- tunombredeusuariodegithub.github.io de 2 organizaciones de las que no seais ni administradiores ni colaboradores.
## 2. Crearos una rama en cada fork.
## 3. En cada rama modificar el fichero index.html añadiendo vuestro nombre.
## 4. Con cada rama hacer un pull-request.

:+1: Hecho

![picture alt](/resources/Image10.jpg "Imagen10") 
![picture alt](/resources/Image11.jpg "Imagen11") 

## 2.30 GESTIONAR PULL-REQUESTS
### 1. Aceptar los pull-request que lleguen a los repositorios de tu organización.
:+1: Hecho
