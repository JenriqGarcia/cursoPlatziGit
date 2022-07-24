Paso a paso para subir proyecto a repositorio nuevo

-- 1 Se agrega el repositorio remoto
$ git remote add origin (URL)

-- 2 Verificar que la URL se haya guardado:
$ git remote
$ git remote -v

-- 3 Traemos la versión del repositorio remoto y hacemos merge para crear un commit con los archivos de ambas partes.
Podemos usar git fecth y git merge o solo lo siguiente:
$ git pull origin main --allow-unrelated-histories

-- 4 Ahora sí podemos hacer git push para guardar los cambios de nuestro repositorio local y en repositorio remoto
$ git push origin main


##Notas SSH
*** Crear llave ssh con rsa o con ed25519
ssh-keygen -t rsa -b 4096 -C "email@example.com"
ssh-keygen -t ed25519 -C "email@example.com"

**Para agregar llave ssh
eval $(ssh-agent -s)
ssh-add ~/.ssh/id_rsa

**cambiar passphrase de la llave ssh, para removerla se usa lo mismo pero se "cambia" a una contraseña vacia
ssh-keygen -p 


##Notas LOG
git log

**arbol de ramas
git log --all --graph --decorate --oneline

**crear alias de git
git config alias.arbolito "log --all --graph --decorate --oneline"

**commits por persona
git shortlog

**quien modifico las lineas de codigo indecadas
git blame nombre-archivo.txt -L35,50 -c         //muestra de la linea 35 a la 50 del archivo nombre-archivo.txt 

##Notas generales
**Borrar archivos no deseados
git clean --dry-run        //Te dise cuales se van a borrar

git clean -f            //ejecutar el borrado


##Buscar entre archivos
git grep -n busqueda                 // -n nos dice en que linea
git grep -c busqueda                 // -c nos dice cuantas veces aparece

##Ramas
git branch          //ver ramas locales
git branch -r        //ver ramas remotas
git branch -a         //ver todas ramas
