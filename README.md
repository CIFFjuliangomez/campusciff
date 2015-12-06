# DATA SCIENCE TOOLKIT
## EJERCICIOS GIT, GITHUB Y MARKDOWN

Julián Gómez

![picture alt](https://dujk9xa5fr1wz.cloudfront.net/course/480x270/221696_d05a_4.jpg "DATA SCIENCE TOOLKIT") 

# 2.1 REPOSITORIO CAMPUSCIFF (I)
## 1. Crear un repositorio en vuestro GitHub llamado campusciff.

En la página web de github

![picture alt](https://dujk9xa5fr1wz.cloudfront.net/course/480x270/221696_d05a_4.jpg "Imagen1") 
![picture alt](https://dujk9xa5fr1wz.cloudfront.net/course/480x270/221696_d05a_4.jpg "Imagen2") 


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
Notas: en este documento tendreís que ir poniendo los comandos que habéis tenido que utilizar durante todos los ejercicios y las explicaciones y capturas de pantalla que consideréis necesarias.
  
  Ya creado al inicio :+1:
  
## 2.4 COMMIT INICIAL
#### 1. Añadir al README.md los comandos utilizados hasta ahora y hacer un commit inicial con el mensaje commit inicial.


```
MacBook-Pro-de-Julian:campusciff jgomez$ git add .
MacBook-Pro-de-Julian:campusciff jgomez$ git commit -m "commit inicial"
[master d079fdc] commit inicial
 1 file changed, 24 insertions(+), 2 deletions(-)
 rewrite README.md (82%)
MacBook-Pro-de-Julian:campusciff jgomez$ 
