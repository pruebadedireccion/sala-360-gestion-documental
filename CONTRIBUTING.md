# Contribución y mantenimiento

## Alcance

Este repositorio contiene la versión publicada de la experiencia 360°. Cualquier cambio debe conservar:

- El funcionamiento sin backend.
- La independencia de recursos externos para la escena.
- La accesibilidad básica por teclado.
- La alternativa táctil al control por movimiento.
- Los créditos y licencias de terceros.

## Antes de modificar

1. Confirmar el cambio funcional o de contenido.
2. Revisar si afecta nombres institucionales, mensajes o licencias.
3. Realizar una copia de seguridad del archivo que se va a modificar.
4. Mantener los cambios separados por tema.

## Validación mínima

Antes de publicar:

- [ ] `index.html` abre sin errores de JavaScript.
- [ ] La escena 3D se renderiza.
- [ ] Existen las cinco estaciones.
- [ ] Los nombres coinciden en rótulos, quioscos, paneles y navegación.
- [ ] El recorrido guiado visita todas las estaciones.
- [ ] El botón de música funciona.
- [ ] El modo 360° mantiene la cámara fija.
- [ ] La navegación táctil funciona sin sensores.
- [ ] La interfaz se adapta a móvil.
- [ ] No se agregaron recursos externos sin documentarlos.
- [ ] Se actualizó `CHANGELOG.md` cuando corresponde.

## Estilo de cambios

- Mantener la indentación de cuatro espacios.
- Conservar los comentarios en español.
- Evitar dependencias nuevas cuando una solución local sea suficiente.
- No incluir credenciales, tokens, datos personales ni rutas locales.
- No modificar archivos generados sin actualizar su origen.
- Documentar los recursos de terceros en `CREDITS.md`.

## Historial de Git

Se recomienda usar mensajes claros y en modo imperativo:

```text
Agregar control de volumen
Corregir orientación del modo 360
Actualizar guía de operación
```

## Publicación

```powershell
git add .
git commit -m "Descripción del cambio"
git push
```

Después de publicar, abrir la URL de GitHub Pages y comprobar que la versión nueva se está sirviendo correctamente.

## Recursos de terceros

No se debe incorporar música, tipografías, imágenes o bibliotecas sin:

1. Verificar que la licencia permita el uso previsto.
2. Registrar autor, título, fuente y licencia.
3. Conservar una copia de la evidencia de licencia.
4. Actualizar `CREDITS.md`.
