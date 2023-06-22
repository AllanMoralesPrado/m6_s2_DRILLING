## Javascript FullStack Web Development
### Módulo 6, Sesión 2 - INTRODUCCIÓN AL GESTOR DE PAQUETES NPM

# DRILLING: RECORDANDO USO DE GIT 

### EJERCICIO

- Crea una nueva carpeta, e inicializa un nuevo repositorio de git.  
- Crea un archivo `.gitignore`, que omita la carpeta `node modules` al momento de subir cambios.  
- Busca en la web los paquetes más utilizados de npm, e instala los cinco primeros de la lista.  
- Haz un chequeo de los cambios en tu proyecto (git status) posterior a la instalación, agrega los cambios a git, y luego realiza un commit de estos cambios.  
- Elige dos paquetes de tu proyecto, y realiza una desinstalación.  
- Vuelve a realizar un chequeo de los cambios luego de la  desinstalación, añade los cambios, y guárdalos en el repositorio local de git.  
- ¿Puedes ver cuál es el archivo que cambia cada vez que realizas una instalación o desinstalación de paquetes? 

### DIVIDIENDO ARCHIVOS, INSTALANDO PAQUETES

Dados los siguientes Arrays: 

```JAVASCRIPT
let autos = ["mazda", "renault", "ferrari", "mazda", "jeep", "audi", "ferrari"];  
```

```JAVASCRIPT
let animales = [  
  {animal: 'perro', tipo: 'mascota', nombre: 'elvis'},  
  {animal: 'tigre', tipo: 'salvaje', nombre: 'hendrix'},  
  {animal: 'tiburon', tipo: 'salvaje', nombre: 'ray charles'},  
  {animal: 'gato', tipo: 'mascota', nombre: 'lady gaga'} 
 ];  
 ```
- Inicia un nuevo proyecto con npm init, e instala el paquete lodash (https://www.npmjs.com/package/lodash).
- Asegúrate de que la versión del paquete lodash en package.json sea la versión “^4.17.21”. 
- Crea un archivo `index.js`, y un archivo `datos.js`. 
- Agrega y exporta las variables autos y animales al archivo `datos.js`. 
- Importa las variables autos y animales dentro de tu archivo `index.js`. 
- Utiliza la documentación de *lodash* (https://lodash.com/docs/4.17.15) para requerir el paquete, e investiga cómo implementar los métodos `find()` y `uniq()`. 
- Utiliza el método `uniq()` para obtener un Array de elementos únicos desde la variable `autos`, y guarda el resultado en una variable en tu archivo `index.js`. 
- Utiliza  el  metod  `find()`  para  obtener  todos  los  animales  de  tipo  salvaje  de  la  variable `animales`, y guarda el resultado en una variable en tu archivo `index.js`. 
- Muestra por consola el resultado contenido en las variables creadas.

### SOLUCIÓN

1. Crear repositorio git en un directorio
```
git init
```
2. Crear archivo `.gitignore`
```
- en cmd -
copy nul ".gitignore"

- en bash -
touch .gitignore
```
3. Instalar Top 5 paquetes npm: 
```
npm init
npm i loadsh express react axios moment
```
4. Se acaba de crear la carpeta `node_modules` configurar el archivo `.gitignore` para ignorarlo en el control de versiones, agregando lo siguiente:
```
# Ignorar archivos y directorios generados automáticamente

node_modules/
```
5. Comprobar estado del proyecto:
```
git status
```
RESULTADO
```
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        .gitignore
        README.md
        package-lock.json
        package.json

nothing added to commit but untracked files present (use "git add" to track)
```
6. Agregar cambios y realizar el commit:
```
git add -A && git commit -m "loadsh express react axios y moment"
```
RESULTADO
```
warning: LF will be replaced by CRLF in package-lock.json.
The file will have its original line endings in your working directory
warning: LF will be replaced by CRLF in package.json.
The file will have its original line endings in your working directory
[master (root-commit) ff532ad] loadsh express react axios y moment
 4 files changed, 815 insertions(+)
 create mode 100644 .gitignore
 create mode 100644 README.md
 create mode 100644 package-lock.json
 create mode 100644 package.json
```