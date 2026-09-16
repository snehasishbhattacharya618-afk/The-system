# THE SYSTEM — self-hosted PWA

This folder is a complete, installable web app. Deploy it for free in about 2 minutes.

## Fastest option: GitHub Pages

1. Create a free GitHub account if you don't have one.
2. Create a new repository (e.g. `the-system`).
3. Upload all 5 files in this folder (`index.html`, `manifest.json`, `sw.js`, `icon-192.png`, `icon-512.png`) to the repo root — drag and drop works on github.com.
4. Go to the repo's **Settings → Pages**.
5. Under "Source," pick the `main` branch and `/root` folder, then save.
6. Wait ~1 minute. Your app will be live at:
   `https://YOUR-USERNAME.github.io/the-system/`

## Even faster: Netlify Drop

1. Go to https://app.netlify.com/drop
2. Drag this entire folder onto the page.
3. You get an instant live URL — no account required for a quick test (create a free account to keep it permanent).

## Installing on your phone (and your friends')

1. Open the deployed link in Chrome (Android) or Safari (iPhone).
2. Tap the browser menu → **"Add to Home Screen"** (or **"Install app"**).
3. It now opens full-screen with its own icon, like a native app.
4. Allow the notification permission prompt when it appears.

## Sharing with friends

Just send them the link. Each person's quest progress is stored locally on
their own device (`localStorage`) — nobody sees anyone else's data.

## Honest limits (please read)

- Notifications fire while your browser/app is running in the background,
  not after fully force-closing it or restarting your phone. True
  "closed-app" push notifications need a real backend push server
  (Firebase Cloud Messaging, etc.) — this setup doesn't include one.
- The included icons are simple placeholders. Swap `icon-192.png` and
  `icon-512.png` for your own artwork any time — same filenames, same
  folder.
- If you update `index.html` later, bump `CACHE_NAME` in `sw.js` (e.g.
  `v1` → `v2`) so the service worker knows to fetch the new version
  instead of serving the cached old one.
