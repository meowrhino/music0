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

## Las pruebas (lluvia de ideas, lote 1)

Puntuaciones de la investigación — **VI** = interés visual, **CD** = profundidad conceptual (1–10).

| # | Prueba | Qué hace | Cat. | VI/CD |
|---|--------|----------|------|-------|
| 01 | [Lissajous](pruebas/01-lissajous.html) | Intervalos como curvas. Justo = curva fija; temperado = gira (∝ batido). | 2 | 9/8 |
| 02 | [Círculo cromático](pruebas/02-circulo-cromatico.html) | Acordes como polígonos; presets, raíz y orden cromático↔quintas. | 1 | 8/6 |
| 03 | [Tonnetz](pruebas/03-tonnetz.html) | Retícula de tríadas; ▲ mayor / ▼ menor; hover + clic para sonar. | 4 | 9/9 |
| 04 | [Serie armónica](pruebas/04-serie-armonica.html) | Cuerda vibrante, 16 sobretonos, cents y timbre aditivo. | 2 | 8/9 |
| 05 | [Cymatics / Chladni](pruebas/05-cymatics-chladni.html) | 12 000 granos posándose en las líneas nodales del modo (n, m). | 3 | 9/8 |
| 06 | [Curva de disonancia](pruebas/06-curva-disonancia.html) | Modelo Plomp–Levelt/Sethares; valles = consonancia. Arrastra y oye. | 6 | 8/10 |

## Rumbos posibles (la "web loquita")

- **A · Galería + navegador** ✦ *(aquí estamos)* — mini-experimentos autónomos + este `index.html`.
- **B · Showpiece profundo** — pulir UNA pieza a fondo (Tonnetz toroidal 3D con Three.js + Web MIDI,
  lattice de entonación justa con audio, u orbifold de Tymoczko).
- **C · Ensayo explorable** — scrollytelling que explica la armonía con widgets incrustados (modelo osar.fr).
- **D · Playground audiovisual en vivo** — un instrumento: tocas notas/MIDI y varias visualizaciones
  reaccionan a la vez (Tonnetz + chroma + cymatics).
- **E · Hub mixto** — A como base + 1–2 piezas de B + intro narrativa de C. Destino a medio plazo.

## Ideas para el siguiente lote

- Mapeo color↔nota (Scriabin / sinestesia) como capa compartida entre piezas (cat. 7).
- Visualizador espectral / mandala reactivo al micrófono (FFT, cat. 5).
- Hélice de croma / tonos de Shepard en Three.js (cat. 1/2).
- Lattice de entonación justa al estilo Hayward Tuning Vine (cat. 2).
- Entrada Web MIDI para tocar el Tonnetz y el círculo cromático con un teclado real.

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
    └── 06-curva-disonancia.html
```

## Stack

Vanilla JS · Canvas 2D · Web Audio API (`OscillatorNode`, `PeriodicWave`, `GainNode`). Sin frameworks
ni CDNs para que sea portable y fácil de hackear.
