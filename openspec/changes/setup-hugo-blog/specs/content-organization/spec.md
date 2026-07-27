## ADDED Requirements

### Requirement: Directorio de posts técnicos

El sistema SHALL tener un directorio `content/posts/` para artículos técnicos con archetype que incluya frontmatter con title, date, tags, y draft.

#### Scenario: Crear nuevo post

- **WHEN** se ejecuta `hugo new posts/mi-articulo.md`
- **THEN** se crea archivo con frontmatter predefinido listo para editar

### Requirement: Directorio de proyectos

El sistema SHALL tener un directorio `content/projects/` para documentar proyectos open source con archetype que incluya title, date, tags, github URL, y description.

#### Scenario: Listar proyectos en página dedicada

- **WHEN** usuario navega a `/projects/`
- **THEN** ve lista de todos los proyectos con título y descripción

### Requirement: Página About

El sistema SHALL tener una página `content/about.md` con información personal del autor incluyendo bio, skills, y links de contacto.

#### Scenario: About accesible desde menú

- **WHEN** usuario hace clic en "About" en el menú
- **THEN** navega a página con información del autor

### Requirement: Homepage con posts recientes

El sistema SHALL mostrar en la homepage una lista de los posts más recientes usando el layout de PaperMod.

#### Scenario: Homepage muestra contenido

- **WHEN** usuario visita la raíz del sitio
- **THEN** ve lista de posts recientes con título, fecha y resumen
