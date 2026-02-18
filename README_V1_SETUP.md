# Literatura V1 - Instalador y Configuración

## 📦 Descargas

### Versión 1.0.0 - Offline
- **Instalador**: `Literatura-V1-Setup-1.0.0.exe` (~165 MB)
- **Ubicación Local**: `C:\Program Files\TG Gestion Estables\Literatura\Literatura V1\installer_output\Literatura-V1-Setup-1.0.0.exe`

## 🚀 Características del Instalador

✅ **Versión**: 1.0.0 (Offline)  
✅ **Aplicación**: Literatura - Gestor de Contenidos  
✅ **Compresión**: LZMA2 (Alta compresión)  
✅ **Requisitos**: Windows 7 SP1 o superior  
✅ **Permisos**: Requiere Administrador  

### Funcionalidades Incluidas

- ✓ Instalación en modo Administrador
- ✓ Opción para crear ícono en escritorio
- ✓ Opción para ejecutar siempre como Administrador
- ✓ Opción para instalar Visual C++ Redistributable 2022 (recomendado)
- ✓ Desinstalador completo
- ✓ Interfaz multiidioma (Español/Inglés)
- ✓ Aplicación completamente offline

## 📋 Cambios Realizados

### Modificaciones del Instalador

1. **Nombre de Aplicación**: TG Gestion → **Literatura V1**
2. **Versión**: Actualizada a **1.0.0**
3. **Ejecutable**: `Literatura.exe`
4. **Licencia**: Renovada y actualizada para Literatura V1
5. **Rutas de Salida**: Configurada en `installer_output/`

### Configuración de Privilegios

- Instalación requerida en modo Administrador
- Opción para ejecutar siempre como Administrador (mediante Registry HKLM)
- Integración con Windows User Access Control (UAC)

### Componentes Incluidos

- **Aplicación**: Literatura.exe con todas sus dependencias
- **Framework**: Chromium Embedded Framework (CEF)
- **Backend**: PHP y componentes necesarios
- **Web**: Archivos www con interfaz web
- **Datos**: Caché y archivos de configuración
- **Localizaciones**: Soporte multiidioma

## 💾 Información de Instalación

### Archivos Modificados

- `installer.iss` - Script de Inno Setup configurado para Literatura V1
- `LICENSE.txt` - Licencia actualizada
- `INSTALADOR_GENERADO.txt` - Documento de cambios realizados

### Directorio de Instalación por Defecto

```
C:\Program Files\Literatura V1\
├── Literatura.exe
├── php/
├── www/
├── locales/
├── data/
├── webcache/
└── LICENSE.txt
```

## 🔧 Requisitos del Sistema

- **Sistema Operativo**: Windows 7 SP1 o superior (Windows 10/11 recomendado)
- **Memoria RAM**: Mínimo 2 GB (4 GB recomendado)
- **Espacio en Disco**: Mínimo 500 MB disponible
- **Visual C++ Redistributable**: 2022 o superior (se ofrece instalar en el setup)

## 📥 Proceso de Instalación

1. Descargar `Literatura-V1-Setup-1.0.0.exe`
2. Ejecutar el instalador
3. Seleccionar idioma (Español/Inglés)
4. Aceptar la licencia
5. Elegir ubicación de instalación
6. Seleccionar opciones:
   - ☑ Crear ícono en escritorio
   - ☑ Ejecutar siempre como Administrador (recomendado)
   - ☑ Instalar Visual C++ Redistributable 2022 (recomendado)
7. Completar la instalación

## 🔐 Notas de Seguridad

- El instalador requiere permisos de Administrador
- Se recomienda ejecutar siempre la aplicación como Administrador
- Incluye soporte para Visual C++ Redistributable 2022 para máxima compatibilidad
- Todas las dependencias están incluidas (offline)

## 📄 Licencia

Ver `LICENSE.txt` para más información sobre los términos de uso.

---

**Versión**: 1.0.0  
**Fecha**: Febrero 2026  
**Estado**: Listo para Producción

