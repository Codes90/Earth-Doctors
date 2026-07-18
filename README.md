# Earth Doctors

**Fine Fermentation. Live Fire. Microbial Intelligence.**

Live site: **https://earth-doctors.com** (also https://codes90.github.io/Earth-Doctors/)

Want to change pictures, text, prices, or the contact email? See
**[CONTENT-GUIDE.md](CONTENT-GUIDE.md)** — no web-development knowledge needed.

## How it's hosted

Every push to the `main` branch automatically publishes `public/` to
**GitHub Pages** (free) via `.github/workflows/deploy-pages.yml`. There is
nothing to run or maintain.

## Going live (one-time)

Two halves: turn on GitHub Pages, then point the GoDaddy domain at it.

**A. Enable GitHub Pages** (the deploy workflow fails until this is done):

1. On github.com/Codes90/Earth-Doctors go to **Settings → Pages**.
2. Under **Build and deployment → Source**, choose **"GitHub Actions"**.
3. Go to the **Actions** tab and re-run the failed "Deploy to GitHub Pages"
   run (or push any commit). The site is now live at
   https://codes90.github.io/Earth-Doctors/

**B. Point the GoDaddy domain at GitHub:**

1. Sign in at godaddy.com → **My Products** → `earth-doctors.com` → **DNS**.
2. Delete any existing **A** records and turn off any **Forwarding** for the domain.
3. Add these four **A** records (Name: `@`, TTL: default):
   - `185.199.108.153`
   - `185.199.109.153`
   - `185.199.110.153`
   - `185.199.111.153`
4. Find the existing **CNAME** record named `www` (GoDaddy creates one by
   default) and **edit** its Value to `codes90.github.io` — or add it if
   missing. Leave the `_domainconnect` CNAME alone.
5. Wait for DNS to spread (usually minutes, up to an hour). You can check at
   https://dnschecker.org by looking up `earth-doctors.com` — it should
   show the 185.199.x.x addresses.
6. Back in the GitHub repo: **Settings → Pages** → **Custom domain** → type
   `earth-doctors.com` → **Save**. Wait for the green check.
7. Tick **Enforce HTTPS** (the checkbox appears once the certificate is
   issued, usually within the hour). Done — the site now answers at
   https://earth-doctors.com, and the github.io address redirects to it.

## Local preview

Open `public/index.html` directly in a browser, or run the optional server:

```bash
npm install
npm start
# Visit http://localhost:3000
```

## Alternative hosting (Railway)

The repo still contains `server.js`, so it can also deploy to
[railway.app](https://railway.app) (paid) as a Node.js app if you ever need
server-side features: New Project → Deploy from GitHub repo → add your custom
domain in Settings → Networking.

## Project structure

```
├── .github/workflows/deploy-pages.yml   # auto-publish to GitHub Pages
├── public/
│   ├── index.html    # the entire website (all pages, styles, scripts)
│   ├── 404.html      # redirects unknown URLs to the home page
│   └── images/       # ← drop your photos here (see README inside)
├── server.js          # optional local/Railway server
├── package.json
└── CONTENT-GUIDE.md   # how to edit pictures, text, contact info
```
