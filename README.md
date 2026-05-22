# ❄️ snow-game-in-canvas

Experimental successor to [icegame](https://github.com/muthuishere/icegame) — uses Chrome's **HTML-in-Canvas Origin Trial** (`drawElement` / `THREE.HTMLTexture`) so the player and NPC labels, scoreboards, and checkpoint signs are real DOM nodes projected into the 3D world.

## Status

| | Behaviour |
| --- | --- |
| Chrome 148–150 desktop (with OT token or `chrome://flags/#canvas-draw-element`) | ✨ Full HTML-in-Canvas path |
| Chrome 148+ Android (same conditions) | ✨ Full HTML-in-Canvas path |
| Chrome ≤147, Safari, Firefox, iOS browsers | 🪶 Falls back to canvas-rasterized labels |

## Play

👉 https://muthuishere.github.io/snow-game-in-canvas/

## Local dev

```bash
task install
task play       # serves on :8080 and opens via Playwright
```

For the experimental path locally, launch Chrome (or Canary 149+) with the flag:

```bash
open -na "Google Chrome" --args --enable-blink-features=CanvasDrawElement http://localhost:8080
# or visit chrome://flags/#canvas-draw-element and enable it
```

## Origin trial token

To enable the API for visitors of the deployed site (without each user enabling a flag), register `muthuishere.github.io` at <https://developer.chrome.com/origintrials> for the "Canvas drawElement" trial, then paste the token into the `<meta http-equiv="origin-trial" …>` slot in `index.html`.

## Credits

Game built by **Sreevarshan · Sreejan · Magizhini**.
