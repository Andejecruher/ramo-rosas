# Para Arly: Nuestro Ramo de Amor

Experiencia web interactiva y responsiva creada como una dedicatoria personal para Arly. La página transforma un ramo de rosas amarillas en un recorrido de cinco momentos sobre el amor, la familia, la maternidad y la ingeniería civil.

## Descripción para GitHub

> Experiencia web romántica e interactiva con un ramo de rosas amarillas que florece paso a paso para celebrar el amor, la familia y una vida construida juntos.

## Qué incluye

- Pantalla de bienvenida con la dedicatoria principal.
- Recorrido secuencial de cinco mensajes poéticos.
- Una rosa amarilla SVG generada dinámicamente por cada paso.
- Indicador visual de progreso de `0/5` a `5/5`.
- Avance mediante botones o haciendo clic en la pantalla durante el recorrido.
- Animaciones ambientales: sol, aves, humo, flores, mascotas, brillo y celebración final.
- Estado final con ramo completo, listón rojo, confeti y carta de amor.
- Botón para reiniciar toda la experiencia.
- Diseño adaptable para escritorio, tablet y móvil.

## Vista previa

La captura de referencia está disponible en [`screen.png`](screen.png).

## Ejecutar localmente

No requiere Node.js, npm, bundler ni servidor de aplicaciones. Es una página estática.

1. Cloná o descargá el proyecto.
2. Abrí [`code.html`](code.html) directamente en un navegador moderno.
3. Presioná **Comenzar la Obra**.
4. Avanzá con **Plantar Rosa Siguiente** o haciendo clic fuera de los botones.
5. Al completar las cinco rosas, usá **Revivir la Obra** para empezar de nuevo.

También podés servir la carpeta con cualquier servidor estático local si preferís probarla desde `http://localhost`:

```bash
python3 -m http.server 8000
```

Luego visitá `http://localhost:8000`.

## Flujo de la experiencia

| Estado        | Resultado                                                                 |
| ------------- | ------------------------------------------------------------------------- |
| Bienvenida    | Presenta la dedicatoria y habilita el inicio.                             |
| Pasos 1 a 5   | Muestra un mensaje, actualiza el progreso y hace brotar una rosa.         |
| Ramo completo | Despliega la carta final, el listón rojo y una celebración de pétalos.    |
| Reinicio      | Limpia las rosas, el progreso y la celebración para repetir el recorrido. |

## Tecnologías

- HTML5 y CSS embebido.
- JavaScript vanilla para el estado, las transiciones y la interacción.
- SVG inline para las rosas, el sol, las aves y el listón.
- Tailwind CSS mediante CDN para utilidades visuales.
- Google Fonts mediante CDN: Epilogue, Plus Jakarta Sans, Dancing Script y Poppins.
- Material Symbols Outlined mediante CDN.

## Estructura

```text
.
├── code.html    # Página completa: estructura, estilos y lógica interactiva
├── DESIGN.md    # Dirección visual, paleta, tipografía y componentes
├── README.md    # Documentación del proyecto
└── screen.png   # Captura de referencia
```

## Personalización

El contenido principal se puede ajustar desde `code.html`:

- Los cinco mensajes y sus títulos están en `STEPS_DATA`.
- La dedicatoria inicial y la carta final están en el HTML.
- Los colores, fuentes y proporciones visuales están definidos en el bloque de estilos y en la configuración de Tailwind.
- Las animaciones de fondo y de las mascotas se encuentran en las reglas `@keyframes`.
- Las rosas se generan con `createYellowRoseSVG` y se plantan desde `plantRose`.

## Dependencias y consideraciones

La experiencia funciona sin conexión a un backend, pero necesita conexión a Internet para cargar Tailwind CSS, las fuentes de Google y Material Symbols desde sus CDNs. Si esos recursos no están disponibles, la interacción seguirá existiendo, aunque la apariencia tipográfica y parte del estilo pueden cambiar.

El proyecto no incluye un pipeline de build ni tests automatizados. La verificación recomendada consiste en abrir la página en un navegador moderno y recorrer los cinco pasos, el estado final y el reinicio en escritorio y móvil.

## Licencia

No se ha definido una licencia para este proyecto.
