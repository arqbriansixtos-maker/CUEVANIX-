# Cuevanix

Aplicacion Android TV basada en WebView para navegar CuevanaPRO en pantalla completa.

## Incluye

- Inicio en `https://cuevanapro.org/`.
- Zoom visual nativo al 80 %.
- Navegacion por cursor con D-Pad y activacion con Enter/OK.
- Historial propio para rutas SPA y doble pulsacion de Back para salir.
- Soporte para reproductores en iframe, pantalla completa y controles multimedia.
- Bloqueo de solicitudes y capas publicitarias conocidas.
- Flujo de GitHub Actions que genera el APK debug como artefacto, sin instalar emulador.

## Compilar localmente

Abre la carpeta en Android Studio y ejecuta `assembleDebug`, o usa Gradle 8.7 con JDK 17:

```bash
gradle assembleDebug
```

El APK queda en:

```text
app/build/outputs/apk/debug/app-debug.apk
```

## Compilar con GitHub Actions

1. Crea un repositorio nuevo en GitHub.
2. Sube todo el contenido de esta carpeta a la rama `main`.
3. Abre la pestaña **Actions** y ejecuta **Build Cuevanix APK** si no inicia automaticamente.
4. Descarga el artefacto `Cuevanix-debug-apk` al terminar.

El workflow usa JDK 17 y Gradle 8.7. No instala Android Emulator, por lo que evita el error de descarga/descompresion del emulador.
