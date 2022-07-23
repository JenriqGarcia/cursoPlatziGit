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