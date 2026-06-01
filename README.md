# TMA UW-WLU — Landing Page

## 🚀 Deploy on Netlify via GitHub

### Step 1 — Push to GitHub
```bash
git init
git add .
git commit -m "Initial commit — TMA landing page"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/tma-waterloo.git
git push -u origin main
```

### Step 2 — Connect to Netlify
1. Go to [app.netlify.com](https://app.netlify.com) → **Add new site → Import an existing project**
2. Choose **GitHub** and select your repo
3. Build settings (leave all blank — auto-detected from `netlify.toml`):
   - Build command: *(empty)*
   - Publish directory: `.`
4. Click **Deploy site**

### Step 3 — Add custom domain (thaqalaynma.ca)
1. In Netlify: **Site Settings → Domain management → Add custom domain**
2. Type `thaqalaynma.ca` and confirm
3. At your domain registrar, add these DNS records:
   - `A` record: `@` → `75.2.60.5`
   - `CNAME` record: `www` → `your-site-name.netlify.app`
4. Netlify will auto-provision a free SSL certificate within minutes

---

## 📁 File Structure
```
tma-waterloo/
├── index.html       # Main landing page
├── style.css        # All styles
├── main.js          # Interactions & animations
├── netlify.toml     # Netlify config
├── .gitignore       # Git ignore rules
├── public/
│   └── logo.png     # TMA logo
└── README.md        # This file
```

## ✏️ Updating Content
- **Events**: Edit the `.event-card` blocks in `index.html`
- **Social links**: Update `href` attributes in the Connect section
- **Term label**: Change "Winter 2026 Term" in the hero badge
- Any push to `main` branch auto-redeploys on Netlify
