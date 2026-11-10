# Guía de operación del evento

Esta guía resume la preparación y ejecución de la experiencia 360° durante una transmisión por Microsoft Teams.

## Roles recomendados

- **Presentador:** comparte la experiencia, controla el recorrido y explica cada estación.
- **Soporte técnico:** verifica el acceso, ayuda con permisos del celular y monitorea la transmisión.
- **Responsable de contenido:** valida nombres, mensajes institucionales y licencias.

Una misma persona puede asumir varios roles en un piloto, pero es recomendable separar la presentación del soporte.

## Antes del evento

### Una semana antes

- Confirmar los nombres oficiales de las cinco estaciones.
- Validar el mensaje institucional de los 100 años.
- Revisar y aprobar la música y la licencia documentada en `CREDITS.md`.
- Verificar que el repositorio y la cuenta de GitHub sigan activos.
- Preparar el enlace corto y la imagen QR oficial.

### Un día antes

- Abrir `https://pruebadedireccion.github.io/sala-360-gestion-documental/`.
- Ejecutar el recorrido guiado completo.
- Probar la música, el silencio y la reanudación.
- Abrir el modo 360° en un Android y en un iPhone.
- Probar el permiso de sensores concedido y rechazado.
- Comprobar el modo táctil.
- Abrir `qr.html` en el equipo que se usará para la presentación.
- Probar el QR con la cámara de un segundo dispositivo.

### El día del evento

- Cerrar aplicaciones que puedan consumir recursos gráficos.
- Conectar el equipo a energía.
- Verificar la conexión de red.
- Abrir la experiencia y `qr.html` antes de iniciar Teams.
- Comprobar que el audio del equipo esté configurado correctamente.
- Tener preparada una copia local de `index.html`.

## Flujo recomendado en Teams

1. Compartir la pantalla con la vista de presentación.
2. Mostrar `qr.html` durante la bienvenida.
3. Enviar también el enlace de acceso por el chat de Teams.
4. Explicar la diferencia entre la transmisión y la experiencia interactiva.
5. Iniciar el recorrido guiado.
6. Realizar pausas breves para explicar cada proceso.
7. Recordar al público que puede abrir la experiencia en su celular.

El QR funciona mejor para asistentes que ven Teams en un computador. Quienes siguen la transmisión desde su único celular deben usar el enlace enviado por el chat.

## Acceso desde el celular

1. Escanear el QR o abrir el enlace.
2. Pulsar **Entrar en 360°**.
3. Autorizar el movimiento si el navegador lo solicita.
4. Mover el celular para mirar alrededor.
5. Usar **Recentrar** si la orientación se desvía.
6. Utilizar los botones inferiores para seleccionar estaciones.
7. Si el movimiento falla, deslizar la pantalla.

La experiencia no accede a la cámara ni al micrófono.

## Audio

- La música inicia después de una interacción del usuario.
- En reuniones puede ser necesario compartir el audio del equipo.
- Regular el volumen antes de la transmisión para evitar saturación.
- Si no se desea transmitir música, desactivarla antes de compartir pantalla.

## Contingencia

| Situación | Acción |
|---|---|
| GitHub Pages no responde | Abrir la copia local de `index.html` desde un servidor HTTP de respaldo. |
| El movimiento no funciona | Continuar con navegación táctil y el recorrido guiado. |
| El QR no se lee en Teams | Enviar el enlace por el chat y mostrar el texto de la URL. |
| La música no carga | Continuar sin sonido; la experiencia 3D no depende del audio. |
| Baja fluidez | Cerrar otras aplicaciones y usar una resolución de pantalla menor. |
| El micrófono o el audio fallan | Continuar con la presentación visual y restablecer el audio de Teams. |

## Verificación final

- [ ] La URL abre por HTTPS.
- [ ] Las cinco estaciones están disponibles.
- [ ] El recorrido guiado funciona.
- [ ] La música se reproduce y se puede silenciar.
- [ ] El QR apunta a la experiencia.
- [ ] El enlace está disponible en el chat.
- [ ] Se probó el modo 360° en un celular real.
- [ ] Se conoce el procedimiento alternativo si fallan los sensores.
- [ ] Existe una copia local de respaldo.
- [ ] Se revisaron los créditos y licencias.
