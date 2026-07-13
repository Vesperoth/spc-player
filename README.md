# Biblioteca SPC PWA v68

Archivos para subir al repositorio `spc-player` y probar GitHub Pages / PWA en iPhone.

Contenido:
- `index.html`: reproductor SPC v67 con etiquetas PWA agregadas.
- `manifest.json`: metadatos para instalar como app en iOS/Android.
- `service-worker.js`: caché básico offline.
- `icons/`: íconos para pantalla de inicio.

Notas:
- El `index.html` pesa más de 25 MiB, por lo que puede fallar la subida por navegador. Si GitHub rechaza el upload web, usa GitHub Desktop o git por línea de comandos.
- Para probar como PWA real debe servirse por HTTPS, por ejemplo desde GitHub Pages.
- La reproducción con pantalla bloqueada en iOS no está garantizada; primero validar carga, reproducción y modo offline.
