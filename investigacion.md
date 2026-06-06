# A Catalog of Visual Representations of Musical Harmony — A Builder's Reference

> Investigación de partida para el proyecto **music0**. Documento original conservado tal cual.
> Resumen en español, lluvia de ideas y prototipos: ver [README.md](README.md) y la carpeta [`pruebas/`](pruebas/).

**Scope note:** I could not access the source tweet (https://x.com/male_leo_xxvi/status/2062970826958524596) because X blocks automated access, so this casts a wide net across all eight requested categories. Scores are my own editorial judgment on a 1–10 scale: **VI** = Visual Interest/aesthetic appeal, **CD** = Conceptual Depth/theoretical richness.

## TL;DR

- The richest, most replicable veins for a JAMstack developer are **(1) interactive Tonnetz/neo-Riemannian lattices** (many live JS implementations already exist to fork) and **(2) frequency-ratio visualizations** (Lissajous curves, harmonic-series spirals, just-intonation lattices) — both are mathematically clean and map directly to Canvas/SVG + Web Audio/Tone.js.
- The single deepest theoretical well is **Dmitri Tymoczko's orbifold/voice-leading geometry** (his "The Geometry of Musical Chords," *Science*, 7 July 2006, Vol. 313, No. 5783, pp. 72–74 — the first music-theory article in *Science*'s then-127-year history), and the most aesthetically striking physical phenomena are **Chladni plates and Faraday-wave cymatics**, both of which have existing Shadertoy/Three.js implementations to study.
- Twitter/X and Reddit could not be reliably mined by automated search (both block scraping), so I flag those as gaps with recommended on-platform search strategies; the strongest social-adjacent creative-coder is **Alexander Chen** (Baroque.me, Harmonics, MTA.me).

## Key Findings

- **Tonnetz is the best starting point.** It is conceptually deep (neo-Riemannian theory, the torus topology) yet visually simple (a triangular lattice), and there are at least six live browser implementations to study or fork.
- **Frequency-ratio visuals are the most "beautiful per line of code."** Lissajous figures and harmonic-series spirals are tiny to implement and reward interactivity.
- **Cymatics/Chladni patterns are the highest aesthetic payoff** but require either physics simulation (eigenmodes of a vibrating plate) or shader artistry — existing Shadertoy shaders solve this.
- **Color-music mappings are the easiest to bolt onto any of the above** and connect to a long history (Scriabin, synesthesia research).
- **The two genuine sourcing gaps are Reddit and Twitter/X**, which require manual, logged-in searching.

## Details

### Category 1 — Geometric / mandala representations of chords, intervals, and scales

**Interactive Chromatic Circle (Subhrajit Bhattacharya)** — https://chromatic-circle.subhrajit.net/
Scales, modes and chords drawn as polygons inscribed on the 12-note chromatic circle; hover a chord to see its polygon, with preset progressions and chord-type identification driven by JSON. Open-source (GPLv3). **VI 7 / CD 7.** Interactive, browser-based (JS). Easy to fork; recreate with SVG `<polygon>` + Web Audio.

**muted.io — Chromatic Scale / Circle of Fifths** — https://muted.io/chromatic-scale/ , https://muted.io/circle-of-fifths/
Clean interactive circles where triads form characteristic triangles (major/minor/diminished/augmented each a distinct shape); audio playback and sharp/flat toggles. **VI 8 / CD 6.** Canvas/SVG + Tone.js would replicate this.

**fachords — Circle of Fifths Chord Shapes** — https://www.fachords.com/circle-of-fifths-chord-shape/
Demonstrates that connecting a chord's notes on the circle of fifths yields a polygon whose shape is invariant per chord quality (augmented = equilateral triangle, etc.), with an animation cycling through major chords. **VI 7 / CD 7.** Trivial SVG animation.

**Ian Ring — "A study of musical scales"** — https://ianring.com/musictheory/scales/
The canonical "bracelet/necklace" notation: scales as 12-bead bracelets (filled = note present), with modes shown as rotations and symmetry classes explained (prime forms, modes of limited transposition). Each scale also has a unique integer ID (a 12-bit number). **VI 6 / CD 10.** A reference, not an audio toy, but the definitive necklace model — a perfect data model for a generative scale visualizer.

**TerryTrilla — Scale Circle** — https://terrytrilla.com/
Each scale/chord rendered as its own circular geometry so its structure is recognized at a glance; covers diatonic through exotic scales. **VI 7 / CD 7.** Interactive, browser-based.

