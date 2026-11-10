# Arquitectura técnica

## Resumen

La experiencia está implementada como una aplicación web estática de un solo archivo principal. No requiere backend, autenticación, base de datos ni proceso de compilación.

`index.html` contiene:

- Estructura HTML.
- Estilos de interfaz.
- Escena 3D construida con Three.js.
- Controladores de cámara.
- Recorrido guiado.
- Modo 360°.
- Reproductor de música.
- Iconografía y gráficos generados con Canvas.

Three.js está incluido dentro del archivo para evitar dependencias de CDN durante el evento.

## Tecnologías

- HTML5.
- CSS3.
- JavaScript.
- Three.js.
- WebGL.
- Web Audio API.
- Device Orientation API.
- Canvas 2D para texturas e iconos.

## Flujo de ejecución

```text
Carga de página
    ↓
Inicialización de escena y renderer
    ↓
Construcción de arquitectura, oficinas y estaciones
    ↓
Construcción de interfaz y enlaces de eventos
    ↓
Bucle de renderizado
    ↓
Interacción por mouse, toque, teclado o sensores
```

## Componentes principales

### Escena

La escena contiene:

- Piso con textura de concreto generada en Canvas.
- Oficina cerrada con techo, muros y fachada de vidrio.
- Escritorios, personal estilizado y paneles holográficos animados.
- Cinco pabellones distribuidos en círculo.
- Punto central de observación 360°.
- Recorrido luminoso circular.
- Iluminación ambiental, direccional y puntos de color por estación.

### Estaciones

Los datos de las estaciones se concentran en el arreglo `STATIONS`. Cada registro contiene:

- Identificador.
- Nombre y líneas del rótulo.
- Frase principal.
- Relato de impacto.
- Descripción.
- Color.
- Posición y rotación.
- Icono.

Los nombres se reflejan automáticamente en los rótulos 3D, quioscos, panel de información y navegación inferior.

### Cámara

Existen dos comportamientos:

- **Presentación:** cámara orbital elevada y acercamientos a cada pabellón.
- **360°:** cámara fija a 1,65 m de altura; solamente cambia la orientación.

La transición entre cámaras usa interpolación dependiente del tiempo para mantener una velocidad consistente en equipos rápidos y lentos.

### Sensores de orientación

El modo 360° utiliza `DeviceOrientationEvent`. La orientación se calibra respecto a la posición inicial del dispositivo y se convierte en una dirección de cámara sin desplazamiento.

Características:

- Permiso solicitado después de una acción del usuario.
- Recentrado manual.
- Límite de inclinación vertical.
- Desactivación automática al usar gestos táctiles.
- Alternativa completa mediante arrastre o deslizamiento.

### Recorrido guiado

El recorrido mantiene un índice de estación y un temporizador. Permite:

- Iniciar.
- Pausar.
- Reanudar.
- Avanzar.
- Detener.
- Regresar automáticamente a la vista general al finalizar.

La duración por estación se configura en `CONFIG.tourDuration`.

### Audio

La música se carga mediante `fetch` y se decodifica con Web Audio API. Esto permite:

- Reproducción en bucle.
- Control de volumen.
- Desvanecimiento al silenciar.
- Reanudación sin reiniciar la pista.

El archivo se sirve desde `audio/future-design.mp3`.

### Interfaz

La interfaz se construye con HTML y CSS sobre el canvas. Incluye:

- Barra inferior de estaciones.
- Panel de información.
- Controles de música e inmersión.
- Recorrido guiado.
- Controles específicos del modo 360°.
- Diseño adaptable a móvil.

## Rendimiento

Medidas aplicadas:

- Three.js incluido localmente.
- Texturas generadas en Canvas, sin descargas adicionales.
- Plantas creadas con `InstancedMesh`.
- Resolución de píxeles limitada a 1,75.
- Sombras suaves con un único foco direccional.
- Partículas de ambiente reducidas.
- Animaciones pausadas cuando el usuario prefiere movimiento reducido.

El rendimiento final debe validarse en dispositivos móviles reales.

## Privacidad

- No se solicita cámara.
- No se solicita micrófono.
- No hay backend.
- No hay cuentas ni formularios.
- No hay analítica de terceros.
- La orientación del dispositivo solo se usa localmente para controlar la cámara.

## Publicación

El repositorio se publica con GitHub Pages desde la rama `main`. El archivo `.nojekyll` mantiene el contenido estático sin procesamiento de Jekyll.

## Puntos de extensión

- Nuevas estaciones: agregar un registro en `STATIONS` y un constructor en `buildStationObject`.
- Nuevos textos: modificar `phrase`, `story` y `detail`.
- Nueva música: reemplazar `audio/future-design.mp3` y actualizar `CREDITS.md`.
- Nuevos idiomas: extraer los textos del arreglo `STATIONS` a archivos de traducción.
- Integración con servicios institucionales: implementar una capa de datos separada sin modificar la escena.
