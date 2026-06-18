# Segundo Cerebro — Kit de Inicio

Una carpeta simple para organizar tu vida, tus proyectos y tus ideas con ayuda de
tu asistente de IA. Solo necesitas abrir esta carpeta en Cowork y empezar a hablar.

## Qué hay adentro

| Archivo / carpeta | Para qué sirve |
|---|---|
| `CLAUDE.md` | Las instrucciones que tu asistente lee automáticamente. No necesitas tocarlo. |
| `PERFIL.md` | Todo sobre ti: quién eres, qué quieres lograr, cómo escribes. Tu asistente lo usa para ayudarte mejor. |
| `MEMORIA.md` | Un registro de cosas sueltas que vas aprendiendo o descubriendo. |
| `Inbox/` | Tu buzón de entrada: tira aquí lo que se te ocurra y después lo ordenas. |
| `Proyectos/` | Una carpeta por cada proyecto. Cada uno tiene su propio archivo con toda la info. |
| `skills/` | Habilidades especiales de tu asistente (entrevistarte, escribir en tu voz, revisión semanal). |

---

## Cómo empezar — dile esto a tu asistente

> "Inicializa mi segundo cerebro."

Tu asistente va a:

1. **Leerte las instrucciones** (el archivo `CLAUDE.md`, automático).
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
