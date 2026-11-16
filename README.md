# YT Freedom Player

Aplicación web ligera y adaptable para abrir videos mediante el reproductor oficial de YouTube. Está pensada para publicarse como sitio estático en GitHub Pages.

## Funciones actuales

- Abrir videos pegando un enlace o un ID de YouTube.
- Reproductor oficial incrustado.
- Historial reciente y favoritos guardados en el navegador.
- Inicio y cierre de sesión con Google mediante Firebase Authentication.
- Diseño adaptable a escritorio y móvil.

## Activar el inicio de sesión con Google

1. Crea un proyecto en [Firebase Console](https://console.firebase.google.com/).
2. En el proyecto, registra una aplicación web y copia su objeto de configuración.
3. Abre **Authentication → Sign-in method** y activa **Google**. Guarda los cambios.
4. En **Authentication → Settings → Authorized domains**, añade este dominio:
   `10574084-cmd.github.io`
5. En los ajustes del proyecto, busca la configuración de tu aplicación web.
6. En `index.html`, reemplaza los valores de ejemplo de `firebaseConfig` por los valores reales de tu aplicación web:
   - `apiKey`
   - `authDomain`
   - `projectId`
   - `appId`
7. Guarda el cambio en la rama `main` y espera a que GitHub Pages publique la actualización.

La configuración web de Firebase está diseñada para incluirse en el navegador. **No** publiques claves privadas, archivos JSON de cuentas de servicio ni credenciales de Firebase Admin.

El acceso usa Firebase Authentication para crear una sesión de la aplicación y mantenerla entre recargas. No inicia sesión en YouTube ni concede permisos para dar Me gusta, publicar comentarios o administrar suscripciones.

## Límites

- La reproducción depende del reproductor oficial de YouTube y de que el video permita la inserción.
- La aplicación no actúa como proxy ni evita bloqueos de red, controles escolares, restricciones de cuenta o límites de YouTube.
- La búsqueda interna, los comentarios, los Me gusta de YouTube y las suscripciones todavía no están implementados. Requieren integración con las API oficiales y los permisos correspondientes.
- El historial y los favoritos actuales se guardan localmente en el navegador; no se sincronizan entre dispositivos.

## Publicación

Mantén la configuración de GitHub Pages y el workflow de Actions que ya tiene el repositorio. El archivo principal de la aplicación es `index.html`.

## Documentación oficial

- [Firebase: iniciar sesión con Google en JavaScript](https://firebase.google.com/docs/auth/web/google-signin)
- [Firebase: añadir Firebase a un proyecto web](https://firebase.google.com/docs/web/setup)
