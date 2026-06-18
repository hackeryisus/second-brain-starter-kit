# CLAUDE.md — Router del Segundo Cerebro

Instrucciones para el asistente de IA que trabaja en esta carpeta. Esto es un
**segundo cerebro personal**: una base de conocimiento viva hecha de archivos
Markdown. No es un proyecto de software.

Este archivo se carga automáticamente. Todo lo demás se lee cuando se necesita.

---

## Los archivos principales

| Archivo | Qué guarda | Cuándo leerlo |
|---|---|---|
| `CLAUDE.md` (este) | Reglas y ruteo | Siempre (se carga solo) |
| `PERFIL.md` | Quién es el usuario: metas, voz, contexto, limitantes | Antes de personalizar cualquier cosa |
| `MEMORIA.md` | Datos sueltos con fecha que no van en otro lado | Cuando necesites contexto reciente |
| `Inbox/` | Capturas rápidas sin procesar — la puerta de entrada | Al procesar o hacer revisión |
| `Proyectos/<nombre>/INDEX.md` | Info y estado de un proyecto | Cuando la tarea toque ese proyecto |

**Lee en vivo, no copies.** Cuando necesites datos del perfil o de un proyecto, lee
el archivo directo. Nunca copies el contenido de `PERFIL.md` a otro lugar — las
copias se desactualizan.

---

## REGLA PRINCIPAL — Proyecto nuevo → carpeta + INDEX.md

Cuando el usuario diga que **empieza un proyecto, workstation, esfuerzo o
iniciativa nueva** (por ejemplo: "estoy empezando X", "nuevo proyecto: X",
"vamos a armar X"):

1. Crea la carpeta `Proyectos/<nombre-en-kebab-case>/`.
2. Copia `Templates/project-index-template.md` como `INDEX.md`.
3. Llena lo que puedas inferir; deja `POR DEFINIR:` en lo demás.
4. Dile al usuario qué carpeta creaste y hazle 1–2 preguntas para completar el brief.

Haz esto **antes** de empezar el trabajo del proyecto. Un proyecto = una carpeta =
un `INDEX.md`.

---

## Dónde va cada cosa

- **Captura rápida** (nota suelta, link, idea a medio cocinar, "guárdame esto para
  después") → tira un archivo en `Inbox/`. No lo clasifiques al momento; se ordena
  después.
- **Regla o comportamiento fijo** (siempre haz X, nunca hagas Y) → este `CLAUDE.md`
  o el `SKILL.md` de la habilidad correspondiente.
- **Dato sobre el usuario** (durable: metas, voz, limitantes) → `PERFIL.md`.
- **Dato suelto o aprendizaje** que no va en un proyecto ni en el perfil → agrega una
  línea con fecha en `MEMORIA.md`. Formato: `- YYYY-MM-DD — <el dato>`.
- **Dato de un proyecto** (estado, decisión, link) → el `INDEX.md` de ese proyecto.
- En caso de duda, propón dónde va y confirma. Convierte fechas relativas a absolutas
  (`YYYY-MM-DD`) antes de guardar.

## Procesar el Inbox

Cuando el usuario diga "procesa mi inbox" (o durante la revisión semanal): toma cada
cosa en `Inbox/`, llévala a su hogar real (`PERFIL.md`, un `INDEX.md` de proyecto,
`MEMORIA.md`, o un proyecto nuevo), y bórrala del `Inbox/`. Meta: inbox vacío.

## Cerrar un proyecto (regla de archivo)

Cuando el `INDEX.md` de un proyecto llegue a `status: terminado` o `status: cancelado`,
mueve su carpeta a `Proyectos/_archivo/`. **Crea `_archivo/` solo cuando sea
necesario** — la primera vez que se archive algo. Así `Proyectos/` solo muestra lo
que está vivo.

## Mantener MEMORIA.md sana (ritual de limpieza)

`MEMORIA.md` crece si nunca se poda. En cada revisión semanal (o cuando te pidan
"limpia la memoria"): revisa cada línea y decide si **promoverla** (un dato duradero
→ `PERFIL.md`; un dato de proyecto → su `INDEX.md`) y borrar la línea, o **tirarla**
si ya no aplica. Lo que queda son datos genuinamente sueltos y vigentes.

---

## Habilidades del asistente

| Cuando el usuario… | Activa |
|---|---|
| dice "grill me", "entrevístame", quiere hacer brainstorm o sacar lo que tiene en la cabeza | `skills/grill-me` |
| **primera vez**, cuando `PERFIL.md` aún tiene marcadores sin llenar | `skills/grill-me`, luego escribe las respuestas en `PERFIL.md` |
| pide escribir "en mi voz", "como yo lo escribiría", un post/email/hilo/newsletter a su nombre | `skills/mi-voz` (lee `PERFIL.md`) |
| dice "revisión semanal", "cómo voy", "qué está atorado", o quiere un check-in periódico | `skills/revision-semanal` |

---

## Arranque inicial (primera vez)

Si `PERFIL.md` todavía tiene marcadores sin llenar (`POR DEFINIR:` / `{{...}}`):
1. Corre `grill-me` para entrevistar al usuario sobre identidad, metas, voz y limitantes.
2. Escribe las respuestas capturadas en `PERFIL.md`, reemplazando los marcadores.
3. A partir de ahí, `mi-voz` y cada proyecto leen de `PERFIL.md`.

---

## Mapa de la carpeta

```
CLAUDE.md      ← este router (se carga solo)
README.md      ← guía de arranque para humanos
PERFIL.md      ← todo sobre el usuario
MEMORIA.md     ← registro de datos sueltos con fecha
Inbox/         ← capturas rápidas sin procesar (puerta de entrada)
Proyectos/     ← una carpeta por proyecto, cada una con INDEX.md
               ← _archivo/ aparece aquí cuando se cierra un proyecto
Templates/     ← plantilla de INDEX.md para proyectos nuevos
skills/        ← grill-me, mi-voz, revision-semanal
```
