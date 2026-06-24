# Cambios — El ingeniero × IA (presentacionanimada.html)

Todo vive dentro del único archivo `presentacionanimada.html` (deck autocontenido,
sin dependencias). Backup en `.presentacionanimada.backup.html`.

---

## 1. Fix: el contador "se veía mal" (contador doble)

Cada slide ya traía su propio contador integrado al marco, pero además había un HUD
**global** `#hud` fijo arriba a la derecha → los dos números quedaban **superpuestos**
(lo que mostraban las fotos del "21/23"). Se ocultó el global con una regla CSS
(`#hud{display:none}`). Queda **un único contador por slide**. El estilo "cuaderno
manuscrito" de las slides del ingeniero es intencional y quedó intacto.

---

## 2. Intro estilo **Claude Code** (terminal) al principio de la slide 1

Al entrar a la portada se reproduce una terminal de **Claude Code** (~8 s), igual que
en la landing de referencia:

```
✻ Welcome to Claude Code!
/help for help · /status for your current setup
cwd: ~/el-ingeniero-x-ia
⎿ contexto: el-futuro-del-ingeniero-frente-a-la-IA.pdf · paper base · 14 págs

> hacé la mejor presentación para este paper        [Enter] to send

● Read el-futuro-del-ingeniero-frente-a-la-IA.pdf (14 págs)
● Tesis detectada: polarización, no reemplazo
● Diseñando 23 slides…
● Plantando easter eggs ✦
✻ Listo. Armé la presentación completa a partir del paper.
  Escondí varios ✦ por las slides — premio para quien los encuentre todos 👀
```

Después la terminal se desvanece y **revela la portada**.
- **Saltar:** botón "saltar intro" o click en el fondo.
- **Repetir:** con la slide 1 abierta, tecla **`i`**.
- Sólo se reproduce la primera vez (no molesta si volvés atrás durante la charla).

---

## 3. Easter eggs animados + **premio**

Cosas que dejó escondidas Claude, pensadas para quien explore la presentación después. Todo es opt-in (no interfiere con la exposición en vivo).

| Trigger | Qué hace |
|---|---|
| Escribir **`eggs`** | Modo búsqueda: los **✦ flotan y brillan** en las slides (animados). |
| **Click en un ✦** | Pop + onda + frase escondida (toast) firmada por Claude; el ✦ queda verde (encontrado). |
| Escribir **`claude`** | Tarjeta "✻ Hecho con Claude Code" (cerrar con `Esc`). |
| Escribir **`premio`** | Vuelve a mostrar el premio. |
| Tecla **`i`** en la portada | Repite el intro. |
| **Consola** (F12) / **ver código fuente** | Mensajes ocultos de Claude. |

**Los ✦ (9 en total):** repartidos en las slides
**3, 5, 6, 9, 11, 14, 17, 20 y 22**, casi invisibles
hasta que los buscás (`eggs`) o pasás el mouse. Flotan suavemente y brillan.

**🏆 Premio:** al encontrar **los 9**, salta **confetti** + una tarjeta de premio
("¡Los encontraste todos! · rango desbloqueado · ingeniero PRO ✦"). El progreso se
guarda en el navegador (`localStorage`), así que no se pierde si recargás.

---

## Cómo verlo
Abrí `presentacionanimada.html` en el navegador. Navegación: **← →** / espacio ·
**F** pantalla completa · **Home/End**.

## Notas técnicas
- 2 inserciones: un bloque CSS antes de `</style>` y un `<script>` antes de `</body>`.
  El motor original (`render/go/fit`) no se tocó. Sin librerías nuevas.
- El logo/marca de Claude se reutiliza del propio deck; el confetti es un `<canvas>`
  liviano sin dependencias.
- Backup: `.presentacionanimada.backup.html`.
