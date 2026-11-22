# SmartRiohacha — Proyecto web académico

Prototipo web para registrar y visualizar reportes ciudadanos de baches y fallas de alumbrado público en Riohacha, basado en el documento **Proyecto Final - SmartRiohacha.pdf**.

## Funcionalidades incluidas
- Página de presentación del proyecto.
- Formulario para reportar baches o fallas de alumbrado.
- Captura de descripción, barrio/sector, nombre opcional, coordenadas y fotografía.
- Geolocalización del dispositivo (requiere permiso del navegador y HTTPS o localhost).
- Mapa para seleccionar la ubicación haciendo clic o moviendo el marcador.
- Mapa público con marcadores y filtros por tipo de incidencia.
- Listado de reportes recientes.
- Estadísticas de reportes pendientes, en revisión y resueltos.
- Panel de administración demostrativo para cambiar el estado.
- Diseño adaptable a computador y celular.

## Cómo ejecutarlo
1. Descomprime `SmartRiohacha.zip`.
2. Abre la carpeta `SmartRiohacha`.
3. Abre `index.html` en un navegador moderno.

Para que la geolocalización funcione de forma más consistente, ejecuta un servidor local desde esa carpeta:

### Opción Python
```bash
python -m http.server 8000
```
Luego abre `http://localhost:8000`.

### Opción VS Code
Instala la extensión **Live Server**, haz clic derecho en `index.html` y selecciona **Open with Live Server**.

## Tecnologías
- HTML5
- CSS3
- JavaScript
- Leaflet.js
- OpenStreetMap
- LocalStorage del navegador

## Importante: alcance del prototipo
Esta entrega es un prototipo funcional para demostración académica. Los reportes se guardan en el almacenamiento local del navegador; por tanto, no se comparten entre distintos dispositivos ni usuarios. El panel administrativo no tiene autenticación real. El mapa y las fuentes tipográficas externas necesitan conexión a internet.

El PDF plantea como evolución futura el uso de IoT (sensores de corriente y fotoceldas en luminarias) y Big Data/analítica para detectar patrones y priorizar mantenimiento. Esos componentes se presentan en la interfaz como visión de evolución, pero no se simula una conexión real con sensores ni con entidades públicas.

## Estructura
```text
SmartRiohacha/
├── index.html
├── styles.css
├── app.js
├── README.md
└── assets/
```

## Personalización
- Cambia textos, colores y distribución en `index.html` y `styles.css`.
- La ubicación inicial del mapa está definida en `app.js` mediante `riohacha`.
- Los tres reportes iniciales son datos de demostración y están definidos en `demoReports`.


## Galería e identidad visual
La carpeta `assets/` contiene el logotipo SVG y cuatro imágenes ilustrativas locales: portada costera, bache vial, alumbrado público y ciudad inteligente. No son fotografías documentales verificadas de puntos específicos de Riohacha. Para cumplir la propuesta de evidencia fotográfica local, sustitúyelas por fotografías propias de los sitios que hayan observado, conservando los mismos nombres de archivo.

## Abrir en Android
Dentro del ZIP también está `index-movil.html`, una versión que integra los estilos y el JavaScript en un único HTML. Descomprime el ZIP y abre ese archivo con Chrome. Las imágenes siguen dentro de `assets/`, por eso no debes mover el HTML fuera de la carpeta. El mapa necesita internet.
