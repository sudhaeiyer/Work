# PQC Register Explorer

Static single-page app for a post-quantum cryptography transition-risk and remediation register. Browse threat areas, use-case threat models, CRI Profile adherence, and the risk heatmap.

Author: Sudha Iyer, Chief Officer — Cryptography & PKI, Citi.

## How to open

There is no build step. The whole app is `index.html`.

- Open `index.html` directly in a browser.
- Or serve this folder with any static file server, then open the URL it prints. For example:

```bash
python3 -m http.server 8080
```

Then visit `http://localhost:8080/`.

## Saved state

Register edits stay in this browser through `localStorage`. That includes adherence status and CRI tracking.

Use **Backup JSON** in the header to download a JSON export of that state. Use **Import JSON** to load a backup into the current browser. After local saves, the app may also offer an automatic backup download.
