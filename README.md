# CryptoEmbed – Privacy-Focused Crypto Portfolio Widget

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Version](https://img.shields.io/badge/version-1.0-red.svg)
![Status](https://img.shields.io/badge/status-stable-success.svg)

A **lightweight, serverless, and privacy-first crypto portfolio embed widget**.  
Designed for **personal websites, Linktree-style bios, blogs, Notion, and dashboards**.

Runs fully **client-side** using vanilla HTML & JavaScript.  
No backend. No tracking. No cookies.

👉 **Live Demo & Embed Generator**  
https://massatianagara.github.io/arah-crypto/

---

## ✨ Core Features

### 📊 Portfolio Value Tracking
- Displays **current portfolio value** in fiat
- Shows **value change (profit / loss)** since a selected period
- Calculates **price growth (%)** of the asset

### ⏱️ Flexible Time Periods
- Toggle between:
  - **3 Months**
  - **6 Months**
  - **1 Year**
- Optional **custom start date** (`btc_then_date`)
- Automatically picks the **most relevant base date**

### 💎 Multi-Asset Support
Powered by CoinGecko asset IDs:
- Bitcoin (BTC)
- Ethereum (ETH)
- Solana (SOL)
- BNB, XRP, DOGE, ADA, TRX
- Easily extendable to any CoinGecko-listed asset

### 💱 Multi-Currency Fiat Support
- IDR (Rp)
- USD ($)
- EUR (€)
- SGD (S$)
- MYR (RM)
- JPY (¥)
- Auto FX conversion via **Frankfurter API**

### 🌍 Multi-Language
- English (`en`)
- Indonesian (`id`)
- Auto-formatted numbers & currency styles

### 🎨 Widget Themes
Choose per embed:
- **Dark** (default)
- **Light**
- **Glass (glassmorphism)**
- **Flat (minimal)**

### 📱 Responsive & Embed-Safe
- Optimized for:
  - Mobile
  - Desktop
  - iFrame containers
- Perfect for:
  - Notion
  - WordPress
  - GitHub Pages
  - Personal bio pages

### 🛡️ Privacy-First by Design
- 100% **client-side**
- No analytics
- No cookies
- No user data storage
- All portfolio data lives only in the URL

---

## 🚀 Quick Start

### Option A — Online Generator (Recommended)

1. Open the generator page
2. Select:
   - Asset
   - Currency
   - Language
   - Theme
3. Enter:
   - Start balance
   - Optional start date
   - Current balance
4. Click **Update Preview**
5. Copy the generated `<iframe>` code
6. Paste it anywhere

---

### Option B — Self Hosting

1. Clone or download this repository
2. Upload these files to your hosting:
   - `index.html` (generator UI)
   - `embed.html` (widget)
3. Open `index.html` locally or online

Works perfectly on:
- GitHub Pages
- Netlify
- Vercel
- Any static hosting

---

## 🔧 Embed URL Parameters

| Parameter | Example | Description |
|--------|--------|-------------|
| `coin` | `bitcoin` | CoinGecko asset ID |
| `fiat` | `IDR` | Fiat currency |
| `lang` | `en` / `id` | Interface language |
| `btc_then` | `1.5` | Initial coin balance |
| `btc_then_date` | `2023-01-01` | Optional start date |
| `btc_now` | `2.5` | Current coin balance |
| `period` | `3m` | Default period |
| `theme` | `dark` | Widget theme |

---

## 🧩 Example Embed Code

```html
<iframe src="https://massatianagara.github.io/arah-crypto/embed.html?coin=bitcoin&fiat=IDR&lang=en&btc_then=1.5&btc_then_date=2022-01-18&btc_now=2.5&period=1y&theme=dark"
style="width:100%;max-width:560px;height:360px;border:0;border-radius:24px;overflow:hidden;background:transparent;" 
loading="lazy" 
title="Crypto Portfolio Widget">
</iframe>
```

---

## 🎨 Customization

### Add New Coins
Edit `index.html`:

```html
<select id="coin">
```
Add:
```html
<option value="polygon">Polygon (MATIC)</option>
```

### Modify Theme Colors
Edit CSS variables in `embed.html`:

```css
:root {
  --up: #00c076;
  --down: #ff5b5b;
}
```

---

## ⚠️ API Notes & Limits

Uses **free public APIs**:

- **CoinGecko API**
  - Rate limited
  - Intended for personal & moderate traffic

- **Frankfurter API**
  - Fiat exchange rates

If data fails to load:
- Wait a moment
- Refresh the page

---

## 📄 License

MIT License  
Free for personal & commercial use.

---

© 2026 — CryptoEmbed by **Satia Studio**  
Not financial advice.
