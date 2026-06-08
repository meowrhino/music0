# music0 · visualizaciones de la armonía musical

[![en vivo](https://img.shields.io/badge/en%20vivo-meowrhino.github.io%2Fmusic0-3ee8d0?style=flat-square)](https://meowrhino.github.io/music0/)
![piezas](https://img.shields.io/badge/piezas-31-9b6bff?style=flat-square)
![dependencias](https://img.shields.io/badge/dependencias-0-ff4d9d?style=flat-square)
![stack](https://img.shields.io/badge/Canvas%20%2B%20Web%20Audio-vanilla-e9ff5a?style=flat-square)

### 🌐 **[Pruébalo en vivo → meowrhino.github.io/music0](https://meowrhino.github.io/music0/)**

[![music0](og.png)](https://meowrhino.github.io/music0/)

**31 juguetes interactivos** para **ver y oír** la teoría musical, a partir de la
[investigación](investigacion.md) de partida. Todo es **HTML + Canvas + Web Audio API** puro:
sin build, sin dependencias, sin red. Cada pieza es un `.html` autónomo que funciona abriéndolo
directamente. Hay además un **[ensayo explorable](ensayo.html)** y una página **[sobre](sobre.html)**.

👉 Empieza por **[`index.html`](index.html)** (la galería) o por el **[ensayo](ensayo.html)**.

## Cómo abrir

```bash
# opción A: doble clic en index.html (file://) — funciona

# opción B (recomendada): servidor estático local
cd music0
python3 -m http.server 8000
# luego abre http://localhost:8000
```

> El audio arranca al primer clic/gesto (política de autoplay de los navegadores).

## Las pruebas (31 piezas, agrupadas por categoría)

Puntuaciones de la investigación — **VI** = interés visual, **CD** = profundidad conceptual (1–10).
En la portada (`index.html`) están ordenadas de lo geométrico a lo perceptual.

**★ Instrumento en vivo**

| # | Prueba | Qué hace | Cat. | VI/CD |
|---|--------|----------|------|-------|
| 13 | [Instrumento en vivo](pruebas/13-instrumento.html) | Tocas (piano / teclado / Web MIDI) y el círculo, el Tonnetz y las ondas reaccionan a la vez. | D | 9/7 |

**I · Geometría de acordes y tríadas**

| # | Prueba | Qué hace | Cat. | VI/CD |
|---|--------|----------|------|-------|
| 02 | [Círculo cromático](pruebas/02-circulo-cromatico.html) | Acordes como polígonos; presets, raíz y orden cromático↔quintas. | 1 | 8/6 |
| 03 | [Tonnetz](pruebas/03-tonnetz.html) | Retícula de tríadas; ▲ mayor / ▼ menor; hover + clic para sonar. | 4 | 9/9 |
| 11 | [Tonnetz+](pruebas/11-tonnetz-midi.html) | Transformaciones PLR + Web MIDI + estela de conducción de voces (atajos P/L/R). | 4 | 9/9 |
| 12 | [Tonnetz toroidal](pruebas/12-tonnetz-toro.html) | La retícula envuelta en un toro 3D navegable (Z₁₂ ≅ Z₃×Z₄). Gira + PLR. | 4 | 9/10 |
| 14 | [Orbifold de Tymoczko](pruebas/14-orbifold-tymoczko.html) | Una díada = un punto en una banda de Möbius; borde=unísonos, centro=tritonos. Cruza voces. | 4 | 8/10 |
| 15 | [Orbifold de tríadas](pruebas/15-orbifold-triadas.html) | El triángulo de tipos de tríada (sección del prisma): aumentada al centro, unísonos en los vértices. | 4 | 8/10 |
| 21 | [Collares de escalas](pruebas/21-collares-escalas.html) | Escalas como collares de 12 cuentas (Ian Ring); modos = rotaciones, patrón de intervalos + ID binario. | 1 | 7/9 |
| 22 | [Orbifold de tétradas](pruebas/22-orbifold-tetradas.html) | El espacio de acordes de 4 notas: tetraedro 3D, séptima disminuida en el centro. | 4 | 8/10 |
| 27 | [Secuenciador del Tonnetz](pruebas/27-secuenciador-tonnetz.html) | Teje una progresión sobre el Tonnetz y míralo recorrer la retícula en bucle. | 4 | 9/8 |
| 28 | [Música infinita](pruebas/28-musica-infinita.html) | Armonía generativa sin fin (paseo PLR aleatorio, modo Eno). Déjalo sonar. | 4 | 8/6 |
| 29 | [Teclado isomórfico](pruebas/29-teclado-isomorfico.html) | Wicki–Hayden en hexágonos: la misma forma de acorde sirve en cualquier tono. | 1 | 8/8 |

**II · Frecuencia, ratios y afinación**

| # | Prueba | Qué hace | Cat. | VI/CD |
|---|--------|----------|------|-------|
| 01 | [Lissajous](pruebas/01-lissajous.html) | Intervalos como curvas. Justo = curva fija; temperado = gira (∝ batido). | 2 | 9/8 |
| 04 | [Serie armónica](pruebas/04-serie-armonica.html) | Cuerda vibrante, 16 sobretonos, cents y timbre aditivo. | 2 | 8/9 |
| 10 | [Lattice de entonación justa](pruebas/10-lattice-ji.html) | Retícula 5-límite (quintas × terceras justas); ratios, cents; justa vs temperada. | 2 | 8/9 |
| 09 | [Hélice de Shepard](pruebas/09-helice-shepard.html) | Tono que sube/baja para siempre (Shepard–Risset), en espiral. | 2 | 7/9 |
| 16 | [Cuerdas pitagóricas](pruebas/16-cuerdas-baroque.html) | Cuerdas con longitud ∝ 1/frecuencia; se pulsan en secuencia y vibran. À la Baroque.me. | 8 | 9/8 |
| 23 | [Hélice de croma](pruebas/23-helice-croma.html) | La hélice de la altura de Shepard; doble hélice de las dos escalas de tonos enteros. | 1 | 9/8 |
| 24 | [Armonógrafo](pruebas/24-armonografo.html) | Péndulos amortiguados que dibujan el cociente: figuras que decaen en espiral. | 2 | 9/7 |
| 25 | [Nudo armónico 3D](pruebas/25-nudo-armonico.html) | Un Lissajous en el espacio: 3 senos en cociente entero tejen un nudo. 4:5:6 = mayor. | 2 | 9/7 |
| 30 | [Espiral de overtonos](pruebas/30-espiral-overtonos.html) | La espiral de la altura: una vuelta = una octava; las octavas se alinean en el mismo radio. | 2 | 9/8 |
| 31 | [La coma que deriva](pruebas/31-coma-pump.html) | El comma pump: en entonación justa el tónico deriva una coma sintónica por vuelta. | 2 | 8/10 |

**III · Física y espectro**

| # | Prueba | Qué hace | Cat. | VI/CD |
|---|--------|----------|------|-------|
| 05 | [Cymatics / Chladni](pruebas/05-cymatics-chladni.html) | 12 000 granos posándose en las líneas nodales del modo (n, m). | 3 | 9/8 |
| 08 | [Mandala FFT](pruebas/08-mandala-fft.html) | El espectro dibuja un mandala radial que late; con micrófono opcional. | 5 | 9/5 |
| 18 | [Cromagrama](pruebas/18-cromagrama.html) | El espectro plegado en 12 clases de altura; círculo de croma + cromagrama desplazante. Con micro. | 5 | 8/8 |
| 19 | [Espectrograma](pruebas/19-espectrograma.html) | El espectro en cascada: tiempo en X, frecuencia (log) en Y, brillo = energía. Con micro. | 5 | 8/6 |
| 26 | [Chladni 3D](pruebas/26-chladni-3d.html) | La placa de Chladni como relieve 3D; líneas nodales en cian sobre el modo (n, m). | 3 | 9/7 |

**IV · Psicoacústica y color**

| # | Prueba | Qué hace | Cat. | VI/CD |
|---|--------|----------|------|-------|
| 06 | [Curva de disonancia](pruebas/06-curva-disonancia.html) | Modelo Plomp–Levelt/Sethares; valles = consonancia. Arrastra y oye. | 6 | 8/10 |
| 07 | [Color ↔ nota](pruebas/07-color-scriabin.html) | Círculo de quintas con los colores de Scriabin / el arcoíris sinestésico. | 7 | 8/7 |
| 17 | [Heatmap de disonancia](pruebas/17-heatmap-disonancia.html) | Mapa 2D de disonancia sensorial de tríadas (Sethares); los valles = consonancia. | 6 | 8/9 |
| 20 | [Batido de dos tonos](pruebas/20-batido.html) | Dos tonos cercanos y su envolvente pulsando: del unísono a la aspereza (banda crítica). | 6 | 8/8 |

## Capa de color compartida

Varias piezas (02, 03, 07, 10, 11, 12, 13, 21, 23) comparten un **selector de paleta**
(croma / **Scriabin** / 5tas) que se guarda en `localStorage`: cambiarlo en una pieza **tiñe todas las
demás** — una capa de color común sin romper la autonomía de cada `.html`. El mapa de Scriabin sale de
la pieza 07; el 07 mismo lo sincroniza con su toggle Scriabin/sinestesia.

## Los cinco rumbos (todos recorridos ✦)

- **A · Galería + navegador** — el `index.html` con las 31 piezas en 5 categorías.
- **B · Showpiece profundo** — Tonnetz 3D toroidal y orbifolds de díadas (14), tríadas (15) y tétradas (22).
- **C · Ensayo explorable** — [`ensayo.html`](ensayo.html): scrollytelling de 10 paradas con widgets.
- **D · Playground en vivo** — el **Instrumento (13)**: tocas y el círculo + Tonnetz + ondas reaccionan.
- **E · Hub mixto** — la portada funde hero en vivo + "Explora" (piezas en vivo) + galería + créditos en
  un scroll, con [`sobre.html`](sobre.html) y nav compartida. Desplegado en GitHub Pages.

## Ideas para "v2" (opcional)

- Fundir aún más el modo E con grabar/compartir lo que tocas; **Web MIDI** en más piezas.
- Más piezas: orbifold de **péntadas**, **secuenciador/looper** sobre el Tonnetz, Chladni con marching cubes.
- **Dominio propio** (CNAME).

## Estructura

```
music0/
├── index.html              ← navegador / galería (el hub)
├── ensayo.html             ← ensayo explorable (scrollytelling)
├── sobre.html              ← sobre el proyecto + créditos
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
    ├── 11-tonnetz-midi.html
    ├── 12-tonnetz-toro.html
    ├── 13-instrumento.html
    ├── 14-orbifold-tymoczko.html
    ├── 15-orbifold-triadas.html
    ├── 16-cuerdas-baroque.html
    ├── 17-heatmap-disonancia.html
    ├── 18-cromagrama.html
    ├── 19-espectrograma.html
    ├── 20-batido.html
    ├── 21-collares-escalas.html
    ├── 22-orbifold-tetradas.html
    ├── 23-helice-croma.html
    ├── 24-armonografo.html
    ├── 25-nudo-armonico.html
    ├── 26-chladni-3d.html
    ├── 27-secuenciador-tonnetz.html
    ├── 28-musica-infinita.html
    ├── 29-teclado-isomorfico.html
    ├── 30-espiral-overtonos.html
    └── 31-coma-pump.html
```

## Stack

Vanilla JS · Canvas 2D · Web Audio API (`OscillatorNode`, `PeriodicWave`, `AnalyserNode`, `GainNode`)
· Web MIDI · getUserMedia. Sin frameworks ni CDNs para que sea portable y fácil de hackear.
