# Literatura Gestión

Sistema de gestión offline para literatura y apadrinamientos con control de inventario, ventas y reportes. Aplicación de escritorio multiplataforma desarrollada con PHP Desktop.

## ✨ Características

- **Gestión de Apadrinamientos**: Registro, seguimiento y finalización de ceremonias de apadrinamiento
- **Control de Inventario**: Gestión de stock, precios y códigos de barras con historial de cambios
- **Sistema de Ventas**: Registro de ventas con deudores y seguimiento de pagos
- **Reportes Avanzados**: Exportación a Excel (consolidado, apadrinamientos, ventas)
- **Sistema de Roles**: Admin/Superadmin y Ayudante con permisos diferenciados
- **Modo Offline**: Funciona completamente sin conexión a internet con SQLite
- **Autenticación Segura**: CSRF tokens y validación de sesiones

## 🛠 Tecnología

- **Backend**: PHP 7.4+
- **Base de Datos**: SQLite
- **Frontend**: JavaScript vanilla, HTML5, CSS3
- **Escritorio**: PHP Desktop (Chrome embedded)
- **Librerías**: PHPSpreadsheet (Excel), FontAwesome, SweetAlert2

## 🚀 Inicio Rápido

### Requisitos
- PHP Desktop (incluido en el proyecto)
- No requiere instalación de servidor web

### Instalación
1. Descargar o clonar el repositorio
2. Ejecutar `launcher.php` o hacer doble click en `php-desktop.ini`
3. La aplicación abrirá en modo offline

### Login
- **Admin**: Usuario/contraseña configurado en la BD
- **Ayudante**: Seleccionar nombre, estigma y grupo

## 📁 Estructura del Proyecto

```
www/
├── api/                    # Endpoints REST
│   ├── api_apadrinamiento.php
│   ├── api_inventario.php
│   ├── api_ventas.php
│   ├── api_reportes.php
│   └── ...
├── assets/
│   ├── js/
│   │   ├── app.js         # Lógica principal
│   │   ├── login.js
│   │   └── download-handler.js
│   ├── css/
│   │   └── style.css
│   └── img/
├── data/                  # Base de datos SQLite
├── index.php             # Login
├── dashboard.php         # Panel principal
└── config.php           # Configuración
```

## 📝 Permisos por Rol

### Admin/Superadmin
- ✅ Crear, editar y eliminar apadrinamientos
- ✅ Gestionar inventario (CRUD completo)
- ✅ Registrar ventas
- ✅ Ver reportes y exportar
- ✅ Administrar usuarios
- ✅ Ver salud del sistema

### Ayudante
- ✅ Ver historial de apadrinamientos
- ✅ Agregar y terminar apadrinamientos
- ✅ Ver inventario (solo lectura)
- ✅ Ver reportes

## 🔧 Configuración

Editar `config.php` para personalizar:
- Zona horaria
- Rutas de base de datos
- Mensajes del sistema

## 📊 Exportar Datos

- **Consolidado**: Reporte general en Excel
- **Apadrinamientos**: Detalle de ceremonias con quien las finalizó
- **Ventas**: Historial de transacciones
- **JSON**: Exportación en formato JSON

## 🐛 Solución de Problemas

Si la app no inicia:
1. Presionar F12 para ver la consola
2. Revisar `verify-and-fix.php` para diagnosticar
3. Ejecutar `force-init-db.php` para reiniciar la base de datos

## 📄 Licencia

MIT - Ver LICENSE.txt

## 👨‍💻 Autor

Adan Garcia L - [GitHub](https://github.com/AdanGarciaL)

---

**Última actualización**: Febrero 2026
