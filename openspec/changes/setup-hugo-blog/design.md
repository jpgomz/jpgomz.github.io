## Context

Repo vacío `jpgomz.github.io` destinado a GitHub Pages. Necesita un generador de sitios estáticos moderno y liviano para un portafolio de ingeniería de software con blog técnico.

## Goals / Non-Goals

**Goals:**

- Setup mínimo funcional de Hugo con tema PaperMod
- Deploy automático via GitHub Actions
- Estructura clara para posts, proyectos y about
- Soporte dark/light mode y SEO básico

**Non-Goals:**

- CMS o editor visual
- Comentarios (puede agregarse después)
- Analytics (puede agregarse después)
- Dominio personalizado is-a.dev (fase posterior)

## Decisions

### 1. Hugo como generador estático

**Decisión**: Usar Hugo v0.147+
**Alternativas consideradas**:

- Jekyll: Más lento, requiere Ruby
- Astro: Requiere Node.js, más complejo
- 11ty: Flexible pero más configuración inicial

**Razón**: Binary único, builds en milisegundos, sin dependencias de runtime.

### 2. Tema PaperMod via módulo Hugo

**Decisión**: Instalar PaperMod como módulo Hugo (no submódulo git)
**Razón**: Más limpio, mejor manejo de versiones, sin conflictos de submódulos.

### 3. Estructura de contenido

```
content/
├── posts/           # Artículos técnicos (list layout)
├── projects/        # Proyectos OSS (list layout)
└── about.md         # Página about (single layout)
```

### 4. GitHub Actions para deploy

**Decisión**: Workflow oficial de Hugo para GitHub Pages
**Razón**: Mantenido por Hugo, bien documentado, usa actions/cache para builds rápidos.

## Risks / Trade-offs

- **Go templates learning curve** → Mitigación: PaperMod tiene buena documentación y ejemplos
- **Dependencia de tema externo** → Mitigación: Módulo Hugo permite pin de versión específica
- **Builds en CI pueden fallar** → Mitigación: Workflow probado, fácil debug local con `hugo server`
