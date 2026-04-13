# Particle Text

2000 particles floating on screen gather to form the text you type.

**Live Demo**: [prayer168.github.io/particle-type2](https://prayer168.github.io/particle-type2/)

## Features

- **Real-time particle text** — Type in the input box and watch 2000 particles slowly converge into your words
- **Chinese & English** — Supports both languages, up to 40 characters
- **Smooth transitions** — When text changes, particles migrate between characters using nearest-neighbor matching. Existing letters stay intact while edge particles peel off to form new ones
- **Mouse interaction** — Move your cursor near particles to push them away; they drift back after you leave
- **Dreamy physics** — Soft spring attraction with high damping creates a slow, meditative convergence
- **Scatter effect** — Clear the text and particles gently burst outward before resuming their drift

## How It Works

1. **Text sampling** — Input text is rendered on an offscreen canvas, then pixel positions are extracted by scanning alpha values
2. **Target assignment** — Each particle is matched to its nearest available target pixel, so transitions between different text are spatially coherent
3. **Spring physics** — Particles accelerate toward their target with a weak spring force (`0.003`) and high friction (`0.965`), resulting in ~3 second convergence
4. **Wandering** — Particles without targets drift slowly via random-walk steering with very low acceleration
5. **Mouse repulsion** — A radial force pushes particles away from the cursor within a 120px radius

## Tech Stack

Single HTML file — HTML5 Canvas + vanilla JavaScript. No dependencies.

## Run Locally

Open `index.html` in any modern browser. No build step needed.
