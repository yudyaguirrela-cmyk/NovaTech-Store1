# NovaTech-Store1
NovaTech Store es una tienda virtual desarrollada para la administración de productos tecnológicos. La aplicación permite visualizar un catálogo de productos y cuenta con un panel administrativo desde el cual es posible registrar, consultar y eliminar productos almacenados en una base de datos MySQL.
3. Objetivo del proyecto

Desarrollar una aplicación web que permita gestionar productos tecnológicos mediante una arquitectura cliente-servidor, utilizando HTML, CSS, Bootstrap, JavaScript, Node.js, Express y MySQL, fortaleciendo los conocimientos adquiridos durante el proceso de formación.

4. Tecnologías utilizadas

Frontend

HTML5
CSS3
Bootstrap 5
JavaScript

Backend

Node.js
Express.js

Base de datos

MySQL

Herramientas de desarrollo

Visual Studio Code
MySQL Workbench
Git y GitHub
Live Server
5. Estructura del proyecto
NovaTech-Store
│
├── backend
│   ├── config
│   │   └── conexion.js
│   ├── node_modules
│   ├── package.json
│   └── server.js
│
├── frontend
│   ├── css
│   │   └── estilos.css
│   ├── js
│   │   ├── auth.js
│   │   ├── login.js
│   │   └── productos.js
│   ├── index.html
│   ├── productos.html
│   ├── contacto.html
│   ├── ayuda.html
│   ├── login.html
│   └── admin-productos.html
│
└── README.md
6. Instrucciones de instalación y ejecución
1. Clonar el repositorio
git clone URL_DEL_REPOSITORIO

Entrar a la carpeta del proyecto

cd NovaTech-Store
2. Instalar las dependencias

Entrar a la carpeta backend

cd backend

Instalar las dependencias

npm install
3. Configurar la base de datos

Abrir MySQL Workbench y ejecutar:

CREATE DATABASE novatech_store;
4. Crear las tablas

Crear la tabla productos

CREATE TABLE productos (
id INT AUTO_INCREMENT PRIMARY KEY,
nombre VARCHAR(100) NOT NULL,
descripcion TEXT NOT NULL,
precio DECIMAL(10,2) NOT NULL,
categoria VARCHAR(50) NOT NULL,
stock INT NOT NULL,
imagen VARCHAR(255) NOT NULL
);

Crear la tabla usuarios

CREATE TABLE usuarios (
id INT AUTO_INCREMENT PRIMARY KEY,
usuario VARCHAR(50) UNIQUE,
contraseña VARCHAR(100)
);
5. Configurar la conexión

Editar el archivo

backend/config/conexion.js

Verificar los siguientes datos:

const conexion = mysql.createConnection({
    host: "localhost",
    port: 3307,
    user: "novatech",
    password: "123456",
    database: "novatech_store"
});

Nota: Si el puerto, usuario o contraseña de MySQL son diferentes, deben modificarse en este archivo.

6. Ejecutar el servidor

Desde la carpeta backend ejecutar:

node server.js

Debe aparecer el siguiente mensaje:

Servidor ejecutándose en http://localhost:3000
Conexión exitosa con MySQL
7. Ejecutar el Frontend

Abrir la carpeta frontend con Visual Studio Code.

Ejecutar la página utilizando la extensión Live Server.

También se puede abrir directamente el archivo index.html en el navegador.

7. Funcionalidades implementadas

La aplicación cuenta con las siguientes funcionalidades:

Página principal
Presentación de NovaTech Store.
Menú de navegación.
Diseño responsive.
Catálogo de productos
Visualización de productos tecnológicos.
Información de cada producto.
Botón de compra.
Contacto
Formulario de contacto.
Inicio de sesión
Acceso al panel administrativo.
Panel administrador
Registrar productos.
Consultar productos.
Eliminar productos.
Actualización automática de la tabla después de cada operación.
8. Flujo de información

El flujo principal del proyecto funciona de la siguiente manera:

Usuario abre la aplicación
        ↓
Frontend envía una solicitud mediante Fetch API
        ↓
Node.js recibe la petición
        ↓
Express procesa la solicitud
        ↓
Se ejecuta la consulta SQL
        ↓
MySQL almacena o consulta la información
        ↓
Express responde al Frontend
        ↓
JavaScript actualiza la interfaz
Flujo para registrar un producto
Administrador diligencia el formulario
        ↓
JavaScript captura la información
        ↓
Se envía una petición POST
        ↓
Express recibe la información
        ↓
MySQL inserta el registro
        ↓
Se devuelve un mensaje de confirmación
        ↓
La tabla se actualiza automáticamente
Flujo para consultar productos
Se carga el panel administrador
        ↓
JavaScript realiza una petición GET
        ↓
Express consulta MySQL
        ↓
MySQL devuelve los registros
        ↓
La información se muestra en la tabla
Flujo para eliminar un producto
Administrador presiona Eliminar
        ↓
JavaScript envía una petición DELETE
        ↓
Express recibe la solicitud
        ↓
MySQL elimina el registro
        ↓
La tabla se actualiza automáticamente
9. Pruebas realizadas

Se realizaron pruebas para verificar el correcto funcionamiento del sistema.

Pruebas del servidor
Se verificó la conexión con MySQL.
Se comprobó el inicio del servidor Node.js.
Pruebas del panel administrador
Registro de nuevos productos.
Consulta de productos.
Eliminación de productos.
Actualización automática de la tabla.
Pruebas de la base de datos
Verificación de registros creados.
Verificación de eliminación de registros.
Confirmación de la información mediante MySQL Workbench.
Pruebas del Frontend
Navegación entre páginas.
Funcionamiento del formulario.
Visualización correcta del catálogo.
Diseño responsive.

12. Conclusión

NovaTech Store es una aplicación web desarrollada para la administración de productos tecnológicos. Durante el desarrollo del proyecto se integraron tecnologías como HTML, CSS, Bootstrap, JavaScript, Node.js, Express y MySQL, permitiendo la comunicación entre el frontend, el backend y la base de datos.

El sistema permite registrar, consultar y eliminar productos desde un panel administrativo, demostrando el funcionamiento de una arquitectura cliente-servidor y fortaleciendo los conocimientos adquiridos en desarrollo web y gestión de bases de datos.
