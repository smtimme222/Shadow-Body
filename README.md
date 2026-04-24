# Shadow Body

Real-time full body shadow puppet theater that runs entirely in your browser. Step in front of your webcam and your body is cast as a silhouette onto an animated stage — no installation, no backend, just HTML and a camera.

---

## Demo

> Allow camera access, step back so your full body is visible, and click **Raise the Curtain**.

---

## Features

- **Full body silhouette** — tapered limbs, curved torso, oval head, and shaped feet built from 33 pose landmarks
- **Real finger tracking** — MediaPipe Holistic tracks all 21 landmarks per hand, rendering individual fingers that move with you
- **3 animated scenes** — switch between them live while performing
  - 🌅 **Sunset Forest** — layered pine silhouettes, floating embers, sun glow
  - 🌃 **City Night** — multi-depth building skyline, lit windows, twinkling stars
  - 🌊 **Underwater** — animated light rays, swaying seaweed, rising bubbles
- **Parallax** — background layers shift as your body moves left and right
- **Tracking visualizer** — toggle to see the raw MediaPipe skeleton and landmark dots color-coded by body region
- **Camera overlay** — transparency slider to blend your live webcam feed over the puppet stage

---

## How to Use

1. Open `index.html` in a modern browser (Chrome or Edge recommended)
2. Allow camera access when prompted
3. Step back 6–8 feet so your full body fits in frame
4. Click **Raise the Curtain**
5. Use the controls at the bottom to switch scenes or toggle tracking

### Controls

| Control | Description |
|---|---|
| Scene buttons | Switch between Forest, City, Underwater |
| **Show Tracking** | Toggle MediaPipe landmark overlay |
| Camera slider | Fade live camera feed over the stage |

### Tracking Dot Colors

| Color | Body Region |
|---|---|
| Cyan | Face |
| Green | Arms & shoulders |
| Yellow | Hips |
| Orange | Legs |
| Gold | Hands & fingers |

---

## Tech Stack

| Library | Purpose |
|---|---|
| [MediaPipe Holistic](https://google.github.io/mediapipe/solutions/holistic) | Full body + hand landmark detection |
| [MediaPipe Camera Utils](https://www.npmjs.com/package/@mediapipe/camera_utils) | Webcam frame loop |
| HTML5 Canvas | All rendering — scenes, silhouette, particles |

Everything runs client-side. No server, no dependencies to install, no build step.

---

## Running Locally

```bash
git clone https://github.com/smtimme222/Shadow-Body.git
cd Shadow-Body
# Open in browser — use a local server if camera doesn't work over file://
npx serve .
# or
python3 -m http.server 8080
```

> **Note:** Most browsers require a secure context (localhost or HTTPS) to access the camera. If opening the file directly doesn't work, use a local server as shown above.

---

## License

MIT
