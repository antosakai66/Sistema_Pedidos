# Sistema de Pedidos

Proyecto básico para gestionar pedidos y productos de una pequeña aplicación web. La estructura actual incluye una base de datos en MySQL y una interfaz frontend en HTML estático.

## Descripción

Este sistema está pensado para:

- Registrar productos con nombre, descripción, precio y cantidad.
- Gestionar la parte visual de la aplicación con páginas HTML.
- Iniciar sesión desde una interfaz de login.
- Servir como base para ampliar la funcionalidad del sistema de pedidos.

## Estructura del proyecto

```text
SistPedidos/
├── BACKEND/
│   └── Productos.sql
├── FRONTEND/
│   ├── index.html
│   ├── interfazProducto.hmtl
│   ├── login.html
│   └── Users.html
├── .gitIgnore
├── readme.md
└── .git/
```

## Archivos principales

- `BACKEND/Productos.sql`: Script SQL para crear la tabla de productos.
- `FRONTEND/login.html`: Vista de inicio de sesión.
- `FRONTEND/index.html`: Página principal de la interfaz.
- `FRONTEND/interfazProducto.hmtl`: Vista de productos o interfaz de administración.
- `FRONTEND/Users.html`: Vista para usuarios.

## Base de datos

El script SQL crea la siguiente tabla:

```sql
CREATE TABLE IF NOT EXISTS PRODUCTOS (
    ID_PRODUCTO INT PRIMARY KEY AUTO_INCREMENT,
    NOMBRE VARCHAR(50) NOT NULL,
    DESCRIPCION VARCHAR(100) NOT NULL,
    PRECIO DECIMAL(10,2) NOT NULL,
    CANTIDAD INT NOT NULL
);
```

## Requisitos

- MySQL o MariaDB
- Navegador web
- Editor de código (opcional)

## Instalación

1. Crear una base de datos en MySQL.
2. Importar el archivo `BACKEND/Productos.sql`.
3. Abrir los archivos HTML dentro de la carpeta `FRONTEND` en el navegador.

Ejemplo de importación:

```bash
mysql -u tu_usuario -p tu_base_de_datos < BACKEND/Productos.sql
```

## Ejecutar la interfaz

Puedes abrir los archivos directamente en el navegador o servir la carpeta frontend localmente con un servidor simple:

```bash
cd FRONTEND
python -m http.server 8000
```

Luego accede en el navegador a:

```text
http://localhost:8000
```

## Estado actual

El proyecto se encuentra en una etapa inicial y tiene la estructura base para continuar con el desarrollo de la lógica del sistema, autenticación, gestión de ventas y administración de productos.

## Futuras mejoras

- Login funcional con validación de usuarios.
- CRUD de productos.
- Gestión de pedidos.
- Conexión con base de datos mediante PHP, Node.js o Java.
- Panel administrativo.

## Autor

Proyecto desarrollado para práctica y evolución de un sistema de pedidos.
