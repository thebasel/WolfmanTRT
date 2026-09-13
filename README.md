# WolfmanTRT site

Minimal static site for **WolfmanTRT** — peer education on TRT literacy, training, recovery, and lifestyle. Dark theme, few files, no frameworks. Ready for GitHub Pages at domain root.

**Not medical advice.** Copy is education-only; no dosing, sourcing, or protocols-as-prescriptions.

## File tree

```
wolfmantrt-site/
├── index.html          # Home
├── 404.html            # Custom 404
├── README.md
├── css/
│   └── styles.css
├── blog/
│   └── index.html
└── start-here/
    └── index.html
```

(Mobile nav is CSS-only — no `js/` file.)

## Push to GitHub Pages

1. Create a new GitHub repository (e.g. `wolfmantrt.github.io` for user Pages, or any repo if you’ll use a custom domain / project Pages).
2. From this folder:

   ```bash
   cd /workspace/wolfmantrt-site
   git init
   git add .
   git commit -m "Initial WolfmanTRT GitHub Pages site"
   git branch -M main
   git remote add origin git@github.com:YOUR_USER/YOUR_REPO.git
   git push -u origin main
   ```

3. On GitHub: **Settings → Pages → Build and deployment**
   - Source: **Deploy from a branch**
   - Branch: **main** / **/ (root)**
   - Save

4. Wait for the Pages deploy; the site URL appears on the same Settings → Pages screen.

**DNS / custom domain (e.g. wolfmantrt.com)** is out of scope for this setup — configure A/CNAME and the custom domain field in Pages settings yourself when ready.

## Local preview

Any static server from the site root works, e.g.:

```bash
cd /workspace/wolfmantrt-site
python3 -m http.server 8080
```

Open `http://localhost:8080`. Paths are root-absolute (`/blog/`, `/css/...`) so they match GitHub Pages at domain root.
