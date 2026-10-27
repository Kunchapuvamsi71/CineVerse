# CineVerse — One World. Every Movie. Every Language.

CineVerse is a responsive movie discovery website built with HTML, CSS, and vanilla JavaScript. Browse movies by title, original language, genre, year, and rating; open movie details; and save favorites or a watchlist on your device.

> **Important:** Demo-mode movie entries are illustrative sample data, not verified real movie listings. Add a TMDB API key for real movie metadata. CineVerse does not host or stream movies.

## Features

- Dark cinematic responsive interface
- All-language discovery, with Indian regional and international language filters
- Search, language, genre, year, rating, and sort controls
- Trending, popular, all-movies, favorites, and watchlist views
- Movie detail modal
- Favorites and watchlist stored with `localStorage`
- Demo mode works without an API key
- TMDB integration for real data when configured
- Friendly loading, empty, and fallback states

## Technologies

- HTML5
- CSS3
- Vanilla JavaScript
- TMDB API (optional)
- Browser localStorage
- GitHub Pages

## Project structure

```text
CineVerse/
├── index.html
├── style.css
├── script.js
├── README.md
├── LICENSE
├── .gitignore
└── assets/
    └── favicon.svg
```

## Run locally

### Quick option

1. Download or clone this repository.
2. Open `index.html` in a modern browser.

Some browser setups restrict API requests from local files. If you use the TMDB API, run a local web server instead.

### Windows local server

If Python is installed, open PowerShell in the project folder and run:

```powershell
py -m http.server 8000
```

Then visit `http://localhost:8000`.

### Android

You can upload the files to a GitHub repository and enable GitHub Pages, then open the published site on your phone. Alternatively, use a code editor that supports a local HTML preview.

## Enable live TMDB data

1. Create an account at [The Movie Database](https://www.themoviedb.org/).
2. Request an API key from your account settings.
3. For a quick local learning demo, open `script.js` and set:

   ```js
   const TMDB_KEY = "YOUR_TMDB_V3_API_KEY";
   ```

4. Refresh the website using a local server.

**Security note:** Do not commit API credentials to a public repository. A key embedded in client-side JavaScript is visible to visitors. For a public production site, use a backend or serverless proxy to keep secrets private. If you add a key for local testing, remove it before pushing code.

TMDB API documentation: https://developer.themoviedb.org/docs

## Deploy with GitHub Pages

1. Create a GitHub repository named `CineVerse` (or another name you prefer).
2. Upload the project files to the repository's root.
3. Open **Settings → Pages**.
4. Under the build and deployment section, select **Deploy from a branch**.
5. Choose the `main` branch and `/ (root)`, then save.
6. Wait for GitHub Pages to publish the site. The exact URL will be shown in the Pages settings.

Do not put a private API key in the public repository. Demo mode works without it.

## Git commands

Run these in the project folder after creating the GitHub repository:

```bash
git init
git add .
git status
git commit -m "Build CineVerse movie discovery website"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/CineVerse.git
git push -u origin main
```

Replace `YOUR-USERNAME` with your actual GitHub username. If Git says the remote already exists, inspect it with `git remote -v` before changing it.

## Supported languages

The interface includes filters for Telugu, Tamil, Hindi, Malayalam, Kannada, Bengali, Marathi, Punjabi, Gujarati, Odia, Assamese, English, Korean, Japanese, Chinese, Spanish, French, German, Italian, Portuguese, Turkish, Thai, Indonesian, Arabic, Russian, Persian, and additional languages supported by TMDB.

The database and API do not guarantee literally every movie ever made. Results depend on available metadata, API coverage, region, and pagination.

## Screenshots

Add your own screenshots here after running the project, for example:

```md
![CineVerse home page](screenshots/home.png)
```

No screenshots are included yet.

## Known limitations

- Without a TMDB key, the site uses a small set of illustrative demo entries.
- The demo list is not exhaustive and its descriptions/ratings are sample content.
- Favorites and watchlist are stored in the current browser only; they do not sync between devices.
- TMDB API keys embedded in front-end code are public to site visitors.
- Streaming availability is not provided; this is a discovery-only project.
- Poster availability depends on the source metadata.

## Future improvements

- Serverless API proxy and secure configuration
- Advanced filters and multi-language title search
- Dedicated language pages and richer pagination
- Automated tests and accessibility audit
- Watch-provider links using authorized availability data

## Attribution

When using TMDB data, comply with the current [TMDB API terms and attribution requirements](https://www.themoviedb.org/api-terms-of-use). This product uses the TMDB API but is not endorsed or certified by TMDB.

## Author

- **Name:** Your Name
- **GitHub:** https://github.com/YOUR-USERNAME

## License

This project code is released under the MIT License; see [`LICENSE`](LICENSE). This license does not grant rights to third-party movie artwork or metadata.
