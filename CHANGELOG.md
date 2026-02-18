# Changelog

Todos los cambios notables en este proyecto se documentan en este archivo.

## [v1.0.0] - 2026-02-18

### ✨ Características Nuevas
- Sistema completo de gestión de apadrinamientos
- Rol "Ayudante" con permisos limitados (solo agregar y terminar)
- Control de inventario con historial de cambios
- Gestión de ventas y seguimiento de deudores
- Exportación a Excel en 3 formatos
- Autenticación con CSRF tokens
- Sistema offline con SQLite

### 🔧 Mejoras
- Interfaz responsive con Bootstrap
- Tema claro/oscuro
- Búsqueda y filtros en tiempo real
- Cálculo automático de duración de apadrinamientos
- Notificaciones visuales (SweetAlert2)
- Validación en cliente y servidor

### 🐛 Correcciones
- Error 500 en salud_sistema para ayudante (FIXED)
- Botones de editar/eliminar visibles para ayudante (FIXED)
- Error al terminar apadrinamiento con rol ayudante (FIXED)
- Problema con interpolación de $nowExpr en queries (FIXED)
- Token CSRF no se guardaba en sessionStorage (FIXED)

### 📝 Documentación
- README completo con instrucciones de inicio
- DEVELOPMENT.md con arquitectura y flujos
- .gitignore configurado
- Comentarios en código

## Próximas Versiones

### [v1.1.0] - Planeado
- Sincronización con servidor remoto
- Gráficos y estadísticas
- Búsqueda avanzada con filtros personalizados
- Backup automático

### [v2.0.0] - Futuro
- Aplicación móvil (React Native)
- Autenticación 2FA
- Integración con sistemas de pago
- Importación de datos desde Excel
