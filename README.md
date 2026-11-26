# ASPHALT BUTCHER ACADEMY

Sitio web estático y multipágina para una academia de pilotaje deportivo ubicada en Bucaramanga, Colombia.

El proyecto presenta la oferta formativa en:

- Autódromo y pilotaje de auto.
- MotoGP y motociclismo deportivo.
- Drift y freestyle.
- Mecánica y reparación rápida.
- Preparación para competición.
- Motocross y enduro.

La propuesta comunica disciplina, precisión, seguridad y entrenamiento en circuitos cerrados. Está dirigida a personas que ya cuentan con licencia de conducción vigente; el sitio no se presenta como una autoescuela ni ofrece conducción básica.

## Índice

- [Vista general](#vista-general)
- [Páginas disponibles](#páginas-disponibles)
- [Tecnologías utilizadas](#tecnologías-utilizadas)
- [Estructura del proyecto](#estructura-del-proyecto)
- [Cómo ejecutar el sitio](#cómo-ejecutar-el-sitio)
- [Arquitectura CSS](#arquitectura-css)
- [Diseño responsive](#diseño-responsive)
- [Accesibilidad](#accesibilidad)
- [Contenido y configuración](#contenido-y-configuración)
- [Formulario de agenda](#formulario-de-agenda)
- [Recursos visuales](#recursos-visuales)
- [Limitaciones actuales](#limitaciones-actuales)
- [Mejoras recomendadas](#mejoras-recomendadas)
- [Personalización rápida](#personalización-rápida)
- [Publicación](#publicación)

## Vista general

ASPHALT BUTCHER ACADEMY utiliza una identidad visual inspirada en el automovilismo y el motociclismo:

- Grafito oscuro para transmitir profesionalismo y fuerza.
- Rojo intenso para acciones y elementos destacados.
- Rojo vivo para llamadas a la acción y estadísticas.
- Gris metálico para detalles técnicos.
- Tipografía condensada para titulares de alto impacto.
- Tipografía legible para párrafos, formularios y navegación.
- Líneas, ángulos y patrones que recuerdan trazados, banderas y sectores de pista.

## Páginas disponibles

| Archivo | Propósito |
|---|---|
| `index.html` | Página principal, propuesta de valor, disciplinas, cifras y llamadas a la acción. |
| `sobre.html` | Historia, propósito, misión, visión, valores y testimonios de la academia. |
| `instructores.html` | Presentación del equipo de auto, moto, stunt, mecánica y coordinación de pits. |
| `vehiculos.html` | Catálogo de autos y motos con filtros visuales por categoría. |
| `cursos.html` | Programas, especialidades, precios en COP y tabla comparativa. |
| `agenda.html` | Formulario de solicitud de sesión y requisitos previos. |
| `contacto.html` | Datos de contacto, horarios, ubicación y planos ilustrados de las pistas. |

Todas las páginas comparten estilos, navegación, identidad de marca y estructura de pie de página.

## Tecnologías utilizadas

- **HTML5** para la estructura semántica.
- **CSS3** para diseño, transiciones y adaptación responsive.
- **SVG** para iconos locales de redes sociales.
- **Imágenes JPG, JPEG y PNG** para fotografía e ilustraciones.
- **Video MP4** para los avances usados en los testimonios.
- **Google Fonts** para Inter y Barlow Condensed.
- **CSS Grid** y **Flexbox** para la distribución visual.

El proyecto no utiliza frameworks, compiladores, gestores de paquetes ni bases de datos. Puede abrirse directamente en un navegador moderno.

## Estructura del proyecto

```text
drivesafe-academy/
|-- index.html
|-- sobre.html
|-- instructores.html
|-- vehiculos.html
|-- cursos.html
|-- agenda.html
|-- contacto.html
|-- README.md
|-- css/
|   |-- reset.css
|   |-- variables.css
|   |-- layout.css
|   `-- styles.css
`-- assets/
    |-- img/
    |   |-- hero-circuito.jpeg
    |   |-- disciplina-*.jpg
    |   |-- disciplina-*.jpeg
    |   |-- disciplina-*.png
    |   |-- instructor-*
    |   |-- *-pista.png
    |   |-- mapa-bucaramanga-*.png
    |   |-- avance-pista-*.mp4
    |   `-- otros recursos visuales
    |-- iconos/
    |   |-- facebook.svg
    |   |-- instagram.svg
    |   `-- youtube.svg
    `-- fuentes/
```

La carpeta `assets/fuentes/` está disponible para alojar tipografías locales, aunque el proyecto actualmente carga las fuentes desde Google Fonts.

## Cómo ejecutar el sitio

### Apertura directa

1. Abre la carpeta del proyecto.
2. Ejecuta `index.html` con cualquier navegador moderno.
3. Navega desde el encabezado a las diferentes secciones.

Este modo no requiere instalación ni configuración adicional.

### Visualización con Live Server

1. Abre la carpeta `drivesafe-academy` en Visual Studio Code.
2. Instala la extensión Live Server si todavía no está disponible.
3. Haz clic derecho sobre `index.html`.
4. Selecciona **Open with Live Server**.

Live Server permite recargar automáticamente los cambios y facilita revisar el sitio en distintas resoluciones.

## Arquitectura CSS

`styles.css` actúa como hoja principal y carga los demás archivos mediante `@import`:

```text
reset.css
  - Normalización básica.
  - Tamaño de caja.
  - Valores iniciales de tipografía y elementos.

variables.css
  - Colores de marca.
  - Tipografías.
  - Espaciado.
  - Sombras y bordes.
  - Variables de tema claro y oscuro.

layout.css
  - Contenedores.
  - Espaciado de secciones.
  - Foco visible.
  - Acciones, botones y enlaces.
  - Breakpoints de tabla, móvil y escritorio.

styles.css
  - Componentes específicos.
  - Encabezado y navegación.
  - Portadas.
  - Tarjetas.
  - Vehículos.
  - Cursos.
  - Formulario.
  - Mapas.
  - Pie de página.
```

Los nombres de clases incluyen variantes en inglés y español mediante selectores `:is(...)`. Esto permite mantener compatibilidad mientras se mejora progresivamente la nomenclatura.

## Diseño responsive

El proyecto usa una estrategia mobile-first complementada con breakpoints:

- Hasta 600 px: experiencia móvil.
- 601–768 px: ajustes de tableta y portadas.
- 601–992 px: cuadrículas de dos columnas y navegación intermedia.
- Desde 993 px: distribución completa de escritorio.

Entre los elementos adaptados se encuentran:

- Tamaño y altura del encabezado.
- Navegación principal.
- Titulares del hero.
- Cuadrículas de estadísticas.
- Tarjetas de disciplinas.
- Presentación de instructores.
- Catálogo de vehículos.
- Programas y especialidades.
- Comparativa en tabla.
- Layout de contacto.
- Formulario de agenda.
- Pie de página.

La tabla comparativa está dentro de un contenedor desplazable para evitar que se desborde en pantallas estrechas.

## Accesibilidad

El sitio incluye varias prácticas orientadas a mejorar su uso con teclado y tecnologías de asistencia:

- Etiqueta `lang="es"` en todas las páginas.
- Enlace **Saltar al contenido**.
- Jerarquía de encabezados.
- `aria-label` en navegación, redes sociales y contenido visual.
- Indicador visible de foco mediante `:focus-visible`.
- `aria-current="page"` en el elemento activo de navegación.
- Campos de formulario asociados a etiquetas mediante `for`.
- Leyendas y fieldsets para agrupar opciones.
- Campos obligatorios mediante HTML nativo.
- Hints y mensajes de ayuda junto a los campos sensibles.
- Respeto a `prefers-reduced-motion`.
- Control de reproducción disponible en los videos.
- Textos alternativos en imágenes informativas.

Como mejoras futuras se recomienda una auditoría completa con Lighthouse, axe o herramientas equivalentes.

## Contenido y configuración

### Precios

Los programas muestran precios en pesos colombianos (**COP**) dentro de `cursos.html`.

Antes de publicar se debe validar:

- Si los precios incluyen IVA.
- Qué incluye cada jornada.
- Cómo se cobra el equipo de seguridad.
- Qué ocurre si la pista cancela una sesión.
- Si existen tarifas por sesiones privadas.
- Si los valores pueden cambiar según temporada o disponibilidad.

### Contacto

Los datos principales se encuentran en `contacto.html`:

- Base de operaciones.
- Teléfono.
- Correo electrónico.
- Horario de atención.
- Prácticas según calendario.

Los enlaces sociales del pie de página actualmente apuntan a las páginas genéricas de las plataformas. Antes de publicar deben configurarse con las cuentas oficiales.

### Ubicación

Las imágenes ilustradas de contacto representan ubicaciones en Bucaramanga y sus alrededores. Deben reemplazarse por ubicaciones verificables si el sitio se utiliza públicamente.

## Formulario de agenda

El formulario de `agenda.html` incluye:

- Nombre completo.
- Correo electrónico.
- Número telefónico.
- Número de licencia.
- Categoría de licencia.
- Programa de interés.
- Fecha preferida.
- Experiencia del participante.
- Objetivo o comentario.
- Confirmación de requisitos.

El formulario usa validación HTML nativa y actualmente envía los datos a `action="#"`. Por lo tanto:

- Los datos no llegan a una base de datos.
- No se envían correos automáticamente.
- No existe confirmación persistente.
- No hay disponibilidad real de fechas.
- No hay procesamiento en servidor.

Para convertirlo en una reserva real se requiere integrar un backend, servicio de formularios, correo empresarial o API.

También se recomienda:

- Impedir fechas anteriores al día actual.
- Validar disponibilidad antes de confirmar.
- Preseleccionar el programa desde `cursos.html`.
- Evitar recopilar datos innecesarios.
- Añadir política de tratamiento de datos.
- Mostrar confirmación o número de solicitud.
- Conectarlo con WhatsApp o correo corporativo.

## Recursos visuales

### Imágenes

Los recursos gráficos se encuentran en `assets/img/`.

Incluyen:

- Imágenes de hero y disciplinas.
- Retratos del equipo.
- Vehículos de pista y motociclismo.
- Ilustraciones de circuitos.
- Avances de pista en video.
- Recursos para comunidad y eventos.

Se recomienda optimizar las imágenes grandes a formatos modernos como WebP y conservar dimensiones coherentes con su contenedor.

### Iconos

Los iconos sociales son SVG locales ubicados en `assets/iconos/`:

- Instagram.
- YouTube.
- Facebook.

### Fuentes

Las fuentes principales son:

- **Barlow Condensed** para titulares.
- **Inter** para textos generales.

Existen alternativas locales en el sistema:

- `Arial Narrow`.
- `Segoe UI`.
- Fuentes sans-serif genéricas.

## Limitaciones actuales

- No tiene backend ni persistencia de reservas.
- No existe conexión con calendario o sistema de pagos.
- Los enlaces sociales son marcadores generales.
- Los datos de contacto deben verificarse.
- Los testimonios y cifras deben validarse antes de uso comercial.
- Las certificaciones y experiencia mostradas deben corresponder a información real.
- Los precios de referencia deben aprobarse internamente.
- Las imágenes y ubicación deben revisarse antes de publicar.
- El sitio puede cambiar automáticamente al modo oscuro según el sistema operativo, sin que todas las páginas hayan sido optimizadas para ello.

## Mejoras recomendadas

### Prioridad alta

1. Integrar el formulario de reserva.
2. Añadir confirmación de solicitud y conservación de datos.
3. Conectar un calendario real de disponibilidad.
4. Sustituir redes sociales y datos de contacto genéricos.
5. Validar precios, políticas y requisitos legales.
6. Revisar el modo oscuro.

### Experiencia de usuario

- Convertir la navegación móvil en un menú desplegable.
- Preseleccionar el programa al llegar desde `cursos.html`.
- Añadir una sección de preguntas frecuentes.
- Incluir políticas de cancelación y reprogramación.
- Mostrar qué equipo incluye o excluye cada programa.
- Agregar disponibilidad aproximada o próximas fechas.

### Rendimiento

- Comprimir imágenes grandes.
- Convertir imágenes compatibles a WebP.
- Añadir dimensiones explícitas a las imágenes.
- Añadir `loading="lazy"` a recursos que no sean prioritarios.
- Mantener el `preconnect` de Google Fonts.
- Considerar alojar las fuentes localmente.

### SEO y publicación

- Añadir favicon en todas las páginas.
- Añadir metadatos Open Graph.
- Crear una imagen de vista previa para redes sociales.
- Añadir datos estructurados de LocalBusiness o Organization.
- Crear `robots.txt`.
- Crear `sitemap.xml`.
- Completar títulos y descripciones por página.
- Añadir enlaces canónicos.

## Personalización rápida

### Cambiar colores

Edita `css/variables.css`:

```css
:root {
  --primary: #B5121B;
  --secondary: #F04438;
  --accent: #8C959F;
  --ink: #101820;
  --paper: #F4F5F2;
}
```

### Cambiar la fuente

Modifica las variables en `css/variables.css`:

```css
--font-body: "Inter", "Segoe UI", sans-serif;
--font-display: "Barlow Condensed", "Arial Narrow", sans-serif;
```

### Cambiar precios

Los precios principales y la tabla comparativa se encuentran en `cursos.html`. Deben actualizarse ambos bloques para mantener la consistencia visual.

### Cambiar datos de contacto

Edita los enlaces `tel:` y `mailto:` dentro de `contacto.html` y el pie de página compartido de las páginas que corresponda.

### Cambiar el formulario

La estructura editable del formulario se encuentra en `agenda.html`. Su envío requiere definir un `action` válido y un método adecuado o integrar JavaScript con una API.

## Publicación

El proyecto puede alojarse en cualquier hosting de archivos estáticos, por ejemplo:

- GitHub Pages.
- Netlify.
- Vercel.
- Hosting compartido.
- Servidor web institucional.

Antes de publicar:

1. Verificar todos los enlaces internos.
2. Confirmar que todas las imágenes existen.
3. Revisar enlaces sociales y datos de contacto.
4. Optimizar recursos multimedia.
5. Completar metadatos SEO.
6. Validar el HTML.
7. Revisar móvil, tableta y escritorio.
8. Activar HTTPS.
9. Conectar el formulario a un servicio real.
10. Revisar requisitos legales y tratamiento de datos.

## Créditos

ASPHALT BUTCHER ACADEMY es un concepto visual desarrollado como sitio web estático multipágina.

Las imágenes, ilustraciones, nombres, cifras, testimonios, contactos y programas mostrados deben verificarse antes de utilizarse como una propuesta comercial real.
