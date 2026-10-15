# Sky Hop — Phone-ready deployment

## Files to upload
Upload these files and folders to the **root** of the GitHub repository:
- `index.html`
- `manifest.webmanifest`
- `sw.js`
- `icons/` (all three PNG files)

Do not put the files inside an extra nested folder. `index.html` should be at the same level as `manifest.webmanifest` and `sw.js`.

## Vercel
1. Open the existing `sky-hop-game` project in Vercel.
2. In **Settings → Git**, connect this GitHub repository if it is not already connected.
3. Commit the files to the branch Vercel deploys (usually `main`).
4. Open **Deployments** and wait for the newest deployment to show **Ready**.
5. Open the deployment URL on your phone using HTTPS.

For this plain HTML app, no build command is required. Keep the project root pointed at the folder containing `index.html`.

## Install on phone
- **Android / Chrome:** open the deployed URL, open the browser menu, and choose **Install app** or **Add to Home screen** if offered.
- **iPhone / Safari:** open the deployed URL, tap **Share**, then **Add to Home Screen**.

The service worker caches the core app files for basic offline launching after the app has loaded successfully once. A fresh deployment may take a moment to replace older cached files on a device; reload the page after updating.
