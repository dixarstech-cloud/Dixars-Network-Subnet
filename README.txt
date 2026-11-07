# Dixars SubnetLab PWA

## Deploy to GitHub Pages
1. Upload `index.html`, `manifest.json`, `sw.js`, and the `icons/` folder to the same directory in your GitHub repository.
2. In GitHub, open **Settings → Pages**.
3. Select the branch and folder containing these files (usually `main` and `/root`), then save.
4. Open the published HTTPS URL. The first visit downloads the app shell; subsequent visits can work offline.

## Install
Open the published site in a supported browser. Use the browser's **Install app / Add to Home Screen** option. The in-page Install button appears only when the browser exposes an install prompt.

## App display and phone status bar
The installed app opens in a standalone app window that fills the available screen area while keeping the phone status/notification bar visible. It does not request immersive fullscreen. Install it from the browser menu or the in-page Install button when available.

## Notes
- Service workers require HTTPS (GitHub Pages provides HTTPS) or localhost.
- Offline availability begins after the service worker has installed and cached the app shell once.
- If you update the app, change `CACHE_NAME` in `sw.js` (for example, `v2`) to publish a new cache version.
