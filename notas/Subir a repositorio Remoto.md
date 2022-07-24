Paso a paso para subir proyecto a repositorio nuevo

-- 1 Se agrega el repositorio remoto
$ git remote add origin (URL)

-- 2 Verificar que la URL se haya guardado:
$ git remote
$ git remote -v

-- 3 Traemos la versión del repositorio remoto y hacemos merge para crear un commit con los archivos de ambas partes.
Podemos usar git fecth y git merge o solo lo siguiente:
$ git pull origin master --allow-unrelated-histories

-- 4 Ahora sí podemos hacer git push para guardar los cambios de nuestro repositorio local y en repositorio remoto
$ git push origin master


##Notas SSH
*** Crear llave ssh con rsa o con ed25519
ssh-keygen -t rsa -b 4096 -C "email@example.com"
ssh-keygen -t ed25519 -C "email@example.com"

**Para agregar llave ssh
eval $(ssh-agent -s)
ssh-add ~/.ssh/id_rsa

**cambiar passphrase de la llave ssh, para removerla se usa lo mismo pero se "cambia" a una contraseña vacia
ssh-keygen -p 

