<div align="center">

# aadhyapan.github.io

**The official download site for the Aadhyapan Android app.**

[![Website](https://img.shields.io/badge/website-aadhyapan.github.io-1a73e8.svg)](https://aadhyapan.github.io/)
[![Hosted on GitHub Pages](https://img.shields.io/badge/hosted%20on-GitHub%20Pages-222.svg)](https://pages.github.com/)

[**Visit the site**](https://aadhyapan.github.io/) · [Android source code](https://github.com/Aadhyapan/Aadhyapan-Android-Client-Source-Code) · [Report an issue](../../issues)

</div>

---

## About

This repository is the source of [aadhyapan.github.io](https://aadhyapan.github.io/), a minimalist static website where anyone can download the Aadhyapan Android app (`aadhyapan.apk`) for free.

The app was once a paid product, sold for around $100 by a Nepali software company. It is now open source, and this site is the simplest way to get it. The site was made to credit and celebrate [Raman Chapagain](https://ramanchapagain.github.io/), the developer behind it.

No frameworks, no build step, no trackers. Just HTML, one CSS file, and the APK.

## What's inside

```
.
├── index.html        # Home page with the APK download button
├── privacy.html      # Privacy policy (for this website and repo)
├── terms.html        # Terms of use (for this website and repo)
├── sitemap.html      # Human-readable sitemap
├── sitemap.xml       # Sitemap for search engines
├── robots.txt        # Crawler rules, points to sitemap.xml
├── style.css         # Shared styles (light and dark mode)
└── aadhyapan.apk     # The Android app download
```

## Run locally

No installation needed. From the repo folder, start any static server:

```bash
python3 -m http.server 8000
```

Then open `http://localhost:8000`.

## Deploy

The site is served by GitHub Pages straight from the root of the default branch.

1. Go to **Settings > Pages**.
2. Set the source to **Deploy from a branch**, select the default branch and the `/ (root)` folder.
3. Save. The site goes live at `https://aadhyapan.github.io/`.

## Updating the app

1. Replace `aadhyapan.apk` in the repo root with the new build, keeping the same file name.
2. Commit and push. The download button picks it up automatically.

If you change the file name, update the link in `index.html` and the `downloadUrl` in its structured data.

## SEO

Each page includes a title, meta description, canonical URL, Open Graph and Twitter tags, and a favicon. The home page also carries JSON-LD structured data. When you add a page, remember to:

- add it to `sitemap.xml` and `sitemap.html`
- give it its own title, description, and canonical URL

After the first deploy, submit `https://aadhyapan.github.io/sitemap.xml` in Google Search Console and Bing Webmaster Tools.

## Contributing

Typos, accessibility fixes, and small improvements are welcome. Fork the repo, make your change, and open a pull request. For anything bigger, please open an issue first.

## License

See the [LICENSE](LICENSE) file. The Android app's source code lives in a separate repository and is licensed under GPL-3.0.

## Credits

Made by [**Raman Chapagain**](https://ramanchapagain.github.io/).
