# ToastTomate Dashboard 🍅

A dark, responsive Discord music-control dashboard for ToastTomate.

## Publish with GitHub Pages
1. Open **Settings → Pages** in this repository.
2. Under **Build and deployment**, choose **Deploy from a branch**.
3. Select branch `main` and folder `/ (root)`, then Save.
4. Wait for GitHub Pages to publish the site.

## Local music bridge
The page expects your Node.js Discord bot to expose these endpoints on `http://127.0.0.1:3210`:
- `GET /api/music/status`
- `POST /api/music/command` with an action such as `join`, `play`, `pause`, `resume`, `skip`, `stop`, `leave`, or `volume`

**Important:** the UI has been added, but these endpoints must still be implemented in your existing local bot before controls can actually play audio. The browser also needs CORS support from the local bridge. Never put your Discord bot token in this repository or in browser-side code.

Spotify URLs can be used as metadata/search input, but the bot cannot directly play Spotify's protected audio stream. Actual playback requires a supported audio source.
