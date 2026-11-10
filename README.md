# Sala 360 — Gestión Documental

Experiencia virtual 360° para funcionarios, publicada con GitHub Pages.

## Dirección pública

Experiencia:

https://pruebadedireccion.github.io/sala-360-gestion-documental/

Pantalla con QR para compartir en Teams:

https://pruebadedireccion.github.io/sala-360-gestion-documental/qr.html

## Uso

- **Vista de presentación:** composición general y recorrido guiado para compartir pantalla en Teams.
- **Entrar en 360°:** punto de observación fijo para celulares.
- La música de fondo inicia al entrar y puede activarse o desactivarse con el botón **Activar/Desactivar Música**.
- El control por movimiento requiere HTTPS y autorización del navegador.
- Si el movimiento no está disponible, se puede deslizar la pantalla.

## Archivos

- `index.html`: experiencia completa. Three.js está incluido en el archivo.
- `audio/future-design.mp3`: música de fondo en bucle.
- `qr.html`: pantalla para mostrar el QR durante la transmisión.
- `qr.png`: código QR listo para PowerPoint u otros materiales.
- `qr.svg`: versión vectorial del QR.
- `CREDITS.md`: fuente y licencia de la música.

## Actualización

Sustituir `index.html` por la nueva versión y subir los cambios:

```powershell
git add .
git commit -m "Actualizar experiencia"
git push
```

GitHub Pages publicará los cambios automáticamente.