**ROEL'S WORLD — Music & Geometry / Harmony** — https://roelsworld.eu/blog-music/music-geometry-harmony/
A deep blog mining chord polygons on both the chromatic circle and circle of fifths, superimposing all 12 transpositions to produce mandala-like composite figures, and star polygons (septagrams) for chord progressions. **VI 8 / CD 7.** Static images; ripe for re-implementation as an interactive SVG overlay tool.

**Chroma helix / Shepard pitch helix.** The helical model of pitch (chroma around the circle, height up the axis) due to Roger Shepard; the double-helix variant maps two whole-tone scales. Reference diagrams at audiolabs-erlangen.de (FMP notebooks) and the Shepard–Risset glissando. **VI 7 / CD 9.** A Three.js helix + Web Audio Shepard-tone generator is a compelling, self-contained build. The "equal-temperament spiral" (Donkin 1870; planar equiangular spiral r = (1200/2π)θ) is a 2-D alternative.

### Category 2 — Frequency-ratio and just-intonation visualizations

**Lissajous figures for intervals.** Two perpendicular harmonic motions whose frequency ratio is the interval; simple ratios (octave 2:1, fifth 3:2) yield simple closed curves, dissonant intervals (tritone) yield dense ones; irrational/tempered ratios appear to rotate. Refs: Peter Frazer's tuning appendix (peterfrazer.co.uk), elysiatools.com interactive Lissajous tool, Naveen Venkatesan's Medium piece. A Springer paper (*Recurrence in Lissajous Curves*, link.springer.com) formalizes that the tritone has the most recurrent points. **VI 9 / CD 8.** Canvas parametric plot + Web Audio; one of the highest beauty-to-effort ratios available.

**Hayward Tuning Vine** — https://www.tuningvine.com/
Color-coded prime-number lattice for just intonation, invented by Robin Hayward (b. Brighton, 1969) in 2012, following his fully microtonal tuba of 2009; formally presented in R. Hayward, "The Hayward Tuning Vine: an Interface for Just Intonation," Proc. NIME 2015, Baton Rouge, pp. 209–214 (DOI 10.5281/zenodo.1179084). Higher pitch = higher on screen, enabling intuitive harmonic AND melodic navigation. The site states a shift function along each prime axis allows "unlimited exploration of all ratios up to prime number 31" (the 2015 NIME paper states prime limit 23). **VI 8 / CD 9.** A 5-limit subset is very buildable as an SVG/Canvas lattice with Tone.js.

**mcmire/musical-lattice** — https://github.com/mcmire/musical-lattice
Open-source interactive 5-limit just-intonation lattice. **VI 6 / CD 8.** Direct fork candidate (JS).

**Just Intonation Tuning Lattice (llllllll.co / monome community)** — https://llllllll.co/t/just-intonation-tuning-lattice/74247
Interactive lattice with synth, MIDI, MPE tuning, sequencer. **VI 7 / CD 9.**

**osar.fr — "What I Learned Writing an Album in Just Intonation"** — https://www.osar.fr/notes/justintonation/
Outstanding interactive essay: a JI lattice where clicking a tone highlights its most similar tones (commas), and an animated comparison of the JI lattice vs. its 12-TET tiling, illustrated with the *Lord of the Rings* "Aníron" progression. **VI 9 / CD 10.** A model of what an explorable harmony explainer should be; built with web tech.

