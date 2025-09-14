# Hypnagogia

Hypnagogia is a live audio-visual dance performance that inhabits the threshold between sleep and waking, where nightmares take form. It unfolds as a journey into the recesses of the mind, tracing visions and figures that are at once unsettling and strangely alluring. Rooted in a Gothic aesthetic, it treats the nightmare as a mirror rather than a threat — a place where dread may shift into wonder. The performance is a dialogue between music, dance, computer vision, tracking systems, and generative AI, where the dancer’s gestures are captured in real time, transformed into data, and expanded into dreamlike images that hover between the tangible and the spectral.

## About the Repository

This repository contains the TouchDesigner project files that drive the Hypnagogia performance.

- A Kinect camera captures the dancer’s hand movements in real time.
- These gestures are passed as inputs into the streamDiffusion.tox component (by DotSimulate), which generates AI-driven imagery.
- A curated list of text prompts is used to guide the diffusion outputs, shaping the dreamlike aesthetic.
- In parallel, multiple procedural visual effects are organised into groups inside TouchDesigner.
- These groups are triggered by musical events, synchronising sound, gesture, and generative visuals.
- A VJ controls high-level parameters, balancing the raw presence of the dancer with the shifting visual atmospheres.

Together, this system allows movement, music, and computation to converge into a live performance environment where nightmares become visible landscapes.

## Repository Structure

When cloning this repository, please recreate the following structure in your local environment.  
Some folders (e.g. `Backup`, large media assets) are excluded from Git and must be created manually.

```
Root Folder
│-- file.toe
│-- file-xx.toe
│-- Backup
│ └── backup files (...)
│-- media
│-- toxes
│ └── streamDiffusion.tox
```

- **`.toe` files** – TouchDesigner project files for Hypnagogia.
- **Backup/** – Backup files (not versioned).
- **media/** – Supporting media assets (not included in repo).
- **toxes/** – External components, notably `streamDiffusion.tox`.

---

## Requirements

- [TouchDesigner](https://derivative.ca/) (latest stable build recommended)
- GPU capable of real-time AI inference
- [`streamDiffusion.tox`](https://www.patreon.com/dotsimulate) by **DotSimulate**
- (Optional) external tracking system (camera + computer vision pipeline)

---

## Setup

1. Clone this repository:
   ```bash
   git clone https://github.com/luiz-flamorim/Hypnagogia-02.git
   ```
2. Download streamDiffusion.tox from DotSimulate and place it in:
   toxes/streamDiffusion.tox
3. Ensure required media files are added to the media/ folder.
4. Open file.toe in TouchDesigner to begin.

## Usage

- Run the .toe file in TouchDesigner.
- Connect the tracking system (camera, MediaPipe, etc.) to capture dancer gestures.
- Use the VJ controls inside the patch to adjust:
  - Blend between live video and AI imagery
  - Intensity of generative visuals
  - Layering of dreamlike atmospheres

## Media

Please visit my personal [website](https://lamorim.art/hypnagogia) for more information about the performance

## Credits

- **Concept creation & graphics:** Luiz Amorim
- **Dance performance & choreography:** Marilia Silva
- **Music:** Henry Dearden
- **Photos:** Randolfe Camarotto
- **AI Component:** streamDiffusion.tox by DotSimulate

## Licence

This project is licensed under the **Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International (CC BY-NC-ND 4.0)**.

You may share the work with attribution, but you may not use it commercially or create derivative works without explicit permission.  
See the [full licence](LICENSE.md) for details. lease note that streamDiffusion.tox is a third-party component provided by DotSimulate and is subject to their own licensing and distribution terms.
