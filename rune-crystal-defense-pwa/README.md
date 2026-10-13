# Rune Crystal Defense - GitHub + PWABuilder package

Upload the files in this folder to the ROOT of a GitHub repository (index.html must be at the top level).

## 1. Put it on GitHub Pages
1. Create a new public repository on github.com (for example `rune-crystal-defense`).
2. Upload everything from this folder: `index.html`, `manifest.webmanifest`, `sw.js`, `.nojekyll`,
   the `icons/` folder and the `screenshots/` folder. (Make sure the hidden `.nojekyll` file is included.)
3. Repository Settings > Pages > Build and deployment > Source: "Deploy from a branch",
   Branch: `main`, folder `/ (root)`, then Save.
4. After a minute your game is live at `https://YOUR-NAME.github.io/rune-crystal-defense/`.
   Open it once and check it loads.

## 2. Convert with PWABuilder
1. Go to https://www.pwabuilder.com, paste your GitHub Pages URL, press Start.
2. Manifest, service worker and icons should all pass.
3. Package for stores > Android. Pick a package ID (for example com.yourname.runecrystal), then Generate.
   Keep the signing key and passwords PWABuilder gives you.
4. Install the .apk on a phone to test, or upload the .aab to Google Play.
5. Put the `assetlinks.json` PWABuilder gives you into a `.well-known` folder in the repository
   (`.well-known/assetlinks.json`) so the app opens full screen.

## Notes
- All paths are relative, so it works from a repository sub-folder such as /rune-crystal-defense/.
- The app is landscape only (manifest orientation + in-game rotate message).
- Progress and saves use localStorage, which persists inside the installed app.
- The Silkscreen font loads from Google Fonts online; a system monospace font is used if it is unavailable.
