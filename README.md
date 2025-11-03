# Proyecto Web: Café Rivoli (Soria)

Este repositorio contiene el código fuente completo del sitio web estático para el Café Rivoli, construido con HTML5, Tailwind CSS y Alpine.js.

## 🚀 Objetivo de la Web

1.  **Atraer Clientes:** Mostrar el ambiente, los productos estrella (vermut, pinchos) y la promoción de los jueves.
2.  **Vender el Negocio:** Informar de manera clara y destacada que el bar está en venta por 400.000€.

## 🔧 Cómo Personalizar y Editar el Contenido

La web está diseñada para ser editada fácilmente sin conocimientos de programación. Solo necesitas un editor de texto (como Visual Studio Code o incluso el Bloc de Notas) para abrir el archivo `index.html` y `legal.html`.

Busca y reemplaza los siguientes marcadores **[PLACEHOLDER]**:

### 1. Información de Contacto (¡Muy Importante!)

En `index.html` y `legal.html`:

* `[PLACEHOLDER_PHONE]`: Reemplaza por el número de teléfono principal (ej: `+34975123456`).
* `[PLACEHOLDER_EMAIL]`: Reemplaza por el email de reservas (ej: `reservas@caferivoli.com`).
* `[PLACEHOLDER_EMAIL_VENTA]`: Email para consultas sobre la venta (puede ser el mismo).
* `[PLACEHOLDER_WHATSAPP_NUMBER]`: Número de WhatsApp con prefijo país, sin "+" ni "00" (ej: `34975123456`).

### 2. Ubicación y Mapa

En `index.html` (Sección `#ubicacion`):

1.  `[PLACEHOLDER_CALLE_NUMERO]`: Pon la dirección completa (ej: `Plaza Mayor, 1`).
2.  `[PLACEHOLDER_GOOGLE_MAPS_LINK]`:
    * Busca la dirección en Google Maps.
    * Haz clic en "Compartir".
    * Copia el enlace y pégalo aquí.
3.  `[PLACEHOLDER_GOOGLE_MAPS_EMBED_URL]`:
    * Busca la dirección en Google Maps.
    * Haz clic en "Compartir".
    * Ve a la pestaña "Insertar un mapa".
    * Copia el enlace `src` que aparece dentro del `<iframe>` y pégalo aquí.

### 3. Textos y Personalización

En `index.html`:

* **Sección "Quiénes somos" (`#nosotros`):**
    * `[APELLIDO_FAMILIA]`: Apellido de la familia propietaria.
    * `[NOMBRE_PROPIETARIO]`: Nombre del dueño/gerente.
* **Sección "En Venta" (`#en-venta`):**
    * Rellena los campos `[XXX]` con los metros, aforo, etc.

### 4. Reseñas (Sección `#opiniones`)

He incluido 3 reseñas de ejemplo. Para reemplazarlas:

1.  Ve a tu ficha de Google Maps.
2.  Copia el texto de las mejores reseñas.
3.  Pégalas en el archivo `index.html`, reemplazando el texto de "Ana G.", "Javier M." y "Lucía F.".
4.  Cambia las estrellas (ej: `★★★★★`).
5.  `[PLACEHOLDER_GOOGLE_REVIEWS_LINK]`: Pon el enlace directo para "Ver todas las reseñas" en Google.

### 5. Enlaces y SEO (¡Importante!)

En `index.html`, `legal.html` y `sitemap.xml`:

* `[URL_ABSOLUTA_DE_TU_WEB]`: Una vez desplegada la web (ej: `https://www.caferivoli.com`), reemplaza este marcador en todas partes. Es crucial para el SEO y para que las imágenes de Open Graph (redes sociales) funcionen.
* `[PLACEHOLDER_INSTAGRAM_URL]`: URL de tu perfil de Instagram.
* `[PLACEHOLDER_FACEBOOK_URL]`: URL de tu perfil de Facebook.

### 6. Archivos PDF

En la carpeta `/assets/pdf/`:

1.  `carta.pdf`: Reemplaza este archivo por tu carta real.
2.  `dossier_venta.pdf`: Reemplaza este archivo por el dossier de venta.

### 7. Google Analytics (Opcional)

Si tienes un ID de Google Analytics 4:

1.  En `index.html`, al final del archivo, busca `[PLACEHOLDER_GA4_ID]`.
2.  Reemplázalo por tu ID (ej: `G-XXXXXXXXXX`).
3.  Descomenta (borra ``) ese bloque de código.

---

## 🚀 Opciones de Despliegue (Subir la Web)

### Opción A: Netlify (Recomendada - Fácil y Gratis)

Es la forma más sencilla de tener la web online gratis.

1.  **Crea una cuenta:** Ve a [Netlify.com](https://www.netlify.com/) y regístrate (puedes usar tu cuenta de GitHub/GitLab/Bitbucket si tienes, o email).
2.  **Sube la carpeta:** Una vez dentro de tu panel, ve a la sección "Sites". Simplemente **arrastra y suelta la carpeta completa `cafe-rivoli-website`** en el área indicada.
3.  **¡Listo!** Netlify te dará una URL aleatoria (ej: `ejemplo-raro-123.netlify.app`). Ya puedes visitar tu web.
4.  **Configurar Dominio (Opcional):** Si compras un dominio (ej: `caferivoli.com`), puedes ir a "Domain settings" en Netlify y seguir las instrucciones para apuntar tu dominio a Netlify (normalmente es cambiar las DNS).

**Gestión del Formulario (Automático con Netlify):**
El formulario de contacto (`<form name="contacto" ...>`) está preparado para Netlify. **No tienes que hacer nada.** Cuando alguien lo rellene, Netlify lo detectará automáticamente y te enviará un email a la dirección con la que te registraste. También podrás ver los envíos en la pestaña "Forms" de tu sitio en Netlify.

### Opción B: React + Tailwind + Vercel (Más compleja)

Esta opción es más escalable si en el futuro quieres un CMS (Gestor de Contenidos) para que el dueño edite la web sin tocar código.

1.  **Instalar Node.js:** Necesitas tener Node.js en tu ordenador.
2.  **Crear el proyecto:**
    ```bash
    npx create-react-app cafe-rivoli-react
    cd cafe-rivoli-react
    ```
3.  **Instalar Tailwind:**
    ```bash
    npm install -D tailwindcss postcss autoprefixer
    npx tailwindcss init -p
    ```
4.  **Configurar Tailwind:** Edita `tailwind.config.js` y `index.css`.
5.  **Construir la web:** Pasa todo el HTML de `index.html` a `App.js` (adaptando la sintaxis a JSX).
6.  **Desplegar en Vercel:**
    * Regístrate en [Vercel.com](https://vercel.com/) (similar a Netlify).
    * Conecta tu cuenta de GitHub/GitLab donde tengas el proyecto React.
    * Importa el repositorio.
    * Vercel detectará que es un proyecto React y lo desplegará automáticamente. El comando de *build* es `npm run build` y el directorio de salida es `/build` (Vercel suele saber esto solo).