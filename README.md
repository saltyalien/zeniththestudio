# ZENITH The Studio

Sitio web de portafolio para ZENITH The Studio, un estudio creativo especializado en dirección creativa, identidad visual y desarrollo conceptual.

## Stack

- HTML semántico
- CSS vanilla con Custom Properties
- Google Fonts (Gantari) + fuentes locales (CooperHewitt)
- Sin frameworks ni dependencias externas

## Estructura del proyecto

```
zeniththestudio/
├── index.html              # Página principal
├── zenith-main.css         # Estilos (organizado en 12 secciones)
├── README.md
├── CooperHewitt-WebFonts-public/   # Fuente local CooperHewitt
├── img/                    # Imágenes del sitio
└── logo/                   # Assets de logo
```

## CSS — Guía de estilos

### Variables disponibles

| Variable | Valor | Uso |
|----------|-------|-----|
| `--clr-bg` | `#1C1D22` | Fondo principal |
| `--clr-text` | `#ffffff` | Texto |
| `--clr-accent` | `#B3E5FB` | Acentos, links |
| `--clr-primary` | `#EA2024` | Color primario/rojo |
| `--clr-hover` | `#1449a6` | Hover de botones |
| `--clr-overlay` | `#02051c98` | Overlay de galería |
| `--ff-gantari` | `'Gantari', 'CooperHewitt', sans-serif` | Headings |
| `--ff-cooper` | `'CooperHewitt', sans-serif` | Cuerpo y UI |
| `--navbar-height` | `7.5rem` | Altura del navbar sticky |
| `--content-max-width` | `900px` | Ancho máximo de contenido |
| `--gallery-max-width` | `1200px` | Ancho máximo de galería |

### Convenciones

- **Naming**: Clases en PascalCase para secciones (`.Hero`, `.Nosotros`), lowercase para componentes (`.navbar`, `.gallery-item`, `.overlay`)
- **Organización**: El CSS sigue 12 secciones numeradas — desde Custom Properties hasta Media Queries
- **Unidades**: `rem` para tamaños y espaciado, `px` para detalles finos (paddings de layout en navbar/gallery)
- **Responsive**: 2 breakpoints — `768px` (tablet) y `480px` (mobile)

### Para agregar una sección nueva

1. Seguir la numeración existente en `zenith-main.css`
2. Usar las variables de color y tipografía definidas en `:root`
3. Agregar breakpoints responsive al final del archivo

## Notas para desarrollo futuro

- El modal en la galería está maquetado pero **no tiene JS asociado**. El archivo `scripts/main.js` no existe aún. Para activarlo, agregar toggle de la clase `.is-open` en el elemento `.modal`.
- Las fuentes CooperHewitt están en `.woff` solamente. Si se necesita soporte para navegadores legacy, agregar formatos `.woff2` y `.eot` en los `@font-face`.
- El `<nav>` está actualmente dentro de `<head>` en el HTML — moverlo al `<body>` para HTML válido.
