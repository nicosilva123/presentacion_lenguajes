# Cambios — El ingeniero × IA (presentacionanimada.html)

Deck autocontenido en `presentacionanimada.html`. Backup en `.presentacionanimada.backup.html`.

## 1. Contador
Se **eliminó** el contador "NN/23" de arriba a la derecha de todas las slides
(`.hud .idx{display:none}`). Queda la barra de progreso abajo.

## 2. Intro estilo Claude Code (terminal)
Slide 1: terminal de Claude Code con **fondo claro** (crema, como la referencia),
**tipeo lento** y **más tiempo** para leer la línea de los easter eggs antes de
revelar la portada. Adjunta el paper base y escribe "hacé la mejor presentación
para este paper". Saltar con click/botón · repetir con tecla `i`.

## 3. Easter eggs = Clawd escondido + código secreto + premio
- **6 Clawd** (la mascota oficial de Claude Code, el bloque naranja con ojos `><`)
  escondidos en las slides **3, 6, 8, 13, 16 y 20**, animados (flotan), en distintos
  tamaños/rotaciones. Visibles directo (no hace falta tipear nada).
- **Click** en cada Clawd → da **un dígito** del código. Arriba a la izquierda se
  arma el código a medida que los encontrás.
- Al encontrar **los 6** → se revela el **código secreto: `482026`** (Opus 4.8 · 2026).
- **"Gritá" el código**: si alguien **escribe `482026`** con el teclado → pantalla
  **🎉 ¡GANASTE!** ("mostrá esta pantalla a Martín o Nico y reclamá tu premio").
- Extras: tipear `claude` (tarjeta), progreso guardado en `localStorage`.

## 4. Contenido actualizado según el paper nuevo
(`Paper_Rol_del_ingeniero_informatico_en_10_anios.pdf`)
- **SWE-bench Verified**: corregido **14% → 89%** (el paper dice ~89%, no 95%).
  Barras: 14 · 49 · 72 · 82 · 89. (El deck ahora tiene 22 slides: se quitó la de predicciones históricas.)
- Se quitó **"prima salarial"** del cierre (no está respaldado por el paper).
- Confirmados con el paper: programador puro **−6%**, desarrollador **+15%** (BLS),
  WEF +170M/−92M (saldo neto +78M), problema del 70% (Osmani), Amodei 90%, Altman.
- Nota: la cronología COBOL/4GL/RAD/offshore/low-code es contexto propio del talk
  (el paper menciona COBOL, 4GL y low-code pero sin esos años ni RAD/offshore).

## Cómo verlo
Abrí `presentacionanimada.html` en el navegador. **← →** / espacio · **F** fullscreen.

## 5. Notificaciones de Claude (tecla N)
Durante la charla, apretar **N** hace salir desde el **centro-derecha** una
**notificación de Claude** estilo mini-terminal de Claude Code (semáforos, avatar
Clawd, ✻ "Claude Code", barra de progreso con auto-cierre a 4.5s). Cada N avanza
al siguiente de **10 mensajes** (chistes 4ta-pared: micrófono, tokens, los 6 Clawd,
482026, "no vine a reemplazarlos, vine a tomar asistencia", etc.).
- Funciona **siempre en local** (también en la URL pública).
- En **modo control** (`?control=`) se **sincroniza** por Supabase (broadcast
  `claudenotif`, mismo patrón que el gameplay): el que aprieta N la muestra en la
  pantalla proyectada del otro presentador.
- `N` no choca con navegación / `F` / `i` / `V` ni con los buffers `claude`/`premio`/dígitos.
