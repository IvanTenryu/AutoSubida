# AutoSubida TikTok (Google Drive + Apps Script)

Automatización ligera en **Google Apps Script** para subir videos desde una carpeta de Google Drive a los borradores de TikTok usando la API oficial (**TikTok Content Posting API**).

## Cómo funciona
1. Revisa una carpeta de origen (`Pendientes`) en Google Drive.
2. Toma el siguiente video disponible (`.mp4`, hasta 50 MB).
3. Lo sube a los borradores (Inbox) de TikTok mediante OAuth 2.0.
4. Mueve el archivo procesado a la carpeta `Subidos` para evitar duplicados.
5. Se ejecuta automáticamente según el horario configurado en los activadores de Apps Script.

## Requisitos
* Cuenta en [TikTok for Developers](https://developers.tiktok.com/) con **Login Kit** y **Content Posting API** habilitados.
* Proyecto en [Google Apps Script](https://script.google.com/) con la biblioteca oficial de **OAuth2** (`1B7FSrk5Zi6L1rSxxTDgDEUsPzlukDsi4KGuTMorsTQHhGBzBkMun4iDF`).
* Dos carpetas en Google Drive (`Pendientes` y `Subidos`).

## Configuración rápida
1. Configura la **Redirect URI** en tu app de TikTok:
   `https://script.google.com/macros/d/TU_SCRIPT_ID/usercallback`
2. Reemplaza `CLIENT_KEY`, `CLIENT_SECRET`, `ID_PENDIENTES` e `ID_SUBIDOS` en `Código.gs`.
3. Ejecuta la función `autorizar()` una vez para vincular tu cuenta de TikTok.
4. Crea un activador por tiempo para la función `subirVideoATikTok()`.

## Documentación legal (GitHub Pages)
* [Términos de Servicio](./terms.html)
* [Política de Privacidad](./privacy.html)
