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