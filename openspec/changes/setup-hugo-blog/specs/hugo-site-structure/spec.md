## ADDED Requirements

### Requirement: Hugo configuration file

El sistema SHALL tener un archivo `hugo.yaml` en la raíz con configuración base del sitio incluyendo baseURL, título, idioma, y configuración del tema PaperMod.

#### Scenario: Configuración válida para GitHub Pages

- **WHEN** el sitio se construye con `hugo`
- **THEN** genera archivos estáticos correctos en `public/` con URLs relativas a `https://jpgomz.github.io/`

### Requirement: Tema PaperMod como módulo

El sistema SHALL usar PaperMod como módulo Hugo declarado en `hugo.yaml` bajo la sección `module.imports`.

#### Scenario: Tema se descarga automáticamente

- **WHEN** se ejecuta `hugo mod get` o `hugo server`
- **THEN** Hugo descarga PaperMod automáticamente sin necesidad de submódulos git

### Requirement: Soporte dark/light mode

El sistema SHALL configurar PaperMod con toggle de modo oscuro/claro usando la opción `params.defaultTheme: auto`.

#### Scenario: Tema respeta preferencia del sistema

- **WHEN** usuario visita el sitio con preferencia de sistema en modo oscuro
- **THEN** el sitio muestra tema oscuro por defecto

#### Scenario: Usuario puede cambiar tema manualmente

- **WHEN** usuario hace clic en el toggle de tema
- **THEN** el sitio cambia entre modo oscuro y claro

### Requirement: Menú de navegación

El sistema SHALL configurar un menú principal con enlaces a Home, Posts, Projects y About.

#### Scenario: Navegación visible en todas las páginas

- **WHEN** usuario visita cualquier página del sitio
- **THEN** ve el menú de navegación con los 4 enlaces principales
