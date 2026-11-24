# Seminar Interpreter — iPad / iPhone version

Live speech translation for seminars (Japanese ⇄ English and other languages), using Soniox or OpenAI.
This folder is the version for **iPad and iPhone**, meant to be published with **GitHub Pages**.
The app detects whether it is running on an iPhone or an iPad and adapts its layout.

© 2026 DS-Lab

## Files

| File | What it is |
|---|---|
| `index.html` | The whole app |
| `manifest.webmanifest` | Lets the iPad/iPhone install it on the Home Screen |
| `icon-180.png`, `icon-192.png`, `icon-512.png` | App icons |

**No API key is stored in these files.** Each person pastes their own key in the app. It is saved only in that device's browser.

## Publish on GitHub Pages

1. Create a repository on GitHub (for example `seminar-interpreter`) and upload the files of this folder to its main branch, at the top level (not inside a folder).
2. In the repository, go to **Settings → Pages → Build and deployment**. Set **Source** to **Deploy from a branch**, choose branch `main` and folder `/ (root)`, then click **Save**.
3. After a minute or two the app is at `https://<your-user>.github.io/seminar-interpreter/`.

> GitHub Pages sites are public. Anyone with the link can open the app, but they can't use it without their own API key.

## Install on the iPad or iPhone

1. Open the address above in **Safari**.
2. Tap **Share** → **Add to Home Screen** → **Add**.
3. Open it from the new icon. It runs full screen, without Safari's address bar.
4. The first time you press **Start**, allow the microphone.

## iPad

- **Microphone only.** The iPad can't capture Zoom/system audio.
- **No Left/Right windows.** Use *Layout → Side by side* instead.
- Bigger buttons and fields for touch. Fields use a 16px font so the device doesn't zoom in when you tap them.
- To leave full screen, tap the screen and press **✕ Exit full screen**.
- **▲ Hide menu** hides the menus without going full screen. Bring them back with **▼ Menu** (top right). They also come back by themselves if an error or warning appears.

## History (all devices)

- Swipe the history up to read earlier translations. While you read, it stops moving, grows to the free space, and a yellow **⬇ Live** button appears. Tap it, or swipe back to the bottom, to return to the live text.
- The big line shows at most 3 lines. If a sentence is longer, its beginning moves up to the history, so nothing is cut off.

## iPhone

- The menus are folded into **⚙ Settings**. **Start**, **Stop** and the sound level stay visible at the top. The menus close by themselves when you press Start.
- **Side by side** puts the two languages one above the other when the iPhone is upright, and side by side when it is turned.
- **⛶ Hide menus** hides the menus (the iPhone has no real full screen for web pages; installing it on the Home Screen already removes Safari's bars).
- Smaller default text (adjust with *Font size*), 2 history lines, and *Single* layout.
- **Keep the app open and the screen on.** If the iPhone locks or you switch apps, iOS stops the microphone. The app asks iOS to keep the screen on while it translates (iOS 16.4 or later). On older iOS, set *Settings → Display & Brightness → Auto-Lock → Never* during class.
- In a classroom, a lapel microphone connected to the iPhone works much better than the built-in microphone.

## Testing on a PC

Add `?device=iphone` or `?device=ipad` to the address to see that layout in a desktop browser.
*Help → About* shows which device the app detected.

## Updating

Replace `index.html` in the repository with the new version, and change `APP_VERSION` at the top of the script.
The device may keep the old version for a while. Close the app completely and open it again.
