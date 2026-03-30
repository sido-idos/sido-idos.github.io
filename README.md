# Portafolio Web - Alejandro Abarca

Este repositorio contiene un sitio web de portafolio personal, construido en HTML, CSS y JavaScript, con una linea visual definida en el documento de diseno.

Documento base de diseno: [DESIGN.md](DESIGN.md)

## Objetivo

Presentar de forma clara y moderna:

- Perfil profesional
- Formacion academica
- Certificaciones
- Proyectos destacados
- Canales de contacto

## Estructura del Proyecto

```text
.
├── assets/
│   ├── css/
│   │   └── styles.css
│   ├── js/
│   │   ├── main.js
│   │   └── tailwind.config.js
│   ├── gifs/
│   │   ├── analisis_datos.gif
│   │   └── alke_wallet.gif
│   └── cv.pdf
├── index.html
├── educacion.html
├── proyectos.html
├── contacto.html
├── DESIGN.md
└── README.md
```

## Paginas

- [index.html](index.html): pagina principal
- [educacion.html](educacion.html): estudios y certificaciones
- [proyectos.html](proyectos.html): proyectos destacados
- [contacto.html](contacto.html): formulario y enlaces de contacto

## Recursos Compartidos

- Estilos globales: [assets/css/styles.css](assets/css/styles.css)
- Configuracion visual de Tailwind: [assets/js/tailwind.config.js](assets/js/tailwind.config.js)
- Script general: [assets/js/main.js](assets/js/main.js)
- Curriculum: [assets/cv.pdf](assets/cv.pdf)
- GIF de proyectos: [assets/gifs/analisis_datos.gif](assets/gifs/analisis_datos.gif), [assets/gifs/alke_wallet.gif](assets/gifs/alke_wallet.gif)

## Enlaces Oficiales

- GitHub: https://github.com/sido-idos
- LinkedIn: https://www.linkedin.com/in/alejandro-abarca-esteban-268a88362/

## Lineamientos de Mantenimiento

- Mantener recursos estaticos dentro de la carpeta assets y sus subcarpetas por tipo.
- Si se renombra una pagina, actualizar la navegacion en todas las paginas HTML.
- Mantener consistencia visual y tipografica segun [DESIGN.md](DESIGN.md).
- Antes de subir cambios, validar que no existan rutas rotas de HTML, CSS, JS, PDF o GIF.

## Ejecucion Local

Puedes abrir directamente [index.html](index.html) en el navegador.

Opcionalmente, para una experiencia mas estable, servir el proyecto con un servidor local estatico (por ejemplo, Live Server en VS Code).
