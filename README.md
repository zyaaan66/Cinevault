# 🎬 CineVault

**CineVault** is a premium, cinema-vault themed movie & series discovery app built as a front-end portfolio project. It lets users browse a curated film collection, search and filter by genre, view detailed info in a playbill-style modal, and save titles to a personal watchlist ("The Vault") — all wrapped in a distinctive dark, marquee-poster visual identity instead of a generic template look.

🔗 **Live demo:** https://zyaaan66.github.io/Cinevault/

---

## ✨ Features

- 🔍 **Real-time search** — debounced search across movie titles and synopses
- 🎞️ **Genre filtering** — quick filter chips (Action, Drama, Sci-Fi, Comedy, Horror, Animation, Thriller, Romance)
- 🪧 **Detail modal** — playbill-style layout with rating, runtime, director, genre tags, and a trailer link
- 🎟️ **Personal watchlist ("Vault")** — add/remove titles via a slide-in drawer, with live counter and toast confirmation
- 🖼️ **Adaptive poster art** — shows the real poster when available, and falls back to custom-generated CSS poster art (film-grain texture, accent gradient, sprocket-hole border) when it isn't
- ⌨️ **Accessible & responsive** — keyboard support (`Esc` to close), visible focus states, mobile-friendly layout
- 🌗 **Distinctive visual identity** — dark "film vault" palette, marquee/condensed typography, film-strip sprocket dividers, and ticket-stub notch buttons as a consistent signature motif

## 🛠️ Tech Stack

- Plain **HTML, CSS, and JavaScript** — no build tools or frameworks required
- [OMDb API](https://www.omdbapi.com/) for real movie data (poster, rating, plot, genre, director, runtime)
- Google Fonts: `Oswald`, `Inter`, `JetBrains Mono`

## 🚀 Getting Started

This is a single self-contained `index.html` file — no installation needed.

1. Clone or download this repository
2. Get a free API key at [omdbapi.com/apikey.aspx](https://www.omdbapi.com/apikey.aspx) (check your email to activate it)
3. Open `index.html` and set your key in the `CONFIG` object near the top of the `<script>` tag:
   ```js
   const CONFIG = {
     OMDB_API_KEY: 'YOUR_KEY_HERE',
     // ...
   };
   ```
4. Deploy the file with any static host (GitHub Pages, Netlify, Vercel, etc.) — **note:** opening the file directly from your local filesystem (`file://`) will cause the API requests to be blocked by the browser's CORS policy, so it must be served over `http(s)` to fetch live data.

> Without an API key, the app automatically falls back to a small built-in sample dataset, so the UI remains fully functional and demonstrable out of the box.

## 📂 Curated Collection

Since OMDb has no "discover/trending" endpoint, the app fetches a hand-picked list of well-known titles by IMDb ID (defined in `OMDB_CURATED_IDS`). You can freely edit this list to change which films appear.

## 📌 Notes

- Data is provided by [OMDb API](https://www.omdbapi.com/), sourced from IMDb.
- This project is intended for educational/portfolio purposes (non-commercial use).

## 📄 License

MIT — feel free to fork and adapt.
