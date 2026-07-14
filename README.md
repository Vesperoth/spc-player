# Biblioteca SPC v72 · iOS pulido

Esta versión mantiene el puente que permitió reproducir SPC con el iPhone bloqueado.

Cambios:

- El puente se activa automáticamente con el primer toque en Play/Random.
- La barra flotante `Activar puente` ya no queda sobrepuesta al reproductor.
- La activación permanece durante la carga actual de la PWA. Si iOS cierra por completo la app, el primer Play vuelve a activarla automáticamente.
- Pause limpio: pausa primero el elemento multimedia y luego el motor WebAudio para evitar el bucle de milisegundos.
- MediaSession informa título, autor, álbum, duración y posición.
- Agrega acciones de seek ±10 s / seek directo cuando iOS las expone.
- Pausa animaciones visuales mientras la PWA está en segundo plano.

## Actualización en GitHub Pages

1. Reemplaza los archivos del repositorio por los de este paquete.
2. Commit sugerido: `v72 pausa iOS y tiempo MediaSession`.
3. Push origin.
4. Abre `https://vesperoth.github.io/spc-player/?v=72`.
5. Si el acceso de inicio conserva la versión anterior, elimínalo y agrégalo nuevamente.

## Carátulas por álbum

La v72 ya incluye soporte en MediaSession. Por ahora usa el ícono general como respaldo.
Cuando existan imágenes específicas se puede definir:

```js
window.SPC_ALBUM_ART = {
  "Vip and Wall Mix 3": "./artwork/vip3.png",
  "Vip and Wall Mix 4": "./artwork/vip4.png",
  "Vip and Wall Mix 5": "./artwork/vip5.png",
  "Vip and Wall Mix 6": "./artwork/vip6.png"
};
```

Las imágenes recomendadas son PNG cuadradas de 512 × 512.


Actualización v73: prueba de carátulas por álbum VIP (VIP3, VIP4, VIP5, VIP6) para Media Session / pantalla bloqueada en iPhone.


Actualización v74: carátulas VIP con fondo extendido, controles Anterior/Siguiente en iOS, metadata Tema/Origen/Autor y reactivación suave al desbloquear.


## v75
- El puente de audio iOS sigue activo automáticamente, pero su banner/toast queda totalmente oculto para no cubrir el reproductor.
- Conserva pausa limpia, reproducción bloqueada, controles anterior/siguiente, tiempo y carátulas VIP de la v74.


## v76
- Oculta en la interfaz el error opaco `Script error.` emitido ocasionalmente por WebKit/iOS.
- Los errores reales con detalle siguen mostrándose y quedan registrados en consola.


Actualización v77: reanudación directa y reforzada desde Play en la pantalla bloqueada de iOS.


## v78
- Corrige la pausa/reanudación desde la pantalla bloqueada en modo PWA standalone.
- Congela la posición de MediaSession durante pausa y pausa directamente el backend SPC.
