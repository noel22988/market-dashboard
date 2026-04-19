# Market Dashboard

A full-featured stock tracking app with candlestick charts, AI analysis, screener, heatmap, portfolio tracker, news sentiment, and alerts.

## Deploy to Vercel via GitHub

### Step 1 — Push to GitHub
1. Go to github.com → New repository → name it `market-dashboard`
2. Upload all files in this folder (index.html, api/claude.js, vercel.json, README.md)
   - Click "uploading an existing file" → drag and drop all files
   - For the api/ folder: create it manually → New file → type `api/claude.js` → paste contents
3. Commit changes

### Step 2 — Deploy on Vercel
1. Go to vercel.com → Sign up / Log in with GitHub
2. Click "Add New Project"
3. Import your `market-dashboard` repository
4. Click Deploy — Vercel auto-detects the config

### Step 3 — Add your API key (critical)
1. In Vercel dashboard → your project → Settings → Environment Variables
2. Add: `ANTHROPIC_API_KEY` = your Anthropic API key
3. Redeploy: Deployments tab → click the 3 dots → Redeploy

Your app will be live at: https://market-dashboard-xxxx.vercel.app

## API Keys used
- **Anthropic (Claude)** — set as Vercel env var `ANTHROPIC_API_KEY` (never put in code)
- **NewsAPI** — currently hardcoded in index.html (free tier is fine, browser requests allowed)
- **Yahoo Finance** — no key needed, fetched via allorigins.win proxy

## Features
- Watchlist with AI BUY/HOLD/SELL signals
- Candlestick charts with Bollinger Bands, MA, S/R, RSI, MACD
- Stock screener scoring 32 US + SGX stocks
- Sector heat map
- Portfolio P&L tracker
- News with AI sentiment tagging
- Price alerts with browser notifications
