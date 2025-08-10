# BRS DApp (BTD / BTB) — GitHub Pages

A single-file DApp for BRS system: connect wallet (MetaMask), mint/burn BTD, burn BTB, rebase both tokens, and set prices/annual rate via Config.
This repo is **ready for GitHub Pages**.

## Quick Start (GitHub UI)
1. Create a **new public repo** on GitHub, e.g. `brs-dapp`.
2. Download the ZIP from ChatGPT and unzip it.
3. Drag & drop all files into the GitHub repo (Upload files) and commit.
4. Open **Settings → Pages**:
   - Source: **Deploy from a branch**
   - Branch: **main** (or `master`) / folder: **/** (root)
   - Save.
5. Wait 1–2 minutes. Your site will be live at `https://<your-username>.github.io/<repo>/`.

## Quick Start (Git CLI)
```bash
git init
git add .
git commit -m "Publish BRS DApp to GitHub Pages"
git branch -M main
git remote add origin https://github.com/<your-username>/<repo>.git
git push -u origin main
# Then enable GitHub Pages in Settings → Pages → Source: Deploy from a branch (main / root)
```

## Notes
- If you open the HTML directly via `file://`, most wallet extensions won't inject `window.ethereum`.
  Use https://<your-username>.github.io/<repo>/ (served over HTTPS) to ensure MetaMask injection.
- Default contract addresses are embedded in `index.html`. Update them in-page if needed.
- For local debug without GitHub: `python -m http.server 5500` and open http://localhost:5500/ .
