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

JSON export is the default persistence path. Adherence, threat-area and vendor-dependency evidence, CRI remediation checks, and vendor PQCMM mappings are kept in a JSON file named `pqc-register-backup-….json`.

- **Export JSON** and **Import JSON** in the header are the primary controls. Export downloads the current register. Import loads a file back into the page.
- A meaningful save downloads that file on its own. Adherence **Save** downloads immediately and prompts you to keep the file or import one. CRI checklist and PQCMM edits download immediately, then at most every few seconds while you keep editing, so you do not have to hunt for Export.
- This browser also keeps a working copy in `localStorage` so a refresh here can continue. That cache is not the record. Import the JSON file to restore the register in another browser, or after the working copy is cleared.
