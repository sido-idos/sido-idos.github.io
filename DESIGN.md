# Especificacion del Sistema de Diseno: Portafolio Tecnologico de Alto Nivel

## Estructura del Proyecto
Para mantener el orden del proyecto, los recursos compartidos deben vivir dentro de una carpeta general `assets`.

Estructura actual recomendada:

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
└── DESIGN.md
```

Reglas de rutas:
*   Todas las paginas HTML deben cargar estilos desde `assets/css/styles.css`.
*   Todas las paginas HTML deben cargar scripts desde `assets/js/tailwind.config.js` y `assets/js/main.js`.
*   El boton de descarga de CV debe apuntar a `assets/cv.pdf`.
*   Si se agregan mas recursos (imagenes, iconos, fuentes o documentos), deben colocarse dentro de `assets/` en subcarpetas por tipo.

## Contenido Oficial del Portafolio
Esta seccion define los datos reales que deben mantenerse sincronizados en las paginas del sitio.

### Perfiles
*   GitHub: `https://github.com/sido-idos`
*   LinkedIn: `https://www.linkedin.com/in/alejandro-abarca-esteban-268a88362/`

### Educacion
*   Ingenieria en Informatica en INACAP (en curso).
*   Alumno del bootcamp Desarrollador de Aplicaciones Fullstack Python Trainee de Talento Digital - SENCE Chile, impartido por la OTEC ECAS.

### Certificaciones
*   Oracle Cloud Infrastructure 2025 Certified Foundations Associate
*   Oracle Cloud Infrastructure 2025 Certified AI Foundations Associate
*   Oracle Cloud Infrastructure 2025 Certified Generative AI Professional
*   Oracle Cloud Infrastructure 2025 Certified Multicloud Architect Professional
*   Oracle Cloud Infrastructure 2025 Certified Data Science Professional
*   Huawei HCIA AI
*   Huawei HCIA Cloud Service

### Proyectos Destacados
*   `https://github.com/sido-idos/challenge1-data-science-latam`
*   `https://github.com/sido-idos/mod_7`

## 1. Vision General y Norte Creativo: "La Narrativa Arquitectonica"
Para ir mas alla de la "plantilla generica de desarrollador", este sistema de diseno adopta como norte creativo **La Narrativa Arquitectonica**.

Un desarrollador de pila completa y analista de datos vive en la interseccion entre la logica rigida (servidor/datos) y la experiencia fluida (interfaz). Por eso, la interfaz debe sentirse ingenieril y eterea al mismo tiempo. Lo logramos mediante **Asimetria Intencional** (donde las visualizaciones de datos pueden desbordarse fuera del lienzo) y **Profundidad Tonal**, usando superficies apiladas en lugar de lineas para guiar la mirada. Estamos construyendo una galeria digital, no un panel de control.

## 2. Colores: Profundidad de Pizarra y Vitalidad Electrica
La paleta se apoya en `surface` (`#060e20`), una pizarra profunda y densa que funciona como fondo tipo vacio para acentos que parecen "emitir luz".

### Regla de "Sin Lineas"
**Instruccion explicita:** No usar bordes solidos de 1px para definir secciones. Los limites del layout deben establecerse mediante cambios de fondo.
*   **Seccionado:** Colocar una seccion `surface_container_low` (`#091328`) directamente contra un fondo `surface` (`#060e20`). El cambio de 1.5% en luminancia basta para que el ojo humano perciba un limite sin el "ruido" visual de una linea.

### Jerarquia y Anidamiento de Superficies
Trata la interfaz como una pila fisica de materiales semitranslucidos:
1.  **Capa base:** `surface` (la base).
2.  **Capa media:** `surface_container` (agrupaciones de contenido).
3.  **Capa superior:** `surface_container_high` (tarjetas interactivas o fragmentos de codigo).

### Regla de Cristal y Degradado
Para acciones primarias y elementos hero de alto impacto, utiliza **Texturas Firma**:
*   **CTAs:** Aplicar un degradado lineal desde `primary` (`#bd9dff`) hasta `primary_dim` (`#8a4cfc`) en un angulo de 135 grados.
*   **Navegacion flotante:** Usar `surface_bright` con 60% de opacidad y `20px` de desenfoque de fondo para crear un efecto de "cristal esmerilado" que permita que las visualizaciones de datos del fondo se filtren.

## 3. Tipografia: Autoridad Editorial
Utilizamos un sistema de tres tipografias para diferenciar narrativa, datos tecnicos y etiquetas funcionales.

