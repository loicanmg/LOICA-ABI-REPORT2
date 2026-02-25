# LOICA - Informe OOH

Informe interactivo de medios **Out of Home (OOH)** con dos conjuntos de datos.

## 📁 Contenido de la carpeta

```
github_upload_2/
├── index.html                 # Página de inicio (selector de datasets)
├── report_original.html       # Reporte con 97 ubicaciones
├── report_extended.html       # Reporte con 356 ubicaciones
├── DATOS_OOH_V2.json         # Datos originales (JSON)
├── DATOS_OOH_V2_E2.json      # Datos extendidos (JSON)
├── img/                       # Imágenes para dataset original (193 imágenes)
└── img2/                      # Imágenes para dataset extendido (356 imágenes)
```

## 🚀 Cómo subir a GitHub Pages

### Opción 1: Via GitHub Web Interface (Más fácil)

1. Abre tu repositorio en GitHub
2. Haz clic en **"Add file"** → **"Upload files"**
3. Arrastra y suelta todos los archivos de esta carpeta (`github_upload_2/`)
4. En el mensaje de commit, escribe algo como: `Update OOH reports with extended dataset`
5. Haz clic en **"Commit changes"**

### Opción 2: Via Git CLI (Línea de comandos)

```bash
# Navega a tu repositorio local
cd tu_repositorio

# Copia todos los archivos de github_upload_2 al root del repo
cp -r github_upload_2/* .

# O en PowerShell (Windows):
# Copy-Item -Path ".\github_upload_2\*" -Destination "." -Recurse -Force

# Añade los cambios
git add .

# Commit
git commit -m "Update OOH reports with extended dataset"

# Push a GitHub
git push origin main
```

### Opción 3: Subir a carpeta específica

Si prefieres mantener los archivos en una subcarpeta:

```bash
cp -r github_upload_2 tu_repositorio/ooh-reports/
cd tu_repositorio
git add .
git commit -m "Add OOH reports in separate folder"
git push origin main
```

## 🌐 Acceder al reporte

Una vez subido a GitHub y configurado GitHub Pages:

- **Página de inicio**: `https://tu-usuario.github.io/tu-repositorio/`
- **Datos originales**: `https://tu-usuario.github.io/tu-repositorio/report_original.html`
- **Datos extendidos**: `https://tu-usuario.github.io/tu-repositorio/report_extended.html`

### Configurar GitHub Pages

1. Ve a **Settings** de tu repositorio
2. Busca **"Pages"** en el menú izquierdo
3. En **"Source"**, selecciona la rama (generalmente `main`)
4. Selecciona la carpeta: **`/ (root)`** o tu carpeta específica
5. Haz clic en **"Save"**

⏳ Tu sitio estará disponible en pocos minutos (normalmente 1-2 minutos)

## 📊 Características del reporte

### Vista General
- Métricas resumidas (Total OOHs, Marcas, Comunas, Regiones)
- Gráficos interactivos
- Filtros por Comuna y Marca

### Detalle por Ubicación
- Información completa de cada ubicación
- Galería de imágenes local
- Google Maps agregado
- Navegación entre ubicaciones con teclas flecha

### Mapa Interactivo
- Mapa Leaflet con ubicaciones
- Marcadores por marca (con colores distinguibles)
- Leyenda interactiva
- Filtros por Marca y Soporte

### Tabla Completa
- Vista tabular de todos los datos
- Exportación a CSV
- Exportación a Excel

## 🎨 Características especiales - Datos Extendidos

Cuando se selecciona el dataset extendido (356 ubicaciones):
- Automáticamente se desmarca la marca **"Otras Marcas"**
- Los gráficos muestran solo las 8 marcas principales
- Mejor visualización y análisis de datos

## 📱 Responsive Design

El reporte es completamente responsive y funciona en:
- 💻 Desktop (Chrome, Firefox, Safari, Edge)
- 📱 Tablets
- 📞 Celulares

## 📄 Notas técnicas

- Todos los datos están en formato JSON
- Las imágenes se cargan desde carpetas locales (no requiere servidor)
- El código JavaScript es vanilla (sin dependencias externas)
- Compatible con GitHub Pages sin configuración adicional

## ❓ Troubleshooting

### Las imágenes no se cargan
- Verifica que las carpetas `img/` e `img2/` estén en el root del repositorio
- Asegúrate que los archivos de imagen tienen los nombres correctos: `ID{id}_{1-10}.(jpg|jpeg)`

### El reporte no se ve
- Espera 2-3 minutos después de hacer push para que GitHub actualice
- Verifica que GitHub Pages esté habilitado en Settings → Pages
- Limpia el navegador (Ctrl+Shift+R / Cmd+Shift+R)

### Problemas con rutas de archivos
- Todos los archivos deben estar en el root del repositorio (mismo nivel que index.html)
- Si usas subcarpeta, actualiza las rutas en los HTML

---

**Última actualización**: Febrero 24, 2026
