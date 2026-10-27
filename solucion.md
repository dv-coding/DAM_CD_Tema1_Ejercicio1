# Tema 1: Git

## Ejercicio 1 — Primer repositorio Git

**Enlace al repositorio:** [https://github.com/dv-coding/DAM_CD_Tema1_Ejercicio1](https://github.com/dv-coding/DAM_CD_Tema1_Ejercicio1)

**Salida del terminal:**

```bash
dev@VM-W11DEV UCRT64 ~
$ cd c:

dev@VM-W11DEV UCRT64 /c
$ cd DAM

dev@VM-W11DEV UCRT64 /c/DAM
$ cd ED

dev@VM-W11DEV UCRT64 /c/DAM/ED
$ ls
CD_Tema1_Ejercicio1/

dev@VM-W11DEV UCRT64 /c/DAM/ED
$ cd CD_Tema1_Ejercicio1/

dev@VM-W11DEV UCRT64 /c/DAM/ED/CD_Tema1_Ejercicio1
$ mkdir biblioteca && cd biblioteca

dev@VM-W11DEV UCRT64 /c/DAM/ED/CD_Tema1_Ejercicio1/biblioteca
$ git init -b main
Initialized empty Git repository in C:/DAM/ED/CD_Tema1_Ejercicio1/biblioteca/.git/

dev@VM-W11DEV UCRT64 /c/DAM/ED/CD_Tema1_Ejercicio1/biblioteca (main)
$ echo '# Biblioteca' > README.md && echo 'Proyecto de gestión libros y lectores' >> README.md

dev@VM-W11DEV UCRT64 /c/DAM/ED/CD_Tema1_Ejercicio1/biblioteca (main)
$ git add README.md
warning: in the working copy of 'README.md', LF will be replaced by CRLF the next time Git touches it

dev@VM-W11DEV UCRT64 /c/DAM/ED/CD_Tema1_Ejercicio1/biblioteca (main)
$ git commit -m 'Se añade fichero README con nombre y descripción del proyecto'
[main (root-commit) 6dce8fc] Se añade fichero README con nombre y descripción del proyecto
 1 file changed, 2 insertions(+)
 create mode 100644 README.md

dev@VM-W11DEV UCRT64 /c/DAM/ED/CD_Tema1_Ejercicio1/biblioteca (main)
$ printf 'Thumbs.db\n.DS_Store\n*.tmp\n*.log\n.env\n' > .gitignore

dev@VM-W11DEV UCRT64 /c/DAM/ED/CD_Tema1_Ejercicio1/biblioteca (main)
$ git add .gitignore
warning: in the working copy of '.gitignore', LF will be replaced by CRLF the next time Git touches it

dev@VM-W11DEV UCRT64 /c/DAM/ED/CD_Tema1_Ejercicio1/biblioteca (main)
$ git commit -m 'Se añade fichero .gitignore para ficheros temporales, logs, variables de entorno'
[main 9223e15] Se añade fichero .gitignore para ficheros temporales, logs, variables de entorno
 1 file changed, 5 insertions(+)
 create mode 100644 .gitignore

dev@VM-W11DEV UCRT64 /c/DAM/ED/CD_Tema1_Ejercicio1/biblioteca (main)
$ mkdir datos && cd datos

dev@VM-W11DEV UCRT64 /c/DAM/ED/CD_Tema1_Ejercicio1/biblioteca/datos (main)
$ echo 'Notas iniciales del proyecto' > notas.txt

dev@VM-W11DEV UCRT64 /c/DAM/ED/CD_Tema1_Ejercicio1/biblioteca/datos (main)
$ git add notas.txt
warning: in the working copy of 'datos/notas.txt', LF will be replaced by CRLF the next time Git touches it

dev@VM-W11DEV UCRT64 /c/DAM/ED/CD_Tema1_Ejercicio1/biblioteca/datos (main)
$ cd ..

dev@VM-W11DEV UCRT64 /c/DAM/ED/CD_Tema1_Ejercicio1/biblioteca (main)
$ git commit -m 'Se añade carpeta datos con el fichero notas.txt'
[main ffc1a04] Se añade carpeta datos con el fichero notas.txt
 1 file changed, 1 insertion(+)
 create mode 100644 datos/notas.txt

dev@VM-W11DEV UCRT64 /c/DAM/ED/CD_Tema1_Ejercicio1/biblioteca (main)
$ git remote add origin https://github.com/dv-coding/DAM_CD_Tema1_Ejercicio1.git

dev@VM-W11DEV UCRT64 /c/DAM/ED/CD_Tema1_Ejercicio1/biblioteca (main)
$ git push -u origin main
info: please complete authentication in your browser...
Enumerating objects: 10, done.
Counting objects: 100% (10/10), done.
Delta compression using up to 2 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (10/10), 950 bytes | 237.00 KiB/s, done.
Total 10 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/dv-coding/DAM_CD_Tema1_Ejercicio1.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.

dev@VM-W11DEV UCRT64 /c/DAM/ED/CD_Tema1_Ejercicio1/biblioteca (main)
$ git push -u origin main
branch 'main' set up to track 'origin/main'.
Everything up-to-date

dev@VM-W11DEV UCRT64 /c/DAM/ED/CD_Tema1_Ejercicio1/biblioteca (main)
$ git log --oneline
ffc1a04 (HEAD -> main, origin/main) Se añade carpeta datos con el fichero notas.txt
9223e15 Se añade fichero .gitignore para ficheros temporales, logs, variables de entorno
6dce8fc Se añade fichero README con nombre y descripción del proyecto
```

## Ejercicio 2 — Trabajo con ramas

**Enlace al repositorio:** [https://github.com/dv-coding/DAM_CD_Tema1_Ejercicio1](https://github.com/dv-coding/DAM_CD_Tema1_Ejercicio1)

**Salida del terminal:**

```bash
dev@VM-W11DEV UCRT64 /c/DAM/ED/CD_Tema1_Ejercicio1/biblioteca (main)
$ git switch -c feature/gestion-libros
Switched to a new branch 'feature/gestion-libros'

dev@VM-W11DEV UCRT64 /c/DAM/ED/CD_Tema1_Ejercicio1/biblioteca (feature/gestion-libros)
$ echo 'Título: Cien años de soledad' > libros.txt

dev@VM-W11DEV UCRT64 /c/DAM/ED/CD_Tema1_Ejercicio1/biblioteca (feature/gestion-libros)
$ git mv libros.txt libro.txt
fatal: not under version control, source=libros.txt, destination=libro.txt

dev@VM-W11DEV UCRT64 /c/DAM/ED/CD_Tema1_Ejercicio1/biblioteca (feature/gestion-libros)
$ ls
datos/  libros.txt  README.md  solucion.md

dev@VM-W11DEV UCRT64 /c/DAM/ED/CD_Tema1_Ejercicio1/biblioteca (feature/gestion-libros)
$ mv libros.txt libro.txt

dev@VM-W11DEV UCRT64 /c/DAM/ED/CD_Tema1_Ejercicio1/biblioteca (feature/gestion-libros)
$ ls
datos/  libro.txt  README.md  solucion.md

dev@VM-W11DEV UCRT64 /c/DAM/ED/CD_Tema1_Ejercicio1/biblioteca (feature/gestion-libros)
$ git add libro.txt
warning: in the working copy of 'libro.txt', LF will be replaced by CRLF the next time Git touches it

dev@VM-W11DEV UCRT64 /c/DAM/ED/CD_Tema1_Ejercicio1/biblioteca (feature/gestion-libros)
$ git commit -m 'Se añade fichero libro.txt con el título de un libro'
[feature/gestion-libros e28037e] Se añade fichero libro.txt con el título de un libro
 1 file changed, 1 insertion(+)
 create mode 100644 libro.txt

dev@VM-W11DEV UCRT64 /c/DAM/ED/CD_Tema1_Ejercicio1/biblioteca (feature/gestion-libros)
$ printf 'Autor: Gabriel García Márquez\nisbn: 978-0307474728\n' >> libro.txt

dev@VM-W11DEV UCRT64 /c/DAM/ED/CD_Tema1_Ejercicio1/biblioteca (feature/gestion-libros)
$ git add libro.txt
warning: in the working copy of 'libro.txt', LF will be replaced by CRLF the next time Git touches it

dev@VM-W11DEV UCRT64 /c/DAM/ED/CD_Tema1_Ejercicio1/biblioteca (feature/gestion-libros)
$ git commit -m 'Se añade autor e isbn del libro al fichero libro.txt'
[feature/gestion-libros 1c22fa4] Se añade autor e isbn del libro al fichero libro.txt
 1 file changed, 2 insertions(+)

dev@VM-W11DEV UCRT64 /c/DAM/ED/CD_Tema1_Ejercicio1/biblioteca (feature/gestion-libros)
$ git switch main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

dev@VM-W11DEV UCRT64 /c/DAM/ED/CD_Tema1_Ejercicio1/biblioteca (main)
$ git switch -c feature/gestion-usuarios
Switched to a new branch 'feature/gestion-usuarios'

dev@VM-W11DEV UCRT64 /c/DAM/ED/CD_Tema1_Ejercicio1/biblioteca (feature/gestion-usuarios)
$ echo 'Nombre: Laura Gómez' > usuario.txt

dev@VM-W11DEV UCRT64 /c/DAM/ED/CD_Tema1_Ejercicio1/biblioteca (feature/gestion-usuarios)
$ git add usuario.txt
warning: in the working copy of 'usuario.txt', LF will be replaced by CRLF the next time Git touches it

dev@VM-W11DEV UCRT64 /c/DAM/ED/CD_Tema1_Ejercicio1/biblioteca (feature/gestion-usuarios)
$ git commit -m 'Se añade un usuario al fichero usuario.txt'
[feature/gestion-usuarios 39b9971] Se añade un usuario al fichero usuario.txt
 1 file changed, 1 insertion(+)
 create mode 100644 usuario.txt

dev@VM-W11DEV UCRT64 /c/DAM/ED/CD_Tema1_Ejercicio1/biblioteca (feature/gestion-usuarios)
$ printf 'Email: laura.gomez@gmail.com\nContraseña: ClaveSegura2026\n' >> usuario.txt

dev@VM-W11DEV UCRT64 /c/DAM/ED/CD_Tema1_Ejercicio1/biblioteca (feature/gestion-usuarios)
$ git commit -am 'Se añade email y contraseña del usuario en el fichero usuario.txt'
warning: in the working copy of 'usuario.txt', LF will be replaced by CRLF the next time Git touches it
[feature/gestion-usuarios c6e7aa9] Se añade email y contraseña del usuario en el fichero usuario.txt
 1 file changed, 2 insertions(+)

dev@VM-W11DEV UCRT64 /c/DAM/ED/CD_Tema1_Ejercicio1/biblioteca (feature/gestion-usuarios)
$ git switch main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

dev@VM-W11DEV UCRT64 /c/DAM/ED/CD_Tema1_Ejercicio1/biblioteca (main)
$ git merge --no-ff feature/gestion-libros -m 'Merge branch feature/gestion-libros'
Merge made by the 'ort' strategy.
 libro.txt | 3 +++
 1 file changed, 3 insertions(+)
 create mode 100644 libro.txt

dev@VM-W11DEV UCRT64 /c/DAM/ED/CD_Tema1_Ejercicio1/biblioteca (main)
$ git merge feature/gestion-usuarios -m 'Merge branch feature/gestion-usuarios'
Merge made by the 'ort' strategy.
 usuario.txt | 3 +++
 1 file changed, 3 insertions(+)
 create mode 100644 usuario.txt

dev@VM-W11DEV UCRT64 /c/DAM/ED/CD_Tema1_Ejercicio1/biblioteca (main)
$ git push --all origin
Enumerating objects: 16, done.
Counting objects: 100% (16/16), done.
Delta compression using up to 2 threads
Compressing objects: 100% (13/13), done.
Writing objects: 100% (15/15), 1.60 KiB | 328.00 KiB/s, done.
Total 15 (delta 5), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (5/5), completed with 1 local object.
To https://github.com/dv-coding/DAM_CD_Tema1_Ejercicio1.git
   6d7d84f..676bc19  main -> main
 * [new branch]      feature/gestion-libros -> feature/gestion-libros
 * [new branch]      feature/gestion-usuarios -> feature/gestion-usuarios

dev@VM-W11DEV UCRT64 /c/DAM/ED/CD_Tema1_Ejercicio1/biblioteca (main)
$ git log --oneline --graph --all
*   676bc19 (HEAD -> main, origin/main) Merge branch feature/gestion-usuarios
|\
| * c6e7aa9 (origin/feature/gestion-usuarios, feature/gestion-usuarios) Se añade email y contraseña del usuario en el fichero usuario.txt
| * 39b9971 Se añade un usuario al fichero usuario.txt
* |   433e11c Merge branch feature/gestion-libros
|\ \
| |/
|/|
| * 1c22fa4 (origin/feature/gestion-libros, feature/gestion-libros) Se añade autor e isbn del libro al fichero libro.txt
| * e28037e Se añade fichero libro.txt con el título de un libro
|/
* 6d7d84f Se añade fichero solucion.md con el log del ejercicio 1
* ffc1a04 Se añade carpeta datos con el fichero notas.txt
* 9223e15 Se añade fichero .gitignore para ficheros temporales, logs, variables de entorno
* 6dce8fc Se añade fichero README con nombre y descripción del proyecto
````