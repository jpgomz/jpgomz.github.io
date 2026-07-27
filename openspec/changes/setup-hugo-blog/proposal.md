## Why

Necesito un portafolio personal de ingeniería de software para compartir conocimientos y documentar mi trabajo. El sitio mostrará proyectos de código abierto, artículos técnicos, experimentos con Linux, desarrollo backend, DevOps y desarrollo asistido por IA. Debe desplegarse en GitHub Pages con tecnología moderna y liviana.

## What Changes

- Configurar Hugo como generador de sitios estáticos
- Integrar tema PaperMod para diseño limpio y profesional
- Crear estructura de contenido para posts, proyectos y página about
- Configurar GitHub Actions para deploy automático a GitHub Pages
- Configurar metadata SEO y soporte dark/light mode

## Capabilities

### New Capabilities

- `hugo-site-structure`: Configuración base de Hugo con tema PaperMod, incluyendo config.yaml, estructura de directorios y assets
- `content-organization`: Estructura de contenido con secciones para posts técnicos, proyectos OSS y página about
- `github-pages-deploy`: Workflow de GitHub Actions para build y deploy automático a GitHub Pages

### Modified Capabilities

## Impact

- **Nuevo directorio raíz**: Archivos de configuración Hugo (config.yaml, archetypes/)
- **Contenido**: Directorio content/ con posts/, projects/, about.md
- **CI/CD**: .github/workflows/hugo.yml para deploy automático
- **Tema**: Submódulo git o módulo Hugo para PaperMod
- **Assets**: static/ para imágenes y recursos estáticos
