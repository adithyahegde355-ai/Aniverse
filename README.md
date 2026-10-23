# AniVerse — Full Project

AniVerse is a responsive anime discovery web app designed to run in a browser and be packaged as an Android APK.

## Features
- Browse top-rated anime from the public Jikan API
- Search anime by title
- Explore anime by genre
- View synopsis, score, episodes, release year, and trailer when available
- Save and remove anime from a local watchlist (saved on the device/browser)
- Responsive layout for phones, tablets, and desktop
- GitHub Actions workflow to build a debug APK and publish it to GitHub Releases

## Requirements
- Node.js 20 or newer (Node 22 recommended)
- npm
- Internet access for live anime data and poster images

## Run locally
1. Extract this ZIP.
2. Open a terminal in the extracted `AniVerse-Full-Project` folder.
3. Run `npm install`.
4. Run `npm run dev`.
5. Open the local address printed by Vite.

## Build the website
```bash
npm install
npm run build
```
The built site is written to `dist/`.

## Build an Android APK with GitHub
1. Create a GitHub repository.
2. Upload the contents of this folder (upload the files and folders, not just the ZIP).
3. Ensure the workflow file `.github/workflows/build.yml` is included.
4. Commit to the `main` branch.
5. Open the **Actions** tab and run **Build AniVerse Android APK**.
6. When successful, download `AniVerse.apk` from the run's Artifacts or from the generated GitHub Release.

The workflow creates an installable **debug APK for testing**. It is not a production-signed Play Store release.

## Data and privacy
- Anime data comes from the public Jikan API, which provides MyAnimeList data. Availability and rate limits are controlled by that service.
- Your watchlist is saved in local storage on the current device/browser.
- There is no custom backend, account system, or cloud sync.
- Anime posters and Google Fonts require internet access.
