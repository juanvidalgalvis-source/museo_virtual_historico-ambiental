# El saqueo y su descanso

Museo virtual en 3D para la Actividad 3 de Impactos Ambientales (730078C), Universidad del Valle. Equipo 10: Jhon Edison Suescun Paz, Kevin Steven Trujillo Riascos y Juan Felipe Vidal Galvis.

Bloque temático: los imperios antiguos y el umbral medieval. Hilo conductor: qué relación existe entre la acumulación de excedentes agrícolas, la organización política y el deterioro ambiental en las civilizaciones antiguas, y por qué el Medioevo significó un relativo descanso del saqueo ecológico.

| Sala | Capítulo | Ambientación |
| --- | --- | --- |
| Sala I | 5. Grecia y los Estados comerciales | mármol, friso de meandros, columnas, olivos y un ánfora |
| Sala II | 6. Roma y los imperios comerciales | rojo pompeyano, friso de laurel, mosaico y una corona dorada |
| Sala III | 7. El Medioevo y el descanso del saqueo | piedra, vigas, vitrales, antorchas y una rueda de molino |

Cada sala tiene siete obras tomadas del capítulo, más una pieza en vitrina. El vestíbulo octogonal reúne las tres puertas, el mural de la fachada, un panel con el hilo conductor y otro con las instrucciones.

## Cómo abrirlo

El museo necesita un servidor local para que el navegador pueda cargar las fotos. No lo abras con doble clic sobre `index.html`.

Con Python, que ya viene en macOS:

```bash
cd museo_virtual_historico-ambiental
python3 -m http.server 8080
```

Luego entra en `http://localhost:8080` en Chrome, Firefox, Safari o Edge.

En VS Code también sirve la extensión Live Server: clic derecho sobre `index.html` y "Open with Live Server".

Three.js y las tipografías se descargan de internet la primera vez, así que hace falta conexión. Para presentar por Google Meet conviene abrirlo una vez antes para que quede en caché.

## Cómo poner las fotos

1. Copia las imágenes en `img/sala1`, `img/sala2` e `img/sala3`, numeradas de `01` a `07`.
2. Abre `config.js` y revisa cada obra: la ruta en `src`, el `titulo` que aparece en la cartela y el `texto` de la ficha.
3. Recarga la página.

Reglas útiles:

- Si `src` está vacío o la imagen no existe, se muestra un cuadro provisional con el número de la obra. El museo funciona igual.
- Cada sala admite hasta nueve obras. Con siete se usan dos en la pared del fondo, dos en cada lateral y una junto a la entrada.
- El marco se adapta solo a fotos horizontales o verticales. Entre 1200 y 2000 px de ancho se ven bien y cargan rápido.
- El título, el subtítulo, el hilo conductor y los nombres del equipo también se editan en `config.js`.
- El campo `estilo` de cada sala acepta `griego`, `romano` o `medieval`.

## Controles

| Acción | Teclado y ratón | Pantalla táctil |
| --- | --- | --- |
| Caminar | W A S D o flechas, Shift para correr | palanca de la izquierda |
| Mirar | mover el ratón | deslizar en la mitad derecha |
| Acercarse a una obra | clic o tecla E cuando la miras | tocar la obra |
| Volver del acercamiento | clic, E o Esc | tocar de nuevo |
| Ir a una sala | teclas 1, 2 y 3, la tecla 0 para el vestíbulo, o la barra inferior | barra inferior |

Para guiar el recorrido en vivo conviene usar las teclas 1, 2 y 3: la cámara vuela sola por el camino real hasta la sala, sin que haya que caminar.

## Archivos

- `index.html`: la escena 3D, la interfaz y las animaciones.
- `config.js`: todo el contenido editable, que es lo único que hay que tocar.
- `Fachada_museo.jpg`: ilustración de la portada y del mural del vestíbulo.
- `version_anterior_raycaster.html`: la primera versión del museo, guardada como referencia.
