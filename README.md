# NASA Space Apps Hackathon: EclipseElites

An interactive 3D web experience built for the **NASA International Space Apps Challenge**. Step aboard a spaceship, float in zero gravity, and watch total solar, partial solar, and lunar eclipses unfold in real time.

## Overview

Eclipses are rare and hard to observe. EclipseElites lets anyone explore them from the inside, with the Sun, Earth, and Moon modeled in a 3D scene you can move around in. Each eclipse type has its own info panel explaining what it is and how to observe it safely.

## Features

- First-person movement inside a spaceship corridor, with zero-gravity floating
- 3D models of the Sun and the Moon
- Viewpoint selection for each eclipse event:
  - Total solar eclipse
  - Partial solar eclipse
  - Lunar eclipse
  - Earth's domain
- Informational pop-ups for each eclipse, including safe observation tips
- Physics-based movement and collision handling
- Custom GLSL shaders (Perlin and simplex noise, distortion effects)
- Parallax backgrounds, visual effects, and an in-app instructions panel

## Controls

| Key / Action | Description |
| --- | --- |
| Click | Start the animation (loading may take a few minutes) |
| `I` | Toggle the instructions panel |
| `M` | Toggle the eclipse selection menu |
| `B` | Return to the spaceship |

**How to view an eclipse:** press `M`, pick an eclipse viewpoint before the Moon takes position, watch the Moon's rotation, and press `B` to return to the ship.

## Tech Stack

- **Three.js** for 3D rendering
- **Vite** for development and bundling
- **cannon-es** for physics
- **postprocessing** for visual effects
- **GSAP** and **Framer Motion** for animation
- **React** and **Tailwind CSS** for UI
- **GLSL** shaders for noise and distortion effects
- 3D assets in glTF / GLB format

## Repository Structure

This repository combines several iterations of the same project. They share the same engine structure.

| Folder | Description |
| --- | --- |
| `Nasa/` | Early version of the project |
| `Nasa-Space-app/` | Version with the eclipse info dialogs and controls |
| `Nasa-Space-apps/` | Version with bundled Sun, Moon, and spaceship corridor models |
| `Space-App/` | Engine and scene scaffold |
| `Space_Apps_Challenge-/` | Challenge submission version |

Each folder follows the same layout:

```
<folder>/
  src/
    index.html
    script.js
    styles.css
    js/
      2d/        # Parallax, sprites, visual effects
      3d/        # First-person controllers, GLB loader
      gd/        # Environment, events, collision systems
      shaders/   # GLSL noise and distortion shaders
  static/        # 3D models (Sun, Moon, spaceship)
  package.json
  vite.config.js
```

## Getting Started

### Prerequisites

- Node.js 16 or later
- npm

### Installation

```bash
# Clone the repository
git clone https://github.com/MayorEmpror/NASA-APPS-HACKATHON.git
cd NASA-APPS-HACKATHON

# Choose a project folder
cd Nasa-Space-apps

# Install dependencies
npm install

# Start the dev server
npm run dev
```

### Other scripts

```bash
npm run build     # Production build
npm run preview   # Preview the production build
npm run format    # Format code with Prettier
npm run lint      # Lint with ESLint
```

## Credits

- Built by **EclipseElites** for the [NASA Space Apps Challenge](https://www.spaceappschallenge.org/)
- 3D models of the Sun and Moon are included with their own `license.txt` files in the `static/` folders. Check those for attribution requirements.

## License

This project is released under the MIT License. See the `LICENSE` file in each project folder for details.
