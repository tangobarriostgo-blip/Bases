# Tango de Barrio — Web 3.0 con panel de contenidos

Esta versión mantiene el diseño y las fotografías de la versión 2.0. **No está publicada ni conectada al dominio todavía.**

## Cómo funciona
- Sitio público: `index.html`, `assets/` y `content/site.json`.
- Panel de contenidos: **Pages CMS** (https://pagescms.org/), que edita archivos de un repositorio GitHub usando `.pages.yml`.
- Hosting: Netlify, conectado al repositorio GitHub para publicar cada cambio.
- Las imágenes nuevas se guardan en `assets/uploads/`; las fotografías originales permanecen en `assets/`.

## Pasos de instalación (una sola vez)
1. Crea una cuenta en GitHub, si no tienes una.
2. Crea un repositorio privado o público y sube **todos los archivos** de esta carpeta, incluida `.pages.yml` (archivo oculto). Para subir la carpeta completa, puedes usar GitHub Desktop o Git.
3. En https://pagescms.org/ inicia sesión con GitHub y autoriza el acceso al repositorio que contiene esta web. Selecciona el repositorio. Pages CMS reconocerá `.pages.yml`.
4. En Pages CMS abre **Contenido de la web**, cambia textos o fotografías y guarda. Los cambios quedan en GitHub.
5. En https://app.netlify.com/ crea un sitio nuevo mediante **Import an existing project**, elige GitHub y selecciona el mismo repositorio. No necesita comando de compilación; directorio de publicación: `.`.
6. Comprueba primero la URL de prueba de Netlify. Luego agrega `tangodebarrio.cl` y `www.tangodebarrio.cl` en Domain management y configura los registros DNS **según las instrucciones específicas de Netlify** en el proveedor donde compraste el dominio. No cambies DNS hasta comprobar la URL de prueba.
7. Verifica HTTPS, la portada, el panel, la galería y el acceso desde celulares.

## Cómo cambiar fotografías
En Pages CMS > Contenido de la web, abre **Fotografía de portada** o **Fotografía del equipo docente** y selecciona/sube una imagen. En **Fotografías de la galería** agrega una entrada por foto. Guarda. GitHub recibirá los cambios y Netlify volverá a publicar.

## Importante
- El panel se usa desde pagescms.org, **no** desde `/admin` del sitio.
- Los permisos del panel dependen de tu cuenta GitHub; no compartas contraseñas.
- Si abres `index.html` con doble clic, los textos de ejemplo se muestran, pero las actualizaciones del archivo JSON pueden no cargarse por las restricciones del navegador con `file://`. Para probar localmente, ejecuta `python -m http.server 8000` en esta carpeta y abre http://localhost:8000.
- Antes de publicar, confirma horarios, ubicación, WhatsApp e Instagram. No se han inventado estos datos.
- La compatibilidad y las opciones exactas del servicio Pages CMS deben comprobarse al conectarlo; puede requerir ajustar `.pages.yml` si su configuración cambia.
