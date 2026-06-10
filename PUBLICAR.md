# Publicar desde cero

## 1. Borrar el repo anterior en GitHub

El push incorrecto desde `PROYECTO/` subió código de más. Elimínalo antes de volver a subir:

1. Abre [github.com/cesarsanco-ai/retina-vessel-demo](https://github.com/cesarsanco-ai/retina-vessel-demo)
2. **Settings** → al final **Danger zone**
3. **Delete this repository** → confirma el nombre `cesarsanco-ai/retina-vessel-demo`

## 2. Crear repo vacío (mismo nombre u otro)

1. [github.com/new](https://github.com/new)
2. Nombre sugerido: `retina-vessel-demo`
3. **Sin** README, .gitignore ni licencia (ya están en esta carpeta)
4. Crear repositorio

## 3. Subir solo esta carpeta

```bash
cd retina-vessel-demo

git init -b main
git add .
git status    # ~367 archivos: index.html, manifest.json, assets/, README, workflow
git commit -m "Demo web — detección de vasos retinianos DRIVE"
git remote add origin https://github.com/cesarsanco-ai/retina-vessel-demo.git
git push -u origin main
```

## 4. Activar GitHub Pages

1. Repo → **Settings → Pages**
2. **Build and deployment → Source:** `GitHub Actions`
3. Tras el push, revisa **Actions** → *Deploy demo to GitHub Pages*
4. URL: `https://cesarsanco-ai.github.io/retina-vessel-demo/`

## 5. Comprobar

- Abre la URL y pulsa **Analizar vasos**
- El pie debe enlazar a [github.com/cesarsanco-ai](https://github.com/cesarsanco-ai)

---

## Qué incluye esta carpeta

| Archivo / carpeta | Rol |
|-------------------|-----|
| `index.html` | Demo |
| `manifest.json` | Índice de imágenes y métricas |
| `assets/` | PNG precalculados (~84 MB) |
| `.nojekyll` | GitHub Pages |
| `.github/workflows/github-pages.yml` | Deploy automático |
| `README.md`, `LICENSE` | Documentación |

## Qué NO subir aquí

Mantén en local (`../PROYECTO/`):

- `src/`, `main.py`, `app.py`, `docs/`, tests
- `.venv/`, dataset DRIVE (`../CLASE-CURSO/`)
