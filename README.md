# Playground de Machine Learning · Tópicos de Inteligencia de Negocios

Repositorio que hostea un **playground interactivo de Machine Learning** vía JupyterLite y GitHub Pages.
Los alumnos abren un link y experimentan con 5 modelos directo en el navegador — sin instalar nada.

## 🌐 Link público (rellenar después del primer deploy)

`https://<TU_USUARIO>.github.io/<NOMBRE_DEL_REPO>/lab/index.html?path=README.md`

## 📚 Modelos incluidos

1. **Regresión Lineal** — Ajuste polinomial, Ridge, Lasso
2. **Regresión Logística** — Clasificación binaria, frontera, ROC
3. **KNN** — K-Nearest Neighbors
4. **Árboles de Decisión** — Con visualización del árbol y frontera
5. **K-Means** — Clustering, método del codo y silueta

Cada notebook trae:
- Marco teórico breve alineado con las clases
- Botones `?` con explicación de cada parámetro
- Botón **🚀 Entrenar modelo** con feedback de estado
- Playground sintético + playground con CSV propio
- Ejercicios guiados

## 🚀 Cómo desplegar (paso a paso)

### 1. Crear repo en GitHub

1. Entra a https://github.com/new
2. Nombre del repo: por ejemplo `playground-ml` (puede ser cualquiera, pero recuérdalo)
3. **Público** (necesario para usar GitHub Pages gratis)
4. NO inicialices con README (ya tenemos uno)
5. Clic en **Create repository**

### 2. Subir estos archivos al repo

**Opción A — desde la web de GitHub** (más fácil si no usas Git):

1. En el repo recién creado, clic en **"uploading an existing file"**
2. Arrastra TODOS los archivos y carpetas de este folder (`playground_repo/`):
   - La carpeta `content/` completa
   - La carpeta `.github/` completa
   - `requirements.txt`
   - `jupyter_lite_config.json`
   - `README.md`
3. Mensaje de commit: "Initial setup"
4. Clic en **Commit changes**

**Opción B — desde la terminal** (si usas Git):

```bash
cd playground_repo
git init
git add .
git commit -m "Initial setup"
git branch -M main
git remote add origin https://github.com/<TU_USUARIO>/<NOMBRE_DEL_REPO>.git
git push -u origin main
```

### 3. Habilitar GitHub Pages

1. En tu repo, ve a **Settings** (arriba a la derecha)
2. En el menú izquierdo, clic en **Pages**
3. En **Source**, selecciona **GitHub Actions**
4. ¡Listo! No hay que configurar más.

### 4. Esperar el primer build (~3-5 minutos)

1. Ve a la pestaña **Actions** del repo
2. Verás un workflow corriendo: "Deploy JupyterLite to GitHub Pages"
3. Cuando aparezca palomita verde ✓, el deploy terminó

### 5. Obtener tu link

El link estará en `Settings → Pages` (arriba dirá "Your site is live at...")
o también en la salida del workflow de Actions.

El formato es:
```
https://<TU_USUARIO>.github.io/<NOMBRE_DEL_REPO>/
```

Para abrir el playground directamente:
```
https://<TU_USUARIO>.github.io/<NOMBRE_DEL_REPO>/lab/index.html
```

## ✏️ Modificar los notebooks después del deploy

1. Edita los `.ipynb` en `content/` (en GitHub web o local).
2. Haz commit → push.
3. GitHub Actions rebuildea y republica automáticamente en ~3 minutos.

## 🐛 Solución de problemas comunes

| Problema | Solución |
|----------|----------|
| El workflow falla en "Build JupyterLite" | Verifica que `requirements.txt` no tenga typos |
| Los widgets no se ven | Los alumnos deben refrescar y volver a ejecutar las celdas. Primera carga tarda ~30s. |
| "404 Not Found" al abrir el link | Espera 1-2 min después del primer deploy y refresca |
| Tarda mucho la primera vez | Normal: descarga scikit-learn al navegador (~50MB la primera vez, luego se cachea) |

## 🎯 Para los alumnos

Comparte SOLO el link público. No necesitan instalar nada — solo un navegador moderno (Chrome, Firefox, Edge actualizados).

---

> Hecho para la materia *Tópicos de Inteligencia de Negocios*
>
> Creado por Dr. Angel Moisés Hernández Ponce con ayuda de Claude Code
