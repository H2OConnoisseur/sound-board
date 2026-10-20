# Sound Board

A phonics sound board for the iPad. Tap a letter or letter pair to hear its sound. Record your own voice for each one, with automatic trimming. Everything is saved on the device, with no accounts.

It is plain static files (`index.html`, `sw.js`, `manifest.webmanifest`, two icons). There is no build step.

## Why it needs hosting

Safari only allows microphone access on a page served from its own address over HTTPS. Opening the file directly, or through a chat preview, won't record. Any static host works.

## Deploy with GitHub Pages

1. Create a new GitHub repository (public is simplest), for example `sound-board`.
2. Push the contents of this folder to it:
   ```
   git init
   git add .
   git commit -m "Sound Board"
   git branch -M main
   git remote add origin https://github.com/<you>/sound-board.git
   git push -u origin main
   ```
3. In the repo, go to Settings, then Pages. Set the source to the `main` branch and the `/ (root)` folder, then save.
4. After a minute or two the site is live at `https://<you>.github.io/sound-board/`.

Netlify Drop (drag this folder onto app.netlify.com/drop) also works and needs no git.

## On the iPad

1. Open the site's link in Safari and tap **Allow** when asked about the microphone.
2. Tap Share, then **Add to Home Screen**.
3. Open it from the Home Screen icon and record the sounds there.

Recordings are stored per web address and per browser. Record on the final address, from the Home Screen icon, and don't move the site afterwards.
