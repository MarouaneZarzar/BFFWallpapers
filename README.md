# BFF Wallpapers

Online wallpaper list for the **Best Friend Wallpapers** Android app.
The app downloads `wallpapers.json` from this repo every time it opens.

## Add wallpapers
1. Put the image in `images/` (for example `images/51.jpg`).
2. Add an entry to the `wallpapers` array in `wallpapers.json`:
   ```json
   { "id": 51, "url": "https://raw.githubusercontent.com/MarouaneZarzar/BFFWallpapers/main/images/51.jpg" }
   ```
3. Commit and push. No app update needed.

## Announce an app update
1. Publish the new version on Google Play and wait until it's live.
2. In `wallpapers.json`, set `update.latestVersionCode` to the new `versionCode`.
3. Set `"force": true` only if old versions must stop being used (the dialog can't be dismissed).

Users on an older version will see the update dialog with your `message` the next time they open the app.

Note: GitHub can take up to ~5 minutes to serve the new file after a push.