**Tonalsoft / Joe Monzo — Harmonic Lattice Diagrams** — http://tonalsoft.com/monzo/lattices/lattices.aspx ; **Loophole Letters — Harmonic Lattices** — https://loophole-letters.vercel.app/harmonic-lattices
Deep references on prime-factor lattice construction (Euler's Tonnetz heritage); the Loophole post builds lattices for any number of dimensions. **VI 6 / CD 9.**

**Harmonic-series interactive tools.** muted.io overtone series (https://muted.io/overtone-series/) with vibrating-string simulation and per-overtone volume; Harmonicarium (https://harmonicarium.org/, GitHub IndustrieCreative/Harmonicarium) a full PWA for playing the harmonic/subharmonic series; Overtones Spiral (https://www.suonoterapia.org/overtones/) a spiral with mic input that highlights overtones you sing and lets you click intervals to hear consonance; teropa.info additive-synthesis tutorial with live Web Audio code. **VI 8 / CD 9.** All directly replicable with the Web Audio API.

**Harmonic Wave Studio** — https://www.harmonicwave.app/
Interactive Fourier-series epicycle animations building complex waveforms, with FFT analysis and filters. **VI 8 / CD 8.** Canvas + Web Audio.

### Category 3 — Cymatics and physical resonance

**Chladni plate Shadertoy shaders** — https://www.shadertoy.com/view/3sjfzz , https://www.shadertoy.com/view/WlfyWn , https://www.shadertoy.com/view/4dXSD2 (knot-line version), https://www.shadertoy.com/view/flVyzV (audio-reactive)
Standing-wave nodal patterns on a vibrating plate; the classic 2-D Chladni figure is the zero set of a sum of sinusoidal eigenmodes. **VI 9 / CD 8.** Directly portable to WebGL/GLSL fragment shaders; the audio-reactive one ties FFT to the a/b/m mode parameters.

**3D Chladni Patterns (CDInstitute / SGI 2024)** — https://github.com/CDInstitute/3DChladni , https://summergeometry.org/sgi2024/3d-chladni-patterns/
Extends Chladni figures to 3-D via marching cubes (Skrodzki/Reitebuch/Polthier, Bridges 2016); open-source Shadertoy + Three.js versions. **VI 9 / CD 9.** Three.js + marching cubes build.

**Microphone Audio Chladni Patterns (Observable)** — https://observablehq.com/@jonhelfman/microphone-audio-chladni-patterns
WebGL Chladni driven live by FFT peaks (a/b/m from peaks, n from volume). **VI 8 / CD 7.** Direct Observable fork.

**Faraday-wave / water cymatics (Linden Gledhill, Alexander Lauterwasser).** Standing-wave patterns on a vibrating fluid surface lit with LEDs/strobe; refs FYFD (fyfluiddynamics.com), Wikipedia Cymatics (Lauterwasser, Hans Jenny, Nigel Stanford's "Cymatics" music video). **VI 10 / CD 6.** Physical, not browser-native, but the look is approximated with radial standing-wave shaders.

### Category 4 — Neo-Riemannian and mathematical music theory (Tonnetz, orbifolds)

**Z-Tonnetz** — https://ztonnetz.com/
Interactive 3-D harmonic-space visualizer with 2D/3D/torus modes, leading-tone/chord detection, and built-in Bach demo files. **VI 9 / CD 9.** Polished reference for a Three.js torus Tonnetz.

**TonnetzViz** — https://cifkao.github.io/tonnetz-viz/
Real-time Tonnetz from MIDI input via Web MIDI API; major triads = downward triangles, minor = upward. **VI 7 / CD 8.** Open-source JS; a great Web MIDI starting point.

**Other Tonnetz variants** — **codedot/tonnetz** (https://github.com/codedot/tonnetz); **The Tonnetz** (https://thetonnetz.com/, generalized (a,b,c) Tonnetz, MIDI loading, dual trace); **Chord Progressor** (https://chordprogressor.com/, P/L/R minimal-voice-leading moves with Web Audio); **nami-lab deformed Tonnetz** (http://nami-lab.com/tonnetz/examples/deformed_tonnetz_int_sound_pers.html, a 3-D lattice deformed by a phrase, with sound; from arXiv 1602.00739). Collectively these cover flat, toroidal, generalized, and deformed Tonnetz variants. **VI 7–8 / CD 9.**

**Dmitri Tymoczko — ChordGeometries / orbifolds** — https://dmitri.mycpanel.princeton.edu/ChordGeometries.html ; paper: "The Geometry of Musical Chords," *Science*, 7 July 2006, Vol. 313, No. 5783, pp. 72–74 (DOI 10.1126/science.1126287) — the first music-theory article published in *Science*'s then-127-year history. Its abstract reads: "A musical chord can be represented as a point in a geometrical space called an orbifold. Line segments represent mappings from the notes of one chord to those of another." Famous demos show Chopin's E-minor Prelude on a Möbius strip and 4-D seventh-chord space; the 2-note chord space is the Möbius strip T²/S₂. **VI 8 / CD 10.** Original is a Max/MSP app, but a browser reimplementation exists: **caseykolb/chord-geometries** — https://github.com/caseykolb/chord-geometries. The 2-note Möbius strip is very achievable in Three.js.

**Open Music Theory — Neo-Riemannian chapter** — https://viva.pressbooks.pub/openmusictheory/chapter/neo-riemannian-triadic-progressions/
Clear pedagogical Tonnetz + PLR transformation reference. **CD 9.**

### Category 5 — Spectral / audio-reactive visualizations

**Neon Mandala** — https://neonmandala.art/
Browser music visualizer using WebGL 2.0 + FFT, separating bass/mid/high via a Web Worker to drive radial-symmetry mandala parameters; 60fps, 15 palettes, 10 patterns. **VI 9 / CD 5.** Excellent reference for an audio-reactive FFT mandala.

**saskaZs/FFT-Visualization** — https://github.com/saskaZs/FFT-Visualization
"Digital mandala": custom recursive Cooley-Tukey FFT mapped to a 12-segment polar pattern with Hanning window, beat-detection rotation, alpha-trail persistence. **VI 8 / CD 7.** Port the polar-mapping idea to Web Audio AnalyserNode.

**CodePen spectrum/spectrogram references** — https://codepen.io/TF3RDL/details/VwENJbB (custom-FFT spectrum+spectrogram), https://codepen.io/SolarLiner/pen/QbvgzN (log spectrogram), https://codepen.io/njsteele/pen/abzKjzv (mic spectrogram), https://codepen.io/fgnass/pen/LWeKNq (Siri-style).
Direct Web Audio + Canvas references. **VI 7 / CD 6.**

**Chromagram visualization.** The chromagram folds the spectrum into 12 pitch classes — a spectral cousin of the chroma circle; refs at isca-archive (Wakefield) and audiolabs-erlangen FMP. **VI 6 / CD 8.** Web Audio + chroma-folding math.

### Category 6 — Consonance/dissonance and psychoacoustic curves

**Sethares dissonance-curve calculator (Aykut Çağlayan)** — https://www.aykutcaglayan.net/dissonance_curve.html
Interactive sensory-dissonance curves for any timbre using the Plomp-Levelt model; presets for harmonic/piano/bell/stretched spectra; auto-detects consonant intervals as local minima. **VI 7 / CD 10.** Directly recreatable in JS — the dissonance formula is a simple difference of exponentials.

**edo.jakim.it — Musical Harmony Analysis Tool** — https://edo.jakim.it/
Plots the Plomp-Levelt/Sethares dissonance curve (d = l[e^(−b₁s∆f) − e^(−b₂s∆f)], b₁=3.5, b₂=5.75) plus a circular harmonic display showing how well each EDO matches the harmonic series (green=good, red=poor). **VI 8 / CD 10.** Outstanding model to fork conceptually.

**Sethares originals & theory** — https://sethares.engr.wisc.edu/consemi.html (essay), https://sethares.engr.wisc.edu/forrestjava/html/TuningAndTimbre.html (legacy applet), endolith's Python `dissmeasure` gist (https://gist.github.com/endolith/3066664). The foundational papers are W.A. Sethares, "Local Consonance and the Relationship Between Timbre and Scale," *J. Acoust. Soc. Am.* 94(3), 1218–1228 (1993), DOI 10.1121/1.408175; building on R. Plomp & W.J.M. Levelt, "Tonal Consonance and Critical Bandwidth," *J. Acoust. Soc. Am.* 38, 548–560 (1965), DOI 10.1121/1.1909741. **CD 10.** Endolith's gist is the cleanest formula to port to JS.

**Sebastian Schlecht — On Musical Dissonance** — https://www.sebastianjiroschlecht.com/post/ondissonance/
Reproduces Sethares' 1993 curves and extends to a 2-D triadic dissonance heatmap (the major triad shows as a blue/consonant dip at (400,300)). **VI 8 / CD 9.** A 2-D dissonance heatmap is a striking, buildable Canvas piece.

### Category 7 — Color-music / synesthetic mappings

**Scriabin's color-to-key wheel.** Maps keys around the circle of fifths to a near-perfect color gradient; designingsound.org and Mr Mars' Musical Colour Wheel (warrenmars.com) discuss and critique it. Scriabin's full key→colour list was first published by Leonid Sabaneyev in the journal *Музыка* (Muzyka), January 1911; Scriabin and Rimsky-Korsakov famously agreed that D major was golden-brown/gold-yellow (per Rachmaninoff's *Recollections*). **VI 8 / CD 7.** A pitch/key→HSL hue mapping is a one-liner that enriches any other visualization.

**Pitch-class color synesthesia research** — https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5736759/
Averaged synesthete data: pitch classes map to rainbow hues (do=red … si=violet) with saturation/brightness encoding pitch height; the two pitch dimensions (chroma, height) map to hue-saturation vs. value. **CD 9.** An empirical basis for a principled color model.

**Malinowski's harmonic coloring (Music Animation Machine)** — http://www.musanim.com/Background/
Hue shifted along the circle of fifths to show tonality/harmony; saturation encodes interval stability (consonant = bright, dissonant/chromatic = greyish), per the roboticbuilding.eu writeup of his method. **VI 9 / CD 8.** The single most influential music-visualization body of work; the coloring algorithm is well-documented and replicable.

**musicolors (arXiv 2503.14220)** — Three.js spheres mapping pitch→color, energy, and timbre in real time. **VI 7 / CD 6.** Three.js + Pitchy + Web Audio.

### Category 8 — Notable creative coders and projects

**Alexander Chen — Baroque.me** — http://www.baroque.me/
Bach Cello Suite No. 1 Prelude visualized as plucked strings whose lengths encode Pythagorean pitch ratios (2/3 = fifth, 1/2 = octave); orbiting dots pluck the strings, and you can drag them to disrupt the system, which then re-adjusts. **VI 9 / CD 8.** HTML5 Canvas + JS + SoundManager — a landmark example of harmony-as-geometry; a Tone.js rebuild is very feasible.

**Alexander Chen — Harmonics** — https://alexanderchen.github.io/harmonics/
Simple interactive diagram to see and hear the harmonic series. **VI 7 / CD 8.** GitHub-Pages JS interactive.

**Alexander Chen — MTA.me / Conductor** — http://www.mta.me/
NYC subway map as a string instrument; crossing train lines pluck cello-pizzicato notes, driven by the real MTA schedule. **VI 9 / CD 6.** SVG-coordinate paths → Canvas + sample playback; a generative-harmony classic.

**Dmitri Tymoczko** (orbifold geometry, see Category 4), **William Sethares** (dissonance curves, Category 6), and **Stephen Malinowski** (harmonic coloring, Category 7) are the three foundational figures whose work recurs across categories.

## Recommendations

**Stage 1 — Build a quick win to learn the stack (1–2 weekends).** Start with **Lissajous interval curves** (Canvas parametric plot + Web Audio oscillators) or the **chroma/chromatic circle with chord polygons** (SVG + Tone.js). Both are small, beautiful, and teach the audio+geometry plumbing you'll reuse everywhere. Benchmark to advance: you can render a chord as a polygon and play it on click.

**Stage 2 — Build a deep interactive (a few weeks).** Pick one of: (a) a **Three.js toroidal Tonnetz** with Web MIDI input (fork TonnetzViz/Z-Tonnetz for reference); (b) a **just-intonation lattice** with audio (study osar.fr and mcmire/musical-lattice); or (c) a **Sethares dissonance-curve explorer** (port endolith's formula). Benchmark to advance: real-time interaction stays at 60fps and audio is glitch-free.

**Stage 3 — Aesthetic showpiece (open-ended).** Implement a **WebGL Chladni/cymatics shader** driven by Web Audio FFT (fork the Shadertoy shaders + the Observable example) or a **harmonic-coloring music player** à la Malinowski. These are the highest visual-impact pieces.

**Cross-cutting tech guidance:** Use **Tone.js** for scheduled musical audio and **Web Audio `AnalyserNode`** for FFT/reactive visuals; **SVG** for crisp, few-element diagrams (circles, polygons, lattices); **Canvas 2D** for many-particle/trail effects (Lissajous, spectrograms); **Three.js** for tori, helices, orbifolds, and 3-D Chladni; **raw GLSL/WebGL** for cymatics and FFT mandalas. The **Web MIDI API** unlocks live instrument input for the Tonnetz.

**To close the social-media gap (do this manually):** Run logged-in searches on Reddit (r/musictheory, r/dataisbeautiful, r/generative, r/oddlysatisfying for "circle of fifths," "Tonnetz," "chord geometry," "just intonation") and on X (search "Tonnetz," "voice leading geometry," and follow @alexanderchen, @preinfarction/microtonaltheory.com, and academic theorists such as Jason Yust and Dmitri Tymoczko). These platforms block automated search but are browseable manually.

## Caveats

- **Scores are subjective editorial judgments**, not measured values; treat them as relative rankings to prioritize your build queue.
- **Twitter/X and Reddit could not be searched by automated tools** (both block scraping/JS-render), so the specific viral posts the user prioritized are not catalogued here; I have given concrete manual-search strategies instead. The original tweet's content remains unknown.
- **"432 Hz / sacred frequency" cymatics content** (common on TikTok/YouTube) is wrapped in pseudoscientific health claims; the *visual phenomena* are real physics, but ignore the "healing frequency" framing.
- A few tools (Sethares' Java applet, Tymoczko's standalone ChordGeometries) are **legacy/desktop** and may not run in modern browsers; use the noted JS reimplementations instead.
- The Alexander Chen "Harmonics" exact tech stack (Canvas vs. Web Audio specifics) is inferred from the project type; the page is JS-rendered and didn't expose a verbatim stack statement.
