# Estructura del proyecto - Procesadores Gráficos

## Estructura actual de archivos

```
ProcesadoresGraficos/
├── index.html          # Página de entrada (landing con enlaces)
├── procesadores.html   # Sitio principal (contenido sobre GPUs)
├── 404.html            # Página de error 404
├── robots.txt          # Instrucciones para buscadores
├── README.md
├── .gitignore
├── css/
│   ├── stylesmain.css  # Estilos de la landing (index) y 404
│   └── styles.css      # Tema Bootstrap del sitio principal
├── js/
│   └── scripts.js      # Scripts del sitio principal (navbar, scroll, modales)
├── assets/
│   └── img/
│       ├── icono.ico
│       ├── logo.jpg
│       ├── close-icon.svg
│       ├── navbar-logo.svg
│       ├── portfolio/   # Imágenes del portfolio
│       ├── about/       # Imágenes de la sección Casos Reales
│       └── logos/       # Logos (IBM, Google, etc.)
└── docs/
    └── ESTRUCTURA.md   # Este archivo
```

## Convenciones

- **HTML**: semántico (`header`, `main`, `nav`, `footer`), `lang="es"`, atributos de accesibilidad (`aria-label`, `alt` descriptivos).
- **CSS**: variables en `:root` en `stylesmain.css`; no modificar `styles.css` si no es necesario (tema Bootstrap).
- **Rutas**: relativas desde la raíz del proyecto (`css/`, `assets/`, `procesadores.html`).
- **Enlaces externos**: usar `target="_blank"` y `rel="noopener noreferrer"`.

## Mejoras futuras posibles

1. **CSS**
   - Crear `css/base/variables.css` con variables compartidas e importarlas donde haga falta.
   - Separar componentes en `css/components/` (botones, navegación, footer).

2. **JS**
   - Cargar `scripts.js` solo en `procesadores.html` (no en index).
   - Si creces a más páginas, un `js/common.js` para comportamiento compartido.

3. **Assets**
   - Mantener `assets/img/` por tipo (portfolio, about, icons).
   - Usar nombres en minúsculas y sin espacios para archivos.

4. **SEO**
   - Añadir `sitemap.xml` cuando tengas URL definitiva y sustituir en `robots.txt` `https://tudominio.com` por la URL real.

5. **Servidor**
   - Configurar el servidor para devolver `404.html` en rutas no encontradas (depende de tu hosting).
