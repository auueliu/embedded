# Embedded

_a navigable word space_

🔗 [auueliu.github.io/embedded](https://auueliu.github.io/embedded/)

<img width="500" alt="embedded demo" src="https://github.com/user-attachments/assets/0f3400cb-f260-4711-95d3-a92f59559058" />


Inspired by word embeddings, where words are positioned in space by meaning.

## Interaction

- Click a word to fly to it and load its related words.
- Type a word and press **explore →** (or Enter) to start somewhere new.

## How it works

- **Related words:** clicking a word queries the [Datamuse API](https://www.datamuse.com/api/) for associated words (`rel_trg`) and keeps up to 6 not already on screen.
- **3D placement:** new words are placed at random points on a spherical shell around the clicked word.
- **Text rendering:** words are HTML elements positioned in 3D with Three.js `CSS3DRenderer`, so they stay crisp and clickable. A WebGL layer renders the background.
- **Camera:** clicking sets a target position; the camera eases toward it each frame with linear interpolation.
- **Atmosphere:** 12,000 background points, exponential fog for depth, fade-in on new words, and Perlin-noise drift.

## Tech stack

Three.js (WebGL + CSS3DRenderer) · Datamuse API · netnet standard library · HTML/CSS/JavaScript

## Run locally

```bash
git clone https://github.com/auueliu/embedded.git
cd embedded
python3 -m http.server 8000
# open http://localhost:8000
```
