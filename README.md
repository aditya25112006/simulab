# SIMULAB — Simulation Studio

A React + TypeScript + Vite physics-video editor. Matter.js runs two independent arenas; the final 1080×1920 canvas composites the title, labels, grid arenas, scoreboards, damage bars and timeline. MediaRecorder captures that final canvas as a real WebM.

## Run locally

```bash
npm install
npm run dev
```

Open the local URL printed by Vite (normally http://localhost:5173).

## Production build

```bash
npm run build
npm run preview
```

## Notes

- Use Chrome or Edge for the most reliable WebM recording support.
- Export records the full composition at 30fps and 12Mbps, for the configured duration.
- Physics randomness is seeded. The same configuration and seed produce the same initial arrangement and velocities.
- Collision damage is counted from Matter.js `collisionStart` pairs. A resting contact is not repeatedly counted every frame.
- The default arena dimensions are 480×820 simulation units and are scaled into the portrait output.
