# Comandos importantes para Git

#### Inicia un repositorio vacio en la carpeta donde tengas un proyecto:
	git init

#### Para ver archivos editados:
	git status

#### Para agregar todos los archivos (el punto selecciona todos los archivos excluyendo los del .gitignore):
	git add .

#### Con lo que se publica el commit (mensaje de que cambio se hizo):
	git commit -m "<mensaje de commit>"

#### Sincronizar tu proyecto con github
	- Nota este debe de haber sido creado anteriormente en github
		git remote add origin https://github.com/tuUsuario/your-repo-name.git

#### Descarga todos los cambios del repositorio si es que hubo:
	git pull

##### Si no tienes conflictos 

#### Actualizar tu copia del repositorio (este se usa si es que hiciste un fork a otro repositorio): 
	- Primero debes hacer fetch al repositorio original
		git fetch upstream
	- Despues cambiarte a la rama master y hacer un rebase o merge
		git checkout master
		git merge upstream/master
	- Y a lo ultimo hacer un rebase
		git rebase master

#### Hacer un rebase:
	git rebase master

#### Para subir tus archivos (si falla meter el flag --force):
	git push origin master

###### Para hacerlo en otra branch:
	-Primero cambiarte a ella:
		git checkout miNuevaRama
	-Depues hacer push
		git push origin miNuevaRama

#### Agregar un repositorio remoto (este se usa si es que hiciste un fork a otro repositorio y trabajas en el fork):
	git remote add upstream https://github.com/nombreUsuario/nombreRep.git

###### Para verificar tu repositorio (Para ver tu origin (tu repositorio) y el upstream (ver el repo remoto))
	git remote -v

#### Crear una branch en tu repositorio:
	- Primero tienes que estar en tu rama master porque de ahi es donde vas a sacar tu nueva rama
		git checkout master
	- Despues ya creamos tu nueva rama
		git branch miNuevaRama
	- Y por ultimo nos cambiamos a ella
		git checkout miNuevaRama

#### Cambiarte de branch:
	git checkout miNuevaRama

#### Clonar un repositorio
	git clone https://github.com/tuUsuario/your-repo-name.git

###### Clonar con ssh:
	git clone git@github.com:tuUsuario/your-repo-name.git

### Si buscas hacer un Pull Request se hace en github
- El primer paso seria irte a tu branch
- Luego darle al boton de 'New pull request'
- Despues Te saldrá esta ventana, la llenas diciendo tu trabajo y asegurandote que en base sea el repositorio original y listo!

#### Comandos rapidos 
	echo "# LearningGit" >> README.md
	git init
	git add README.md
	git commit -m "first commit"
	git branch -M master
	git remote add origin git@github.com:MJVNOR/LearningGit.git
	git push -u origin master