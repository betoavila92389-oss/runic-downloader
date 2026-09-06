# Página de descargas de Runic Downloader

Página de presentación y **descargas** de *Runic Downloader*, una aplicación Android de
uso personal para bajar videos y música al teléfono y reproducirlos sin internet.

| Página | Para qué |
|---|---|
| [`index.html`](https://betoavila92389-oss.github.io/runic-downloader/) | Qué hace la aplicación y qué manda a internet (nada). |
| [`descargas.html`](https://betoavila92389-oss.github.io/runic-downloader/descargas.html) | La última versión y cómo se instala. |
| [`historial.html`](https://betoavila92389-oss.github.io/runic-downloader/historial.html) | Todas las versiones y qué trajo cada una. |

**Aquí no está el código de la aplicación**, solo la página. Los APK van en las
*releases* de este repositorio, con la etiqueta `v<versión>-<compilación>`.

## Los dos archivos que mandan

- **`version.json`** — la última versión. Lo lee la página **y también la propia
  aplicación**, desde *Ajustes → Versión de Runic*, para avisar cuando hay algo nuevo.
  Es una lectura y nada más: la app no envía ningún dato y nunca instala nada por su
  cuenta.
- **`historial.json`** — la lista completa, la más nueva arriba.

## Publicar una versión nueva

1. Subir `versionCode` y `versionName` en el proyecto de la app y generar el APK firmado.
2. Crear la *release* con la etiqueta `v<versión>-<compilación>` y subirle el APK.
3. Actualizar `version.json` **y** añadir el mismo bloque arriba de `historial.json`.

El orden importa: si `version.json` apunta a una release que todavía no existe, la app
ofrece una descarga rota.
