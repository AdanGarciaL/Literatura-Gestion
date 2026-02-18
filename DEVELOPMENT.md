# Documentación de Desarrollo

## Arquitectura

### Backend (PHP)
- **api/** - Endpoints REST que manejan toda la lógica
- **config.php** - Configuración centralizada
- **api/db.php** - Conexión a SQLite con reintentos
- **api/csrf.php** - Validación de tokens CSRF

### Frontend (JavaScript)
- **assets/js/app.js** - Módulos para: inventario, apadrinamiento, ventas, usuarios, reportes
- **assets/js/login.js** - Autenticación y manejo de sesiones
- **assets/css/style.css** - Estilos responsive

### Base de Datos
- **SQLite** - Base de datos embebida, sin servidor
- **Tablas**: usuarios, apadrinamientos, inventario, ventas, registros, cambios_inventario

## Flujos Principales

### 1. Login (Ayudante)
```
index.php → form-ayudante
         → api/api_login.php (modo=ayudante)
         → Genera CSRF token
         → sessionStorage: csrf_token, user_role
         → dashboard.php (data-role=ayudante)
```

### 2. Registrar Apadrinamiento
```
Botón "REGISTRAR CERCO" (app.js)
  → apadrinamiento.crear()
  → POST api_apadrinamiento.php?accion=crear
  → INSERT en tabla apadrinamientos
  → Recarga tabla en tiempo real
```

### 3. Terminar Apadrinamiento
```
Botón verde "✓" (app.js)
  → apadrinamiento.finalizar(id)
  → POST api_apadrinamiento.php?accion=finalizar
  → Calcula duración (fecha_fin - fecha_inicio)
  → Guarda usuario_finaliza con rol ayudante: "nombre estigma (grupo)"
  → UPDATE estado='terminado'
```

### 4. Exportar Reporte
```
Botón "Excel" → api/api_reportes.php?accion=exportar&formato=xlsx
  → PHPSpreadsheet genera 3 sheets:
    - Consolidado (resumen)
    - Apadrinamientos (detalle)
    - Ventas (transacciones)
  → Download archivo .xlsx
```

## Seguridad

### CSRF Protection
- Cada login genera un token único
- Token se envía en header `X-CSRF-Token` o body `csrf_token`
- Validado por `require_csrf_or_die()` en cada POST

### Session Handling
- Session storage en servidor (seguro offline)
- Roles: superadmin, admin, ayudante
- Permisos verificados en backend y frontend

### Validación
- Trim y htmlspecialchars en inputs
- Prepared statements en todas las queries
- Validación de tipos (intval, trim)

## Errores Comunes

### "Unexpected end of JSON input"
- El servidor devuelve HTML de error en lugar de JSON
- Verificar que header está establecido como JSON
- Revisar que no hay `echo` de debug antes de `echo json_encode()`

### Error 500 al finalizar
- Problema: `$nowExpr` no interpolado correctamente en query
- Solución: Usar `.` para concatenar: `"... fecha_fin = " . $nowExpr . " ..."`

### CSRF token inválido
- El token no se pasó en header o body
- `fetchWithCSRF()` automáticamente agrega header `X-CSRF-Token`
- Si falla, verificar que `sessionStorage.getItem('csrf_token')` retorna valor

## Testing

### Test Login Ayudante
1. Abrir http://localhost:8080
2. Click "Modo Ayudante"
3. Llenar: Nombre, Estigma, Grupo
4. Verificar que aparece dashboard

### Test Registrar Apadrinamiento
1. Logged como ayudante
2. Click "REGISTRAR CERCO"
3. Llenar formulario
4. Verificar que aparece en tabla

### Test Terminar Apadrinamiento
1. Click botón verde en fila "En proceso"
2. Confirmar diálogo
3. Verificar que estado cambia a "Terminado"
4. Verificar que "Finalizó" muestra: "nombre estigma (grupo)"

### Test Exportar Excel
1. Click en "Reportes"
2. Click "Descargar Excel"
3. Verificar que descarga archivo .xlsx
4. Abrir en Excel y revisar 3 sheets

## Deployment

### En servidor web
1. Copiar contenido de `www/` a carpeta web
2. Configurar permisos de `data/` (writable)
3. Editar `config.php` con ruta de BD
4. Acceder por HTTP/HTTPS

### Desktop (PHP Desktop)
1. Ejecutar `launcher.php`
2. Se abre Chrome embebido
3. Funciona offline completamente

## Performance

- **Queries**: Limitadas a LIMIT 200 para no sobrecargar
- **Caché**: Usar Ctrl+Shift+R para limpiar caché del navegador
- **BD**: Optimizar índices si crece mucho
- **Assets**: Minificar JS/CSS en producción

## Future Improvements

- [ ] Sincronización con servidor remoto
- [ ] Autenticación 2FA
- [ ] Backup automático en la nube
- [ ] Mobile app (React Native)
- [ ] Gráficos de estadísticas
- [ ] Búsqueda avanzada con filtros
