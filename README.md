# Stone Harbor Tradeworks Job Board: home-screen app

<img src="icon-192.png" width="96" alt="Stone Harbor app icon">

A small installable web app that puts **Stone Harbor Tradeworks Job Board** on your phone's home screen (or your computer's app list)
with its own icon and name. Tap the icon and it opens the board.

- **Install page:** https://tom-kraus87.github.io/stone-harbor-app/
- **The board:** https://claude.ai/artifact/NMrLjeQgfMXiiNiEDpo5pV (private: it opens only for people it's shared with, signed in to Claude)

## Why this exists

The board runs inside Claude's page. Saving the board link to your home screen gives you Claude's icon, or opens
the Claude app, which has no "Add to Home Screen" option. This launcher has its own icon and name, and opening it
goes straight to the board.

## Install it

Open **https://tom-kraus87.github.io/stone-harbor-app/** on the device. The page detects your phone and shows the right steps.

| Device | Steps |
|---|---|
| **iPhone / iPad** | Open the link in **Safari**. Tap **Share**, then **Add to Home Screen**, then **Add**. Tap the **Stone Harbor** icon. |
| **Android** | Open the link in **Chrome**. Tap **Install the app** (or **⋮**, then **Add to Home screen**). Tap the **Stone Harbor** icon. |
| **Computer** | In Chrome or Edge, click the install icon in the address bar. On a Mac in Safari: **File, then Add to Dock**. |

If you opened the link inside another app (Gmail, Messages, Facebook, the Claude app), the page tells you to
open it in Safari or Chrome first and gives you a **Copy link** button.

The first time you open it, Claude may ask you to sign in. Use the email the board was shared with.

## What's in this repo

| File | What it does |
|---|---|
| `index.html` | The install page, and the screen that opens the board when you launch the app |
| `manifest.webmanifest` | The app's name, icon and colors, so phones can install it |
| `sw.js` | A small service worker so the launcher loads instantly and works offline (the board itself always loads live) |
| `icon-192.png`, `icon-512.png`, `icon-maskable-512.png`, `apple-touch-icon.png`, `favicon-32.png` | App icons |

There is no board data, no team data and no passwords here. It's safe for this repo to be public.

## Hosting

GitHub Pages serves this repo at https://tom-kraus87.github.io/stone-harbor-app/
(**Settings, then Pages**, Source: **Deploy from a branch**, Branch: **main** / **(root)**).

## Making changes

These files are generated. Edit `tools/launchers/make_launchers.py` in the board's private repo (name, icon,
colors, board link), run `python3 make_launchers.py`, and copy the output folder here. To change the icon on a phone
that already has it, remove the app from the home screen and add it again.

Stone Harbor Tradeworks
