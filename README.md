# music0 · visualizaciones de la armonía musical

Galería de mini-experimentos para **ver y oír** teoría musical, a partir de la
[investigación](investigacion.md) de partida. Todo es **HTML + Canvas + Web Audio API** puro:
sin build, sin dependencias, sin red. Cada prueba es un `.html` autónomo que funciona abriéndolo
directamente.

👉 **Abre [`index.html`](index.html)** — es el navegador/galería que enlaza a todas las pruebas.

## Cómo abrir

```bash
# opción A: doble clic en index.html (file://) — funciona

# opción B (recomendada): servidor estático local
cd music0
python3 -m http.server 8000
# luego abre http://localhost:8000
```

> El audio arranca al primer clic/gesto (política de autoplay de los navegadores).

## Las pruebas (11 piezas, agrupadas por categoría)

Puntuaciones de la investigación — **VI** = interés visual, **CD** = profundidad conceptual (1–10).
En la portada (`index.html`) están ordenadas de lo geométrico a lo perceptual.

**I · Geometría de acordes y tríadas**

| # | Prueba | Qué hace | Cat. | VI/CD |
|---|--------|----------|------|-------|
| 02 | [Círculo cromático](pruebas/02-circulo-cromatico.html) | Acordes como polígonos; presets, raíz y orden cromático↔quintas. | 1 | 8/6 |
| 03 | [Tonnetz](pruebas/03-tonnetz.html) | Retícula de tríadas; ▲ mayor / ▼ menor; hover + clic para sonar. | 4 | 9/9 |
| 11 | [Tonnetz+](pruebas/11-tonnetz-midi.html) | Transformaciones PLR + Web MIDI + estela de conducción de voces (atajos P/L/R). | 4 | 9/9 |

**II · Frecuencia, ratios y afinación**

| # | Prueba | Qué hace | Cat. | VI/CD |
|---|--------|----------|------|-------|
| 01 | [Lissajous](pruebas/01-lissajous.html) | Intervalos como curvas. Justo = curva fija; temperado = gira (∝ batido). | 2 | 9/8 |
| 04 | [Serie armónica](pruebas/04-serie-armonica.html) | Cuerda vibrante, 16 sobretonos, cents y timbre aditivo. | 2 | 8/9 |
| 10 | [Lattice de entonación justa](pruebas/10-lattice-ji.html) | Retícula 5-límite (quintas × terceras justas); ratios, cents; justa vs temperada. | 2 | 8/9 |
| 09 | [Hélice de Shepard](pruebas/09-helice-shepard.html) | Tono que sube/baja para siempre (Shepard–Risset), en espiral. | 2 | 7/9 |

**III · Física y espectro**

| # | Prueba | Qué hace | Cat. | VI/CD |
|---|--------|----------|------|-------|
| 05 | [Cymatics / Chladni](pruebas/05-cymatics-chladni.html) | 12 000 granos posándose en las líneas nodales del modo (n, m). | 3 | 9/8 |
| 08 | [Mandala FFT](pruebas/08-mandala-fft.html) | El espectro dibuja un mandala radial que late; con micrófono opcional. | 5 | 9/5 |

**IV · Psicoacústica y color**

| # | Prueba | Qué hace | Cat. | VI/CD |
|---|--------|----------|------|-------|
| 06 | [Curva de disonancia](pruebas/06-curva-disonancia.html) | Modelo Plomp–Levelt/Sethares; valles = consonancia. Arrastra y oye. | 6 | 8/10 |
| 07 | [Color ↔ nota](pruebas/07-color-scriabin.html) | Círculo de quintas con los colores de Scriabin / el arcoíris sinestésico. | 7 | 8/7 |

## Rumbos posibles (la "web loquita")

- **A · Galería + navegador** ✦ *(aquí vivimos)* — mini-experimentos autónomos + este `index.html`.
- **B · Showpiece profundo** ◐ *(empezado)* — el **Tonnetz+** (PLR + Web MIDI) es la primera pieza
  profunda; siguiente paso: Tonnetz toroidal 3D u orbifold de Tymoczko.
- **C · Ensayo explorable** ◐ *(empezado)* — la portada agrupada por categoría es el primer paso hacia
  un scrollytelling con widgets incrustados (modelo osar.fr).
- **D · Playground audiovisual en vivo** — un instrumento: tocas notas/MIDI y varias visualizaciones
  reaccionan a la vez (Tonnetz + chroma + cymatics).
- **E · Hub mixto** — A como base + 1–2 piezas de B + intro narrativa de C. Destino a medio plazo.

## Ideas para el siguiente lote

- Tonnetz **toroidal 3D** (el showpiece): envolver la retícula en un toro navegable.
- **Color como capa compartida**: teñir el círculo cromático y el Tonnetz con el mapa de Scriabin.
- **Orbifold de Tymoczko**: cinta de Möbius del espacio de díadas (geometría de la conducción de voces).
- **Modo D**: un teclado en pantalla / Web MIDI que dispara a la vez Tonnetz + chroma + cymatics.
- Pulir **responsive**: en móvil vertical el panel inferior tapa parte de la figura en algunas piezas.

## Estructura

```
music0/
├── index.html              ← navegador / galería
├── investigacion.md         ← investigación de partida
├── README.md
└── pruebas/
    ├── 01-lissajous.html
    ├── 02-circulo-cromatico.html
    ├── 03-tonnetz.html
    ├── 04-serie-armonica.html
    ├── 05-cymatics-chladni.html
    ├── 06-curva-disonancia.html
    ├── 07-color-scriabin.html
    ├── 08-mandala-fft.html
    ├── 09-helice-shepard.html
    ├── 10-lattice-ji.html
    └── 11-tonnetz-midi.html
```

## Stack

Vanilla JS · Canvas 2D · Web Audio API (`OscillatorNode`, `PeriodicWave`, `AnalyserNode`, `GainNode`)
· Web MIDI · getUserMedia. Sin frameworks ni CDNs para que sea portable y fácil de hackear.
