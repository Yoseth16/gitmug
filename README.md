# GitMug

Web de presentación de **GitMug**, un termo inteligente **ficticio** para desarrolladores: una pantalla e-ink y un anillo LED que muestran de un vistazo el estado de tus pipelines de GitHub, GitLab y Jira.

> **Proyecto académico.** GitMug no es un producto real. Los formularios de reserva y contacto son demostrativos y no procesan pedidos ni envían datos.

## Proyecto

Trabajo realizado durante el ciclo de **DAW** (actividad ACT-RA1). Simula la presentación web de un producto relacionado con Git y CI/CD: landing, ficha de producto, explicación del funcionamiento, identidad de marca y reserva. El objetivo era practicar maquetación responsive, interacción con JavaScript y un sistema visual coherente.

## Características

- Landing page con visor **3D interactivo** del termo (sin modelos externos: la geometría se genera con Three.js).
- Estados **Passing / Failing** con cambio de LED y de pantalla en el modelo 3D.
- **Simulador de pantalla e-ink** con el flujo "Push update" (conexión, subida, verificación y refresco).
- Páginas de producto, cómo funciona y marca (cartel, paleta, tipografías y mini guía de estilo).
- **Presentación** del producto en un visor de 10 diapositivas (teclado, clic y pantalla completa).
- Vídeo promocional con controles propios de reproducción y sonido.
- Formularios de **reserva** y **contacto** con validación en el cliente (demo).
- Diseño **responsive** con menú móvil y respeto a `prefers-reduced-motion`.

## Tecnologías

- HTML5
- CSS / [Tailwind CSS](https://tailwindcss.com/) (versión CDN)
- JavaScript (sin frameworks)
- [Three.js](https://threejs.org/) (CDN)
- Google Fonts (Inter y JetBrains Mono)

## Estructura

```text
index.html          Landing con visor 3D y simulador e-ink
producto.html       Ficha de producto
como-funciona.html  Cómo funciona
marca.html          Identidad de marca y guía de estilo
presentacion.html   Visor de la presentación (10 diapositivas)
reserva.html        Formulario de reserva (demo)
contacto.html       Formulario de contacto (demo)
visor-3d.html       Visor 3D reutilizable (versión independiente)
img/                Imágenes de producto y cartel (WebP / JPG / PNG)
imagen web/         Imagen de fondo (img1.jpeg)
presentation/       Diapositivas y póster del vídeo (WebP)
Anuncio.mp4         Vídeo promocional
```

## Ejecutar localmente

No requiere instalación ni build. Todas las dependencias (Tailwind, Three.js y las fuentes) se cargan desde **CDN**, por lo que hace falta conexión a internet.

La forma más sencilla es servir la carpeta con un servidor estático, por ejemplo con Python:

```bash
python -m http.server 8000
```

y abrir <http://localhost:8000>. También puedes abrir `index.html` directamente en el navegador, aunque algunos navegadores limitan ciertas funciones cuando se abre desde `file://`.

## Nota

GitMug es un proyecto académico y el producto mostrado es ficticio. Los formularios y las funcionalidades de compra/reserva son demostrativos y no procesan pedidos reales.

## Autor

Yoseth Lopez
