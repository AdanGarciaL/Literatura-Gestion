# 📚 Literatura V1 - Gestión Offline

Sistema de gestión offline para literatura y apadrinamientos con control de inventario, ventas y reportes. Aplicación de escritorio multiplataforma desarrollada con PHP Desktop.

---

## 🎯 Descarga la Aplicación

### 📥 **Descargar Instalador V1.0.0**

> **Versión**: 1.0.0 | **Tamaño**: 164.53 MB | **Estado**: ✅ Listo para Producción

[![Descargar Literatura V1](https://img.shields.io/badge/📥%20Descargar%20Instalador-v1.0.0-green?style=for-the-badge&logo=windows&logoColor=white)](https://github.com/AdanGarciaL/Literatura-Gestion/releases/download/v1.0.0/Literatura-V1-Setup-1.0.0.exe)

**O descarga desde**: [Releases → v1.0.0](https://github.com/AdanGarciaL/Literatura-Gestion/releases/tag/v1.0.0)

---

## 💻 Requisitos del Sistema

### Mínimos
| Requisito | Especificación |
|-----------|---|
| **Sistema Operativo** | Windows 7 SP1 o superior |
| **Memoria RAM** | 2 GB mínimo |
| **Espacio en Disco** | 500 MB disponibles |
| **Procesador** | Intel/AMD dual-core 1.5 GHz |

### Recomendados
| Requisito | Especificación |
|-----------|---|
| **Sistema Operativo** | Windows 10 o Windows 11 |
| **Memoria RAM** | 4 GB o más |
| **Espacio en Disco** | 1 GB disponibles |
| **Procesador** | Intel/AMD quad-core 2.0 GHz |

### Dependencias
- ✅ **Visual C++ Redistributable 2022** - Se ofrece instalar automáticamente
- ✅ **Chromium Embedded Framework** - Incluido en el instalador
- ✅ **PHP 7.4+** - Incluido en el instalador
- ✅ **.NET Framework** - Opcional (para algunas funciones avanzadas)

---

## 🚀 Instalación Rápida

### Paso 1: Descargar
[![Descargar Instalador](https://img.shields.io/badge/Descargar%20Literatura--V1--Setup--1.0.0.exe-164.53%20MB-blue?style=plastic)](https://github.com/AdanGarciaL/Literatura-Gestion/releases/download/v1.0.0/Literatura-V1-Setup-1.0.0.exe)

### Paso 2: Ejecutar
1. Localiza el archivo descargado: `Literatura-V1-Setup-1.0.0.exe`
2. Haz doble clic para iniciar el instalador
3. Se abrirá el asistente de instalación

### Paso 3: Configurar
Durante la instalación, selecciona:
- ☑ **Crear ícono en escritorio** - Acceso rápido
- ☑ **Ejecutar siempre como Administrador** - RECOMENDADO
- ☑ **Instalar Visual C++ Redistributable 2022** - RECOMENDADO

### Paso 4: Completar
- Elige la carpeta de instalación (por defecto: `C:\Program Files\Literatura V1`)
- Haz clic en "Instalar"
- Espera a que termine (puede tomar unos minutos)
- ¡Listo! La aplicación está instalada

### Paso 5: Ejecutar
- Abre el ícono de "Literatura V1" en tu escritorio
- O busca la aplicación en el menú Inicio de Windows
- ¡Comienza a usar!

---

## ✨ Características Principales

### 📋 Gestión de Apadrinamientos
- Registro completo de apadrinamientos
- Seguimiento de ceremonias
- Finalización y confirmación
- Historial detallado

### 📦 Control de Inventario
- Gestión de stock
- Precios y códigos de barras
- Historial de cambios
- Búsqueda y filtrado avanzado

### 💳 Sistema de Ventas
- Registro de transacciones
- Gestión de deudores
- Seguimiento de pagos
- Reportes de ventas

### 📊 Reportes Avanzados
- Exportación a Excel
- Consolidado de datos
- Reportes por periodo
- Análisis de inventario

### 🔐 Seguridad
- Autenticación segura
- Sistema de roles (Admin/Ayudante)
- CSRF tokens
- Validación de sesiones

### 🌐 Funcionalidad Offline
- **Completamente offline** - Sin necesidad de internet
- Base de datos SQLite local
- Sincronización manual opcional
- Modo avión compatible

---

## 🛠 Tecnología

- **Backend**: PHP 7.4+
- **Base de Datos**: SQLite
- **Frontend**: JavaScript vanilla, HTML5, CSS3
- **Escritorio**: PHP Desktop (Chrome embedded)
- **Librerías**: PHPSpreadsheet, FontAwesome, SweetAlert2

---

## 📁 Estructura del Proyecto

```
Literatura V1/
├── Literatura.exe              # Ejecutable principal
├── php/                        # Motor PHP incluido
├── www/                        # Aplicación web
│   ├── api/                    # Endpoints REST
│   ├── assets/                 # CSS, JS, imágenes
│   ├── data/                   # Base de datos SQLite
│   ├── index.php              # Login
│   ├── dashboard.php          # Panel principal
│   └── config.php             # Configuración
├── locales/                    # Localizaciones multiidioma
└── LICENSE.txt                 # Licencia de uso
```

---

## 🔑 Permisos por Rol

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

---

## 📝 Inicio de Sesión

### Primera Sesión
1. Ejecuta la aplicación
2. Usa las credenciales predeterminadas
3. Cambia la contraseña desde configuración

### Roles Disponibles
- **Admin**: Acceso completo a todas las funciones
- **Ayudante**: Funciones limitadas para asistentes

---

## 💾 Exportar y Respaldar

### Formatos Soportados
- 📊 **Excel (.xlsx)** - Consolidado, apadrinamientos, ventas
- 📄 **PDF** - Reportes imprimibles
- 📋 **CSV** - Datos tabulares
- 🔗 **JSON** - Integración con otros sistemas

### Crear Respaldos
1. Accede a Configuración → Respaldos
2. Haz clic en "Crear respaldo"
3. Guarda el archivo en un lugar seguro
4. Restaura cuando sea necesario

---

## 🐛 Solución de Problemas

### La aplicación no inicia
1. Verifica los requisitos del sistema
2. Asegúrate de tener permisos de Administrador
3. Instala Visual C++ Redistributable 2022
4. Reinicia tu computadora

### Error de base de datos
1. Accede a Configuración → Diagnóstico
2. Haz clic en "Verificar base de datos"
3. Si es necesario, restablece la base de datos
4. Restaura desde un respaldo si es necesario

### Problemas de rendimiento
1. Aumenta la memoria RAM asignada (si es posible)
2. Cierra otras aplicaciones
3. Vacía la caché desde Configuración
4. Contacta al soporte técnico

---

## 📧 Soporte y Contacto

- 🐛 **Reportar un bug**: [Issues](https://github.com/AdanGarciaL/Literatura-Gestion/issues)
- 💬 **Sugerencias**: [Discussions](https://github.com/AdanGarciaL/Literatura-Gestion/discussions)
- 📞 **Soporte técnico**: Contacta a través de GitHub

---

## 📜 Licencia

**MIT License** - Ver [LICENSE.txt](LICENSE.txt) para más detalles.

---

## 🙏 Créditos

Desarrollado por **Adan Garcia L**  
GitHub: [@AdanGarciaL](https://github.com/AdanGarciaL)

---

## 📅 Changelog

### Versión 1.0.0 - Febrero 2026
- ✅ Primera versión release
- ✅ Instalador con permisos de Administrador
- ✅ Opción de instalación de Visual C++ Redistributable
- ✅ Interfaz multiidioma (Español/Inglés)
- ✅ Completamente offline

[Ver todas las versiones →](CHANGELOG.md)

---

<div align="center">

### ⭐ ¿Te resultó útil? Por favor, dale una estrella ⭐

[Descargar Ahora](https://github.com/AdanGarciaL/Literatura-Gestion/releases/download/v1.0.0/Literatura-V1-Setup-1.0.0.exe) | [Documentación Completa](README_V1_SETUP.md) | [Reporte de Bug](https://github.com/AdanGarciaL/Literatura-Gestion/issues)

</div>

---

**Última actualización**: 18 de Febrero de 2026 | **Estado**: ✅ Producción
