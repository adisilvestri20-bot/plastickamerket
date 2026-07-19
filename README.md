# PlasticMarket — Sitio web

Sitio web corporativo de **PlasticMarket** (Chile / EE.UU.), fabricante especializado en matricería, inyección, extrusión y coextrusión de plástico y caucho, con compuesto antibacterial certificado.

## Contenido del proyecto

- `PlasticMarket.dc.html` — Componente de diseño (editable en este entorno). Fuente de verdad del sitio.
- `PlasticMarket - Standalone.html` — Versión **autocontenida**: un solo archivo HTML con todo incrustado (imágenes, estilos, scripts). Funciona offline, ideal para enviar por correo o abrir localmente sin servidor.
- `export/` — Paquete de despliegue en carpeta: `index.html` + `support.js` + `image-slot.js` + `assets/` + `robots.txt` + `sitemap.xml`. Ideal para subir tal cual a un hosting (Netlify, Vercel, GitHub Pages, cPanel, etc.).
- `assets/` — Imágenes fuente del proyecto (logo, productos, marcas, banner, certificado).
- `robots.txt` / `sitemap.xml` — Archivos SEO técnico, ya configurados con las URLs del dominio `plastic-market.com`.

## Estructura de la página

1. **Portada** — imagen/video de fondo, botones "Cotizar por WhatsApp" y "Ver productos".
2. **Quiénes somos** — historia, años de trayectoria, presencia CL/EE.UU., certificado LLC.
3. **Servicios** — Matricería, Inyección, Extrusión, Coextrusión (cada uno cotiza por WhatsApp o correo).
4. **Compuesto antibacterial** — diferenciador de marca, medalla "Únicos en Chile", áreas de mayor cotización.
5. **Productos y Proyectos** — grilla de productos con imagen completa y modal de "Ver más información" (detalle + cotizar).
6. **Franja de marcas** — logos de clientes/colaboradores en carrusel animado.
7. **Contacto** — formulario que envía a WhatsApp y/o correo (`ventas@plastic-market.com`), datos de contacto, mapas de Chile y EE.UU. (Google Maps embebido).
8. **FAQ** — preguntas frecuentes (materiales, antibacterial, importación/exportación, cotización).
9. **Footer** — navegación, contacto, redes.

## Funcionalidades

- **Selector de idioma** (Español / English) en la barra superior — traduce toda la interfaz en un clic.
- **Cotización dual**: cada botón de cotizar ofrece WhatsApp (mensaje prellenado) y correo electrónico.
- **Imágenes editables**: los recuadros de producto, logo y marcas usan un componente de arrastrar-y-soltar — el usuario puede reemplazar cualquier imagen directamente en el editor.
- **Animaciones de scroll**: textos, tarjetas e imágenes aparecen con fundido al hacer scroll.
- **Responsive**: se adapta a mobile (menú hamburguesa, grillas de 1 columna).

## Cómo publicarlo

### Opción A — Un solo archivo (más simple)
Sube `PlasticMarket - Standalone.html` a cualquier hosting o ábrelo directo en el navegador. No necesita servidor ni configuración.

### Opción B — Carpeta de despliegue (recomendada para SEO)
Sube el contenido completo de `export/` a la raíz de tu hosting, conservando la estructura de carpetas (`assets/` debe quedar como subcarpeta). Incluye `robots.txt` y `sitemap.xml` para indexación en buscadores.

**Antes de publicar en producción:**
- Reemplaza el número de WhatsApp de prueba y verifica los correos de contacto.
- Sube `portada.mp4` en la raíz si quieres el video de portada animado (hoy se usa una imagen de respaldo).
- Actualiza `sitemap.xml`/`robots.txt` si cambias el dominio real.
- Reemplaza los logos de marcas placeholder por los definitivos si aún faltan.

## Pila técnica

HTML + CSS inline + JavaScript (React vía runtime propio `support.js`). No requiere build ni Node — es 100% archivos estáticos.
