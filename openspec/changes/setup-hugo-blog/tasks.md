## 1. Inicialización Hugo

- [x] 1.1 Inicializar módulo Go para Hugo (`hugo mod init github.com/jpgomz/jpgomz.github.io`)
- [x] 1.2 Crear archivo `hugo.yaml` con configuración base (baseURL, título, idioma)
- [x] 1.3 Configurar PaperMod como módulo en `hugo.yaml`
- [x] 1.4 Configurar parámetros de PaperMod (defaultTheme, ShowReadingTime, ShowShareButtons)
- [x] 1.5 Configurar menú de navegación (Home, Posts, Projects, About)

## 2. Estructura de Contenido

- [x] 2.1 Crear directorio `content/posts/` con archivo índice
- [x] 2.2 Crear directorio `content/projects/` con archivo índice
- [x] 2.3 Crear página `content/about.md` con estructura base
- [x] 2.4 Crear archetype `archetypes/posts.md` para nuevos posts
- [x] 2.5 Crear archetype `archetypes/projects.md` para nuevos proyectos
- [x] 2.6 Crear post de ejemplo en `content/posts/`

## 3. GitHub Actions Deploy

- [x] 3.1 Crear directorio `.github/workflows/`
- [x] 3.2 Crear workflow `hugo.yaml` con build y deploy a GitHub Pages
- [x] 3.3 Configurar cache de módulos Hugo en el workflow
- [x] 3.4 Configurar permisos de GITHUB_TOKEN para Pages

## 4. Verificación Local

- [x] 4.1 Ejecutar `hugo server` y verificar sitio local
- [x] 4.2 Verificar navegación y toggle dark/light mode
- [x] 4.3 Verificar build con `hugo --minify`
