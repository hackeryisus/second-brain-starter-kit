# Segundo Cerebro — Kit de Inicio

Una carpeta simple para organizar tu vida, tus proyectos y tus ideas con ayuda de
tu asistente de IA. Funciona con Claude y con Codex: abre esta carpeta en tu
herramienta preferida y empieza a hablar.

---

## Ábrelo en Obsidian (recomendado)

Este kit es una carpeta de archivos Markdown. Lo puedes leer con cualquier editor,
pero está pensado para [Obsidian](https://obsidian.md) — una app gratuita para tomar
notas. Ya trae configuración lista (`.obsidian/`): plugins útiles, notas diarias en
`Diario/`, y las notas nuevas caen directo al `Inbox/`.

Para empezar:

1. **Descarga Obsidian** desde [obsidian.md/download](https://obsidian.md/download) e
   instala la app (gratis, Windows / Mac / Linux).
2. **Descarga este kit** desde GitHub: botón verde **`Code`** ▸ **`Download ZIP`**.
   Descomprime el ZIP donde quieras guardarlo.
3. **Abre Obsidian** y elige **"Open folder as vault"** (Abrir carpeta como bóveda).
4. **Selecciona la carpeta** que descomprimiste (`second-brain-starter-kit`).
5. Cuando Obsidian pregunte si confías en los plugins de la comunidad, acepta para
   activar los que ya vienen configurados (búsqueda, archivos recientes, barra de
   edición).

Listo: la bóveda abre con todo ordenado. Ahora conecta tu asistente de IA (Claude o
Codex) apuntando a la misma carpeta y empieza a hablar.

## Qué hay adentro

| Archivo / carpeta | Para qué sirve |
|---|---|
| `CLAUDE.md` | Router automático para Claude. Mantener sincronizado con `AGENTS.md`. |
| `AGENTS.md` | Router automático para Codex. Mantener sincronizado con `CLAUDE.md`. |
| `PERFIL.md` | Todo sobre ti: quién eres, qué quieres lograr, cómo escribes. Tu asistente lo usa para ayudarte mejor. |
| `MEMORIA.md` | Un registro de cosas sueltas que vas aprendiendo o descubriendo. |
| `Inbox/` | Tu buzón de entrada: tira aquí lo que se te ocurra y después lo ordenas. |
| `Proyectos/` | Una carpeta por cada proyecto. Cada uno tiene su propio archivo con toda la info. |
| `skills/` | Habilidades especiales de tu asistente (entrevistarte, escribir en tu voz, revisión semanal). |
| `.obsidian/` | Configuración lista de Obsidian: plugins, notas diarias y ajustes. No necesitas tocarla. |

---

## Cómo empezar — dile esto a tu asistente

> "Inicializa mi segundo cerebro."

Tu asistente va a:

1. **Leerte las instrucciones** (`CLAUDE.md` en Claude, `AGENTS.md` en Codex).
2. **Hacerte una entrevista** para conocerte — tus metas, tu forma de escribir, tus
   limitantes — y guardar todo en `PERFIL.md`. Esto solo pasa la primera vez.
3. Confirmar que todo está listo.

Después de eso, el sistema está vivo. Usa estas frases:

- **"Estoy empezando un proyecto nuevo: X"** → Crea una carpeta en `Proyectos/` con
  toda la estructura.
- **"Escribe esto en mi voz"** → Redacta como tú, usando lo que sabe de tu perfil.
- **"Acuérdate de que…"** → Guarda un dato suelto en `MEMORIA.md`.
- **"Guárdame esto para después"** (un link, una nota, lo que sea) → Lo tira al `Inbox/`.
- **"Revisión semanal"** → Te dice qué avanzó, qué está atorado, y limpia el sistema.

---

## Cómo funciona por dentro

```
entrevista (grill-me)  ──llena──▶  PERFIL.md  ──lo lee──▶  mi-voz + cada proyecto
                                       │
                                       └── cosas sueltas ──▶ MEMORIA.md
                                       └── capturas rápidas ──▶ Inbox/

revisión semanal  ──▶  vacía Inbox, poda MEMORIA, archiva proyectos terminados
```

No necesitas entender la estructura para usarlo — solo habla con tu asistente y él
sabe qué hacer con cada cosa.
