# Retumbero Store

Catálogo de las apps de Retumbero. La app **Retumbero Store** lee `catalog.json`
de este repositorio y baja los APK desde las *Releases*.

## Cómo publicar una versión nueva

1. Compila el APK firmado.
2. En GitHub: **Releases → Draft a new release**, etiqueta `playbeat-2.0.35`,
   y arrastra el `.apk` como archivo adjunto.
3. Calcula el SHA-256 del APK: `sha256sum PlayBeat-2.0.35-166.apk`
4. Edita `catalog.json`: pon `versionName`, `versionCode`, `sizeBytes`,
   `sha256` y la `downloadUrl` de la Release
   (`https://github.com/saenzkissinger982-ship-it/Retum-Store/releases/download/<etiqueta>/<archivo>.apk`).
5. Haz commit. La tienda lo ve en cuanto lo abres.

## Añadir otra app

Agrega otro objeto dentro de `apps` en `catalog.json` con los mismos campos.

## Importante

El repositorio tiene que ser **público**, o la tienda no podrá leer el catálogo
ni bajar los archivos sin iniciar sesión.
