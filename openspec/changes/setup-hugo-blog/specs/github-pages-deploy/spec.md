## ADDED Requirements

### Requirement: GitHub Actions workflow para Hugo

El sistema SHALL tener un workflow en `.github/workflows/hugo.yaml` que construya el sitio con Hugo y lo despliegue a GitHub Pages.

#### Scenario: Deploy automático en push a main

- **WHEN** se hace push a la rama `main`
- **THEN** GitHub Actions ejecuta build de Hugo y despliega a GitHub Pages

### Requirement: Build con versión específica de Hugo

El sistema SHALL usar Hugo extended v0.147.0 o superior en el workflow para garantizar compatibilidad con módulos y SCSS.

#### Scenario: Build exitoso con módulos

- **WHEN** workflow ejecuta `hugo --minify`
- **THEN** Hugo descarga módulos automáticamente y genera sitio minificado

### Requirement: Configuración de GitHub Pages

El sistema SHALL configurar el workflow para usar GitHub Pages con source `github-actions` (no branch gh-pages).

#### Scenario: Sitio accesible después de deploy

- **WHEN** workflow completa exitosamente
- **THEN** sitio está disponible en `https://jpgomz.github.io/`

### Requirement: Cache de módulos Hugo

El sistema SHALL configurar cache de módulos Hugo en el workflow para acelerar builds subsecuentes.

#### Scenario: Build rápido con cache

- **WHEN** se ejecuta workflow por segunda vez sin cambios en módulos
- **THEN** Hugo usa módulos cacheados sin descargarlos de nuevo
