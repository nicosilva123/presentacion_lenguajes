# Cambios — El ingeniero × IA (presentacionanimada.html)

Todo vive dentro del único archivo `presentacionanimada.html` (deck autocontenido,
sin dependencias). Backup en `.presentacionanimada.backup.html`.

---

## 1. Fix: contador doble
Había un HUD global `#hud` que se superponía con el contador integrado de cada slide
(lo de las fotos del "21/23"). Se ocultó el global (`#hud{display:none}`). Queda **un
único contador por slide**. El estilo "cuaderno manuscrito" del ingeniero quedó intacto.

## 2. Intro estilo Claude Code (terminal) en la slide 1
Al entrar a la portada corre una terminal de **Claude Code** (~8 s): `✻ Welcome to
Claude Code!`, el paper base como contexto, se escribe **"hacé la mejor presentación
para este paper"**, corren las líneas de trabajo (Read paper, tesis: polarización,
diseñando 23 slides, plantando easter eggs) y **revela la portada**.
- Saltar: botón o click en el fondo · Repetir: tecla **`i`** en la portada.

## 3. Easter eggs = muñequitos de Claude escondidos + código final
**9 muñequitos de Claude disfrazados**, escondidos y **visibles directo** en las slides
(no hace falta tipear nada). Flotan suavemente; al pasar el mouse se agrandan.

- Cada uno tiene un **disfraz** distinto: detective, recién recibido (birrete), mago,
  superhéroe (capa), modo relax (anteojos), traductor (auriculares), el que decide
  (corona), chef y modo fiesta.
- **Click** en uno → pop + ✓ + una frase, y te da **una letra del código**.
- Arriba a la izquierda se va armando el **código** a medida que los encontrás.
- **🏆 Al encontrar los 9** → confetti + tarjeta de premio con el **CÓDIGO FINAL:
  `INGENIERO`** y "rango desbloqueado · ingeniero PRO". El progreso se guarda en el
  navegador (`localStorage`).
- Están en las slides **3, 5, 6, 9, 11, 14, 17, 20 y 22**.

Otros: tipear **`claude`** (tarjeta "Hecho con Claude Code"), **`premio`** (re-mostrar
el premio), mensajes ocultos en la **consola** y en el **código fuente**.

---

## Cómo verlo
Abrí `presentacionanimada.html` en el navegador. Navegación: **← →** / espacio ·
**F** pantalla completa · **Home/End**.

## Notas técnicas
- 2 inserciones (CSS antes de `</style>`, `<script>` antes de `</body>`). El motor
  original (`render/go/fit`) no se tocó. Sin librerías; muñequitos en SVG inline,
  confetti en `<canvas>`. Backup: `.presentacionanimada.backup.html`.
