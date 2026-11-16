# YT Freedom

Interfaz web estática para reproducir videos permitidos mediante el reproductor oficial de YouTube y mostrar su sección de comentarios públicos.

## Estado actual

- Sin inicio de sesión ni cuenta propia de YT Freedom.
- Campo para pegar un enlace o ID de YouTube.
- Reproductor oficial incrustado.
- Panel de comentarios públicos con paginación.
- Diseño adaptable a PC y móvil.

## Reproducción y error 153

La página declara la política de referencia `strict-origin-when-cross-origin` en el documento y en el reproductor. YouTube necesita recibir una cabecera HTTP Referer (o una identificación equivalente del cliente) para permitir la reproducción incrustada.

Si aparece el error 153, comprueba que estás abriendo la página publicada de GitHub Pages y no la URL del iframe directamente. Si la red o el navegador administrado elimina esa cabecera o bloquea YouTube, el código de la página no puede forzar el acceso. En ese caso, usa YouTube por los medios autorizados o pide al administrador que permita el reproductor para un uso aprobado.

## Comentarios

Los comentarios proceden de la API oficial de YouTube Data API. Su disponibilidad depende de que el video tenga los comentarios habilitados y de la configuración válida de la API. No se inventan comentarios ni se muestran comentarios de videos distintos.

## Publicación

El archivo de entrada es `index.html`. El repositorio tiene GitHub Pages habilitado; conserva la configuración de publicación que ya existe.
