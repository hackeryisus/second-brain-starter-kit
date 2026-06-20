---
name: revision-semanal
version: 0.1.0
description: |
  Check-in periódico de todo el segundo cerebro: muestra qué avanzó, qué
  está atorado, y corre los rituales de mantenimiento (procesar Inbox,
  podar MEMORIA, archivar proyectos cerrados). Activa cuando el usuario
  diga "revisión semanal", "cómo voy", "qué está atorado", "revisa mi
  sistema", o quiera un check-in recurrente.
allowed-tools:
  - Read
  - Write
  - Edit
  - Bash
---

# Revisión Semanal

Nota de compatibilidad: el bloque `allowed-tools` del frontmatter es para Claude.
En Codex, lee esta skill como instrucciones operativas y usa las herramientas
equivalentes disponibles para leer, escribir, editar, listar archivos y consultar la
fecha.

El ritual que convierte carpetas en un *sistema*. Dos trabajos: **reportar** (qué
pasó, qué está atorado) y **mantener** (rutar, podar, archivar). Se corre cuando el
usuario lo pida o semanalmente.

## Paso 0 — Cargar contexto (lee en vivo, no copies)

- `PERFIL.md` — metas y dirección, para juzgar qué va bien y qué no.
- Cada `Proyectos/*/INDEX.md` — estado actual de cada proyecto vivo.
- `MEMORIA.md` — el registro suelto.
- `Inbox/` — lista qué hay sin procesar. Saca la fecha con `date +%F`.

## Paso 1 — Reporte

Escribe un briefing corto (en el chat, o en
`Brainstorms/{YYYY-MM-DD}-revision-semanal.md` si el usuario quiere guardarlo):

- **Avanzó** — proyectos que se movieron; nombra el cambio concreto.
- **Atorado** — proyectos sin movimiento o con una pregunta abierta bloqueante. Di por qué.
- **Deriva** — cualquier cosa que se esté alejando de las metas en `PERFIL.md`.
- **Una siguiente acción** — lo de mayor impacto para la semana que viene.

Sé honesto, no animoso. Si algo se frenó, di que se frenó.

## Paso 2 — Mantenimiento (los rituales)

Corre estos en orden, reportando qué cambiaste:

1. **Procesar Inbox.** Lleva cada cosa en `Inbox/` a su hogar real (`PERFIL.md`, un
   `INDEX.md` de proyecto, `MEMORIA.md`, o un proyecto nuevo), luego bórrala de ahí.
   Meta: vacío.
2. **Podar MEMORIA.** Para cada línea en `MEMORIA.md`: promueve datos duraderos a
   `PERFIL.md`, datos de proyecto a su `INDEX.md`, tira los que ya no apliquen. Borra
   las líneas promovidas.
3. **Archivar proyectos cerrados.** Cualquier `INDEX.md` con `estado: terminado` o
   `cancelado` → mueve su carpeta a `Proyectos/_archivo/` (crea `_archivo/` solo si
   no existe).
4. **Actualizar fechas.** Pon la fecha de hoy en `actualizado:` de cualquier
   `INDEX.md` o `PERFIL.md` que hayas tocado.

## Paso 3 — Cierre

Resumen en una línea: qué reportaste, qué limpiaste, y la siguiente acción del
Paso 1. No sobre-expliques.
