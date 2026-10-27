# Fjord

The microphone only works over HTTPS, so the files need a host. Any static host works; GitHub Pages is free:

1. Create a repo (e.g. `fjord`) and push these files to its root.
2. Settings → Pages → Source: *Deploy from a branch*, branch `main`, folder `/ (root)`.
3. Open `https://<you>.github.io/fjord/` on your phone.
4. **Android (Chrome):** menu → *Add to Home screen* / *Install app*.
   **iPhone (Safari):** Share → *Add to Home Screen*.

Allow the microphone when asked. Everything after that runs on the device; the app works offline except for the first font download.

## Voices

keyspeak uses the system's text-to-speech voices. For the right ä, ö, ü and y, install a Swedish, Norwegian, Danish or German voice:

- **iOS:** Settings → Accessibility → Spoken Content → Voices → Swedish (or German) → download one.
- **Android:** Settings → General management → Text-to-speech → Google TTS → Install voice data → Swedish.

Pick it in the app's settings (gear icon). The app prefers Swedish → Norwegian → Danish → German automatically if one is installed.

## iPhone note

Speech recognition in an installed (home-screen) web app works on iOS 17 and later. On older iOS, open it in Safari instead, or type in the text box.

## Files

- `index.html` — the whole app (grammar layer, Fjord phonology, speech, flashcards)
- `manifest.webmanifest`, `sw.js`, `icons/` — install and offline support

## Changing the language

Everything linguistic is at the top of the script in `index.html`: `UNI`/`BIGRAMS` (the grammar layer), `PARTICLES` (the flashcards), `FJ_C`/`FJ_V` (the Fjord sound rules). Edit, bump `CACHE` in `sw.js`, redeploy.
