# Biblioteca SPC v71 · iOS Media Bridge experimental

Versión experimental para probar reproducción con pantalla bloqueada en iPhone.

Cambios principales:

- Mantiene el reproductor SPC/WebAudio/WASM.
- Agrega un puente `MediaStreamDestination` hacia un elemento `<audio>` oculto.
- Agrega botón `Activar puente` para iOS.
- Agrega metadatos MediaSession básicos.
- Actualiza el Service Worker a cache v71.

Prueba recomendada:

1. Subir los archivos al repo.
2. Abrir `https://vesperoth.github.io/spc-player/?v=71` en iPhone.
3. Desactivar modo silencio físico del iPhone.
4. Tocar `Activar puente`.
5. Reproducir un tema.
6. Bloquear pantalla.

Si no funciona, la limitación probablemente está en la suspensión de WebAudio/WASM al bloquear iOS.
