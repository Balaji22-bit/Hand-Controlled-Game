# PALM — Gesture Arcade

A browser based Breakout game controlled by hand gestures. Move your index finger horizontally to steer the paddle; pinch your thumb and index finger to launch. Arrow keys and Space are available as a fallback.

## Run it

Camera access requires a secure browser context (`localhost` or HTTPS). From this folder, run:

```powershell
py -m http.server 8000
```

Then open <http://localhost:8000> in a modern browser, allow camera access, and select **Enable camera & play**. The first launch needs an internet connection to load MediaPipe and its hand landmark model. The video is processed in the browser and is not uploaded by this app.

## Controls

- Index finger position: move the paddle
- Thumb and index pinch: launch/resume
- Left / right arrows: move paddle
- Space: launch/resume
- R: restart

## Built with

- HTML Canvas for the game rendering and collision loop
- MediaPipe Tasks Vision Hand Landmarker for webcam hand landmarks
- Vanilla JavaScript; no Python, PyTorch, or build step required

## Portfolio notes

This is a small playable prototype. Useful next steps: add levels and sound, improve gesture calibration, show a tracking-confidence indicator, add a pause control, and deploy the static page over HTTPS (for example with GitHub Pages).
