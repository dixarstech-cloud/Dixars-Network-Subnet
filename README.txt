# Octavex PWA  (all files in ONE folder - no icons/ subfolder)

Files to upload together to the same directory of your GitHub repository:
  index.html            the app
  manifest.json         install information
  sw.js                 offline engine (service worker)
  icon-192.png  icon-512.png  icon-512-maskable.png  apple-touch-icon.png   app icons

## Deploy to GitHub Pages
1. Upload ALL the files above to the same folder (repository root is simplest).
2. Settings -> Pages -> choose the branch (main) and the folder (/root) -> Save.
3. Open the published https:// link. The first visit downloads the app and the offline engine.

## Icon is created automatically
When the link is opened the page draws the app icon itself (tab icon, iPhone/iPad home-screen icon) and,
if the icon PNG files are ever missing, builds an install-ready manifest on the fly. Nothing to do by hand.

## Install
- Android / Chrome / Edge / desktop: an "Install Octavex" bar appears a moment after the page opens
  (also the "+ Install app" button in the header). Tap Install. Browsers do not allow installing without a tap.
- iPhone / iPad (Safari): tap Share -> Add to Home Screen (the bar shows this hint).
The installed app opens in its own window with the phone status bar visible and works with no internet.

## Updating
Upload the new files, then change CACHE_NAME in sw.js (v3 -> v4). Open pages refresh the cache in the background
and show the new version on the next launch.

## Notes
- Service workers need HTTPS (GitHub Pages is HTTPS) or localhost; opening index.html straight from disk still works as a normal page.
- Offline use starts after the first successful online visit.