*   **Display y titulares (Manrope):** Grande, contundente y aireada. Se usa para impacto. La altura x generosa de Manrope transmite confianza profesional.
*   **Cuerpo y titulos (Inter):** La tipografia de batalla. Inter ofrece maxima legibilidad para descripciones de proyectos y publicaciones tecnicas.
*   **Etiquetas (Space Grotesk):** Sensacion "tech-mono" especializada para metadatos (por ejemplo, "Python", "Django", "PostgreSQL"). Las particularidades geometricas de Space Grotesk refuerzan la identidad del desarrollador.

**Escala destacada:**
*   `display-lg`: 3.5rem (usar solo en titulares hero).
*   `label-md`: 0.75rem (usar en chips del stack tecnico y marcas de tiempo de datos).

## 4. Elevacion y Profundidad: Capas Tonales
Las sombras tradicionales suelen ser un recurso para compensar contraste deficiente. En este sistema priorizamos el **Apilado Tonal**.

*   **Principio de capas:** Para elevar una tarjeta, moverla de `surface_container` a `surface_container_highest`.
*   **Sombras ambientales:** Si un elemento flotante (como un modal) requiere sombra, usar un blur amplio (32px+) con color `surface_container_lowest` al 40% de opacidad. Evitar sombras negras: "ensucian" los azules profundos del fondo pizarra.
*   **Respaldo de "borde fantasma":** Para accesibilidad en campos de entrada, usar `outline_variant` (`#40485d`) al 20% de opacidad. Debe sentirse, no verse.
*   **Profundidad de interaccion:** En hover, una tarjeta no solo cambia color; debe transicionar de `surface_container` a `surface_bright`, simulando una fuente de luz acercandose a la superficie.

## 5. Componentes

### Botones
*   **Primario:** Degradado (`primary` a `primary_dim`), texto `on_primary`, `round-md` (0.75rem).
*   **Secundario:** Fondo `secondary_container` con texto `secondary`. Sin borde.
*   **Terciario:** Estilo fantasma. Fondo transparente, texto `primary`. Usar para "Leer mas" o "Ver codigo".

### Tarjetas y Listas
*   **Prohibicion de divisores:** Nunca usar `<hr>` ni `border-bottom`. Separar elementos de lista con **escala de espaciado** `4` (1.4rem) o con un cambio sutil de fondo a `surface_container_low`.
*   **Tarjetas de proyecto:** Usar radio `xl` (1.5rem) para una sensacion "tecnologica amable". Usar `surface_variant` para el cuerpo de la tarjeta.

### Chips (Stack Tecnologico)
*   **Estilo:** Tipografia `label-md` en `Space Grotesk`. Fondo: `surface_bright` al 40% de opacidad.
*   **Iconos:** Integrar iconos monocromos de 16px para Python, Django y Jupyter. El color del icono debe heredar `on_surface_variant`, salvo en hover.

### Campos de Entrada
*   **Estilo:** Fondo `surface_container_lowest`. Esquinas redondeadas `sm` (0.25rem).
*   **Estado de foco:** Un "borde fantasma" de 2px usando `secondary` al 50% de opacidad y un resplandor externo sutil `primary`.

### Acentos para Visualizacion de Datos
*   **Flujo de datos primario:** `secondary` (`#34b5fa`)
*   **Flujo de datos secundario:** `tertiary` (`#ffa5d9`)
*   **Anomalias/errores:** `error` (`#ff6e84`)

## 6. Buenas y Malas Practicas

### Haz:
*   **Aprovecha el espacio negativo:** Usa espaciado `16` (5.5rem) entre secciones principales para que el contenido tecnico respire.
*   **Anima las transiciones:** Usa `cubic-bezier(0.4, 0, 0.2, 1)` para todos los estados hover. Se siente mas "ingenieril" que una transicion lineal.
*   **Apilado:** Coloca notebooks de Jupyter o bloques de codigo dentro de un contenedor `surface_container_highest` para que se perciban como "herramientas" sobre el "escritorio".

### Evita:
*   **Nada de negro puro:** No usar `#000000` como fondo (salvo en `surface_container_lowest`). Mata la profundidad de la paleta pizarra.
*   **Nada de bordes de alto contraste:** Si te ves tentado a usar borde, aumenta el padding o cambia el color de fondo.
*   **Nada de iconos genericos:** Evita packs de iconos "planos". Usa iconos de linea con trazo de `1.5px` para que coincidan con el peso de `Space Grotesk`.