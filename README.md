# Ruta Ley N° 31071

Sitio estático para compartir una guía interactiva con funcionarios de municipalidades.

## Qué incluye

- Ruta por fases con detalle al hacer clic.
- Fase previa de fortalecimiento de capacidades e incidencia institucional.
- Biblioteca pública de documentos del Drive con filtros por modelos, casos, guías, normativa, herramientas y difusión.
- Asistente documental basado en palabras clave para entregar modelos, enlaces y orientación por proceso.
- Simulador didáctico `Juego31071/juego.html` donde un funcionario municipal practica la implementación real de la Ley N° 31071: encargo de alcaldía, expediente, COMPRAGRO, PAC, requerimiento, convocatoria, pago y reporte.
- Portal para agricultores con preparación de requisitos, avance y borrador de propuesta.
- Fotografías y logos incluidos en la carpeta `assets`.
- La guía y los asistentes funcionan sin cuenta de ChatGPT. El formulario envía solicitudes al Apps Script configurado en `app.js`.

## Volver a subir la web

El paquete `web-ley31071-actualizada-2026-10-07.zip` contiene los archivos listos para publicar.

1. Descomprime el ZIP.
2. Sube todo su contenido al alojamiento de tu web, conservando los nombres de las carpetas.
3. Deja `index.html` en la raíz del sitio y abre la dirección publicada.

Debes subir `index.html`, `app.js`, `assets`, `Agicultores` y `Juego31071` juntos. La guía municipal utiliza `Agicultores/styles.css`; no cambies ese nombre ni muevas ese archivo.

Para revisar la web en tu computadora, abre `index.html`. Desde ahí puedes entrar al portal para agricultores y al simulador.

## Publicación gratuita

La opción más simple, sin configurar repositorio, es Netlify Drop:

1. Entrar a `https://app.netlify.com/drop`.
2. Subir la carpeta descomprimida completa, con `index.html`, `app.js`, `assets`, `Agicultores` y `Juego31071`.
3. Compartir la URL pública generada.

Para mantener versiones y hacer mejoras continuas, recomiendo GitHub Pages:

1. Crear un repositorio público.
2. Subir todos los archivos y las carpetas del paquete conservando su estructura.
3. Activar Pages desde `Settings > Pages > Deploy from branch`.
4. Compartir la URL pública con las municipalidades.

También puede insertarse como enlace dentro de un Google Site institucional.

## Futuras mejoras

- Reemplazar el asistente por un chatbot con IA cuando exista presupuesto.
- Agregar más modelos editables al Drive y registrarlos en `app.js`.
- Añadir descarga directa de documentos en Word/PDF si se consolidan versiones finales.

## Mantenimiento de documentos

Carpeta de referencia actualizada el 7 de octubre de 2026:

https://drive.google.com/drive/folders/171LfjkNa92oegevenwDp_PuJsyBqlfeO?usp=sharing

La biblioteca contiene 15 enlaces a los archivos encontrados en esta carpeta. Las resoluciones de Vice, Cristo Nos Valga y Bellavista de la Unión se presentan como casos de referencia.

Cada documento de la biblioteca está registrado en `app.js`, dentro de `resources`.
Para agregar un nuevo archivo del Drive, copia su enlace público, crea un nuevo objeto con
`title`, `type`, `tag`, `category`, `description`, `url` y `keywords`, y vuelve a publicar el sitio.

## Formulario

Se conserva la URL de Apps Script que estaba configurada. Esta entrega actualiza los enlaces documentales; no cambia el servidor ni la hoja de solicitudes. Consulta `integracion-google-sheet-asistencia.md` para revisar los campos y el destino configurado.
