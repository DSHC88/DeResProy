# **DELILAH RESTÓ**.

**Esta api maneja el inventario de tu restaurante.**

Esta api se conecta con MySQL para la base de datos y te permite controlar el inventario de tu restaurante.
Caracteristicas:
- Registro e inicio de sesión de usuarios.
- Validación de roles (administrador o no)
- Funciones CRUD de los productos
- Funciones CRUD de pedidos
## Especificaciones OPEN API
- [Open API Docs](/spec.yml)
### Clona el repo:
```
$ git clone https://github.com/DSHC88/DeResProy.git
```
### Instala las dependencias:
```
$ npm install
```
#### Auto set up:
- Correr el MySQL server.
- Crear una base de datos desde MySQL usando el cmd o la utilidad de escritorio.
- Abrir el archivo `config.js` (`db/sequelize/config.js`) donde debes editar:
  1. el host y el puerto de la base de datos.
  2. Nombre de la base de datos.
  3. Usuario y contraseña para la coneccion.
```
$ cd db/db-setup
$ node index.js
```
Esto creará el esquema de la base de datos, las tablas e importará datos de ejemplo de usuarios y productos. Puede **edit** información de ejemplo reemplazando los archivos `products.csv` y / o `users.csv` en `db / datasets`
#### Manual Setup:
Si la configuración automática falla, puede hacer lo siguiente:
1. Inicialice el servidor MySQL.
2. Cree la base de datos llamada **delilah_resto** desde la línea de comandos o la utilidad de escritorio.
3. Cree el esquema y las tablas, e inserte los datos manualmente, usando las _queries_ existentes en `dbcreadors.sql`.
Antes de comenzar a usar el servidor, no olvide editar el archivo `config.js` (` db / sequelize / config.js`) con:
1. Host y puerto de la base de datos al que debe conectarse la API
2. Nombre de la base de datos.
3. Usuario y contraseña de la base de datos para conectarse.
## Run the API
```
$ cd server
$ node index.js
```