# Seminar Interpreter — iPad version

Live speech translation for seminars (Japanese ⇄ English and other languages), using Soniox or OpenAI.
This folder is the iPad version, meant to be published with **GitHub Pages**.

© 2026 DS-Lab

## Files

| File | What it is |
|---|---|
| `index.html` | The whole app |
| `manifest.webmanifest` | Lets the iPad install it on the Home Screen |
| `icon-180.png`, `icon-192.png`, `icon-512.png` | App icons |

**No API key is stored in these files.** Each person pastes their own key in the app; it is saved only in that iPad's browser.

## Publish on GitHub Pages

1. Create a repository on GitHub (for example `seminar-interpreter`) and upload the files of this folder to its main branch.
2. In the repository: **Settings → Pages → Build and deployment → Source: Deploy from a branch**, branch `main`, folder `/ (root)`, then **Save**.
3. After a minute or two the app is at `https://<your-user>.github.io/seminar-interpreter/`.

> GitHub Pages sites are public. Anyone with the link can open the app, but they can't use it without their own API key.

## Install on the iPad

1. Open the address above in **Safari**.
2. Tap **Share** → **Add to Home Screen** → **Add**.
3. Open it from the new icon: it runs full screen, without Safari's address bar.
4. The first time you press **Start**, allow the microphone.

## Differences from the PC version

- **Microphone only.** The iPad can't capture Zoom/system audio.
- **No Left/Right windows.** Use *Layout → Side by side* instead.
- Bigger buttons and fields for touch. Fields use a 16px font so the iPad doesn't zoom in when you tap them.
- To leave full screen, tap the screen and press **✕ Exit full screen**.

## Updating

Replace `index.html` in the repository with the new version, and change `APP_VERSION` at the top of the script.
The iPad may keep the old version for a while. Close the app completely and open it again.
