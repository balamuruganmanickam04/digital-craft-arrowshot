# Head Arrow Shot 🏹

A 2D archery game: drag back to aim, release to shoot, and hit the head to clear the level.
No ads, works offline, and runs in any browser or as an Android app.

**Play online:** https://balamuruganmanickam04.github.io/head-arrow-shot/ (after you enable GitHub Pages, see below)

## Features
- Endless levels that get harder: moving targets, wind, smaller heads, fewer arrows
- Head-shatter animation, particles, screen shake
- Sound effects generated in code (no audio files), with a mute button
- Best level saved on the device

## Controls
Drag anywhere to pull the bow back, release to fire. A dotted arc shows the flight path (wind is not shown in the preview).

## Scoring
| Hit | Result |
|---|---|
| Head | Level clear, 100 points + 25 per arrow left |
| Body | 30 points, level continues |
| Miss | Arrow lost |

## Project structure
```
index.html      the whole game (HTML + CSS + JavaScript)
android/        Android Studio project that runs the game in a WebView
LICENSE         MIT
```

## Run locally
Open `index.html` in a browser. No build step.

## Host on GitHub Pages
1. Push this repo to GitHub.
2. Repo **Settings > Pages > Build and deployment**: Source = *Deploy from a branch*, Branch = `main`, folder = `/ (root)`.
3. Wait a minute; the site appears at `https://<username>.github.io/<repo>/`.

## Build the Android app
1. Open the `android/` folder in Android Studio and let Gradle sync.
2. Run on a phone or emulator, or use **Build > Generate Signed Bundle / APK** for release builds.
3. The Android app loads `android/app/src/main/assets/index.html`. After you change the root `index.html`, copy it over that file so both stay in sync:
   ```
   cp index.html android/app/src/main/assets/index.html
   ```
4. Never commit your keystore (`*.jks`, `*.keystore`); the `.gitignore` already blocks them.

## License
MIT, see [LICENSE](LICENSE).
