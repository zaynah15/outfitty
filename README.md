# 👗 Outfitty

> Your personal wardrobe intelligence system — log your clothes, generate outfit combinations.

A private wardrobe app for up to **50 users** with login, a full clothing taxonomy, and a rule-based outfit generator with style buckets.

---

## ✨ Features

- **🔐 Login system** — up to 50 private accounts, no backend needed
- **👚 Full wardrobe** — add items with category, subtype, color, material, pattern, fit, season, occasions
- **✨ Outfit generator** — smart rule-based engine using color harmony, fabric compatibility, silhouette balance
- **🎨 11 style buckets** — Office, Party, Casual, Coffee Date, Date Night, Picnic, Streetwear, Minimalist, Feminine, Edgy, Desi/Ethnic
- **📊 Outfit scoring** — each outfit gets a compatibility score (0–100%)
- **💡 Style reasoning** — explains why each outfit works

---

## 🚀 Deploy to GitHub Pages (Free Hosting)

### Step 1: Create a GitHub repo

1. Go to [github.com](https://github.com) → **New repository**
2. Name it `outfitty`
3. Make it **Public** (required for free GitHub Pages)
4. Don't add any files yet → click **Create repository**

### Step 2: Push this code

```bash
# In the outfitty folder:
git init
git add .
git commit -m "Initial Outfitty build"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/outfitty.git
git push -u origin main
```

### Step 3: Enable GitHub Pages

1. Go to your repo → **Settings** → **Pages**
2. Under **Source**, select **GitHub Actions**
3. The workflow will run automatically on every push

### Step 4: Your app is live!

It'll be at: `https://YOUR_USERNAME.github.io/outfitty/`

Share this URL with your friends. Anyone can sign up (up to 50 users).

---

## 🏗️ Local Development

```bash
npm install
npm run dev
```

Opens at `http://localhost:5173/outfitty/`

---

## 🧠 How the Outfit Engine Works

### Color Harmony
- Neutrals (white, black, beige, grey) pair with **everything** → score 1.0
- Same color family → 0.82
- Warm + cool → 0.5 (contrast)
- Metallics → 0.85 (widely compatible)

### Fabric Compatibility
- Leather + Cotton / Satin / Denim → great pairing
- Satin + Velvet / Lace → elegant combination
- Denim + Cotton / Linen → casual harmony

### Pattern Rules
- Solid + anything → 1.0 (always works)
- Two bold prints (floral + animal) → 0.25 (clash)
- Subtle + solid → excellent

### Silhouette Balance
- Oversized top → Fitted / Bodycon bottom
- Cropped top → Flowy or A-Line bottom
- Structured top → Relaxed bottom

### Scoring Formula
Each outfit gets scored across all compatible pairs, averaged into a 0–100% score.

---

## 🗂️ Project Structure

```
outfitty/
├── src/
│   ├── App.jsx              ← All UI components
│   ├── main.jsx             ← Entry point
│   ├── data/
│   │   └── taxonomy.js      ← Clothing categories, colors, fabrics
│   ├── engine/
│   │   └── fashionRules.js  ← Compatibility logic & outfit generator
│   └── hooks/
│       ├── useAuth.jsx      ← Login/signup system
│       └── useWardrobe.js   ← Wardrobe CRUD
├── .github/
│   └── workflows/
│       └── deploy.yml       ← Auto-deploy to GitHub Pages
├── vite.config.js
├── package.json
└── index.html
```

---

## 🔮 Future Upgrades

- [ ] **Claude AI integration** — send wardrobe data to Claude API for smarter suggestions and conversational styling advice
- [ ] **Custom garment drawing** — canvas-based tool to sketch new subtypes
- [ ] **Outfit saving** — save favourite outfit combinations
- [ ] **Supabase backend** — move from localStorage to a real database for shared wardrobe features
- [ ] **"What to wear today"** — weather + calendar-aware outfit suggestions
- [ ] **Style feed** — see what outfits your friends are generating

---

## 👥 User Limits

This app supports up to **50 users** stored in browser localStorage. All data is stored on each user's own device — there's no shared server.

To share across devices, you'd upgrade to Supabase (free tier available).

---

Made with 💛 for Outfitty crew
