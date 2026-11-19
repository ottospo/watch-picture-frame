# Watch Picture Frame — installable Android web app (PWA)

This is the existing Watch Picture Frame HTML plus an app manifest, icons and an offline cache.
The Bluetooth/photo-transfer logic has **not** been changed.

## Put the app online using GitHub Pages
1. Sign in to https://github.com.
2. Create a new repository, for example `watch-picture-frame` (public for GitHub Pages on a free account).
3. Extract the ZIP and upload the **contents** of this folder into the repository root, including `index.html`, `manifest.webmanifest`, `sw.js` and the `icons` folder.
4. In the repository, open **Settings > Pages**. Under **Build and deployment**, choose **Deploy from a branch**, select your default branch (usually `main`) and **/(root)**, and save.
5. GitHub will publish the page at a URL such as `https://YOUR-USERNAME.github.io/watch-picture-frame/`. Use the actual URL displayed in your repository's Pages settings.

## Install on Android
1. Open the published HTTPS link using **Google Chrome**, not HTML Viewer or Samsung Internet.
2. Chrome's menu (three dots) > **Add to Home screen** or **Install app** > confirm **Install**.
3. Start Watch Picture Frame from the new icon, grant Bluetooth permissions if asked, and click **Connect watch** on the page.
4. Choose photos from the phone, and then send JPEGs to the watch.

## Important
- Opening `index.html` as a local file does **not** install the PWA. It must be served over HTTPS.
- GitHub Pages publishes app source code publicly. Do not put personal photos in the repo. Selected photos are read locally in the browser and sent over Bluetooth, not stored on GitHub Pages by this application.
- Once the app has been loaded, the offline cache can let it open without internet, although Bluetooth features still depend on Chrome/Android device permissions and watch compatibility.
- The `Replace existing photos` mode is only enabled if the connected watch reports compatible firmware.
- If you upload a future update, change `CACHE_NAME` in `sw.js` to a new value to update the cache.
