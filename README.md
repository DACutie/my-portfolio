# Lord Natan Galicia — Portfolio Site

A single-page portfolio built with plain HTML/CSS/JS (no framework, no build step).

## Structure
```
portfolio/
├── index.html          # everything — markup, CSS, and JS in one file
├── assets/
│   └── Lord_Natan_Galicia_Resume.docx   # linked from the "Download Résumé" button
└── README.md
```

## Running it locally in VS Code
No build tools or dependencies needed — it's plain HTML/CSS/JS.

1. Open the `portfolio` folder in VS Code.
2. Easiest: install the **Live Server** extension (Ritwick Dey), then right-click `index.html` → **Open with Live Server**. This gives you hot-reload on save.
   - Alternative without any extension: just double-click `index.html` to open it directly in your browser. Everything works except the file:// protocol can be picky in some browsers about local resource loading — Live Server (or any local dev server) avoids that.
3. Alternative via terminal, from inside the `portfolio` folder:
   ```
   python3 -m http.server 5500
   ```
   then open http://localhost:5500 in your browser.

## Notes
- The portrait photo is embedded directly in `index.html` as a base64 data URI, so the page is fully self-contained — you can move or rename the file and it'll still render the photo correctly.
- The "Download Résumé" button links to `assets/Lord_Natan_Galicia_Resume.docx` by relative path, so keep that file in place (or update the `href` in index.html if you rename/move it).
- Dark mode preference is saved in the browser's localStorage — it'll persist across visits on the same browser.
- The chat widget is a keyword-matching FAQ assistant built from resume content — no backend, no API key, works the moment you open the file. See the `FAQ` array near the bottom of index.html (inside the `<script>` tag) if you want to add or edit answers.

## To deploy publicly
Any static host works since there's no backend:
- GitHub Pages
- Netlify (drag-and-drop the `portfolio` folder)
- Vercel
- Cloudflare Pages
