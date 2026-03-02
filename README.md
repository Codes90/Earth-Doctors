# Earth Doctors

**Fine Fermentation. Live Fire. Microbial Intelligence.**

## Deploy to Railway

### Option A — GitHub (Recommended)

1. Push this folder to a GitHub repository
2. Go to [railway.app](https://railway.app) and sign in
3. Click **"New Project"** → **"Deploy from GitHub repo"**
4. Select your repository
5. Railway auto-detects Node.js and deploys automatically
6. Click **"Generate Domain"** in Settings to get your public URL

### Option B — Railway CLI

```bash
# Install Railway CLI
npm install -g @railway/cli

# Login
railway login

# Initialize project
railway init

# Deploy
railway up
```

### Custom Domain

1. In your Railway project, go to **Settings** → **Networking**
2. Click **"Generate Domain"** for a free `*.up.railway.app` URL
3. Or click **"Custom Domain"** and add your own (e.g., earthdoctorsknow.com)
4. Update your domain's DNS records as Railway instructs

## Project Structure

```
earth-doctors-railway/
├── public/
│   └── index.html    # Full 7-page website
├── server.js          # Express static server
├── package.json       # Dependencies & start script
├── .gitignore
└── README.md
```

## Local Development

```bash
npm install
npm start
# Visit http://localhost:3000
```
