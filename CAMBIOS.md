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

## 6. Bloques 2 y 4 — rediseño completo (arco 7 + 7)
Reescritos siguiendo el guion del usuario (`SLIDES_bloques_2_4.md`), con el sistema
de diseño del deck (kicker mono · título-aserción · un protagonista visual · footer
serif itálico · chrome). Se sumó un **pos-it amarillo** (Caveat) como elemento nuevo.

**Bloque 2 — El presente de la IA** (acento teal `#0E9FB5`, 7 slides):
1. *En dos años pasó algo que no había pasado nunca* — 1,96% → 88,6% (Devin→Opus) + pos-it "el benchmark se saturó".
2. *La adopción más rápida de la historia* — 20.000.000 (fantasma 20M) + chips Google 75% / MS 20–30% / 84% devs + pos-it "lo aprueban ingenieros".
3. *La misma herramienta acelera… y frena* — +55,8% vs −19% (Peng vs METR) + pos-it "creían +20%".
4. *El último 30% es el que duele* — barra 70/30 + cita de Osmani.
5. *Código que parece correcto y no lo es* — 45% Veracode + Stanford + slopsquatting + pos-it malware.
6. *¿Quién está pagando esto?* — cita gigante de Altman + MIT 95% / FMI puntocom + pos-it "el token crudo SÍ rentable".
7. *El cuello de botella se mudó* — medidor ESCRIBIR ✗ → ✅ VERIFICAR + cita Qi 2015.

**Bloque 4 — Nuevo rol, empleo y conclusión** (verde `#12A36B`):
1. *Sube de piso* — ESCRIBIR CÓDIGO → ESPECIFICAR·DISEÑAR·VALIDAR·DECIDIR (cada uno atado a su barrera matemática).
2. *Tres trabajos que la IA hace nacer* — ARQUITECTO / AUDITOR / RESPONSABLE + cita de Brooks.
3. *La buena noticia (y la trampa de Jevons)* — +170M −92M = +78M (WEF) + BLS +15%/−6% + cajeros.
4. *La puerta de entrada se está cerrando* — −65% / −76% junior + Brynjolfsson + pos-it "¿IA o fin del crédito barato?".
5. *Hasta los profetas conceden* — citas de Amodei y Beck.
6. *Se vacía el medio* — (la Conclusión existente: U/polarización) se mantiene.
7. *La paradoja esperanzadora* — cierre a pantalla completa: "La IA no anuncia el fin del ingeniero: redefine quién lo es. Gracias."

El deck pasó de 22 a **30 slides** (intro actualizada: "Diseñando 30 slides…"). La cita
final va después de la Conclusión y del chiste del micrófono, antes del cierre MS-Paint.

## 7. Chiste de localhost (Marte) — Bloque 2
Slide nueva en Bloque 2 (antes de "¿Quién paga?"): «Le pedí a la IA un sistema para
controlar la agricultura en Marte… me lo dio en 5 minutos. Los SWE están muertos» —
con un navegador mock mostrando `localhost:3000/marte-agro` y el remate "«localhost» =
anda solo en tu compu". Refuerza demo ≠ producción. Deck: 30 → 31 slides.
