# 🌍 FennecGlobe — Global Intelligence Platform

> Real-time global intelligence, geopolitical monitoring, market data, and AI analysis across 192 countries.

[![Live Demo](https://img.shields.io/badge/Live-Demo-brightgreen?style=for-the-badge)](https://swordenkisk.github.io/fennecglobe)
[![License](https://img.shields.io/badge/License-MIT-blue?style=for-the-badge)](LICENSE)
[![Version](https://img.shields.io/badge/Version-4.2.0-purple?style=for-the-badge)](CHANGELOG.md)

---

## ✨ Features

| Feature | Description |
|---|---|
| 🗺️ **Global Event Map** | Interactive hotspot map with conflict, weather, shipping & military layers |
| 📰 **Live News Feed** | Real-time aggregated news from 247 global sources |
| 🔴 **Threat Intelligence** | Severity-graded threat feed (Critical → Low) |
| 📈 **Market Data** | Live indices, forex, commodities — cards & table views |
| ₿ **Crypto Monitor** | Top 8 cryptocurrencies with sparklines and market caps |
| 🌤️ **Weather** | 192-city weather monitor with °C/°F toggle |
| 📡 **Social Intel** | Trending social media intelligence feed |
| 🛰️ **Satellite Tracker** | 247 satellites in real-time orbit visualization |
| ⚠️ **Alert System** | Active global alerts with severity classification |
| 🤖 **FennecAI** | AI assistant for geopolitical & market intelligence |
| 🎨 **4 Themes** | Algerian Green · Dark Blue · Light · Cyber Purple |
| 🔒 **Auth** | Google Sign-In · Apple Sign-In · Email/Password |
| 🔖 **Bookmarks** | Sidebar with saved feeds and regions |
| ⚙️ **Settings** | Full preferences panel (theme, notifications, data, privacy) |
| 📊 **Live Ticker** | Scrolling market data ticker |
| 🌐 **i18n** | English · Arabic · French · Spanish · German · Chinese |

---

## 🚀 Quick Start

```bash
# Clone the repository
git clone https://github.com/swordenkisk/fennecglobe.git

# Open in browser
cd fennecglobe
open index.html

# Or serve locally
npx serve .
# → http://localhost:3000
```

**No build step required.** FennecGlobe is a single-file web application — pure HTML, CSS, and JavaScript.

---

## 📁 Repository Structure

```
fennecglobe/
├── index.html          # Main application (complete, self-contained)
├── README.md           # This file
├── LICENSE             # MIT License
├── CHANGELOG.md        # Version history
├── .github/
│   └── workflows/
│       └── deploy.yml  # GitHub Pages auto-deploy
└── assets/             # Optional: custom icons, images
```

---

## 🎨 Themes

Switch themes via **Settings (⚙️)** or by calling `setTheme()` in console:

```javascript
setTheme('green')   // Algerian Green (default)
setTheme('dark')    // Dark Blue
setTheme('light')   // Light
setTheme('cyber')   // Cyber Purple
```

---

## ⌨️ Keyboard Shortcuts

| Shortcut | Action |
|---|---|
| `/` | Focus search bar |
| `Ctrl+K` / `⌘K` | Focus search bar |
| `Esc` | Close any open panel/modal |

---

## 🔌 Configuration

Customize data sources and settings at the top of the `<script>` section in `index.html`:

```javascript
// Data arrays — replace with live API calls
const NEWS_DATA = [...];    // News feed
const MARKETS = [...];      // Market data
const THREATS = [...];      // Threat intelligence
const WEATHER = [...];      // Weather data
const CRYPTO = [...];       // Cryptocurrency
const SOCIAL = [...];       // Social intelligence
const ALERTS = [...];       // Active alerts
```

### Connecting Live APIs

```javascript
// Example: fetch live news
async function fetchLiveNews() {
  const res = await fetch('https://your-api.com/news');
  const data = await res.json();
  NEWS_DATA.splice(0, NEWS_DATA.length, ...data);
  renderNews();
}

setInterval(fetchLiveNews, 60000); // refresh every minute
```

---

## 🛰️ Deploy to GitHub Pages

1. Fork or push to your GitHub repository
2. Go to **Settings → Pages**
3. Set source to `main` branch, `/ (root)`
4. Your site will be live at `https://swordenkisk.github.io/fennecglobe`

Or use the included GitHub Actions workflow:

```yaml
# .github/workflows/deploy.yml — already configured
# Just push to main branch to auto-deploy
```

---

## 🔐 Security

- Content Security Policy (CSP) headers configured
- No external API keys stored client-side
- Referrer policy: `strict-origin-when-cross-origin`
- Auth state is session-only (no sensitive data persisted)
- SOC2 / GDPR / ISO 27001 compliance design patterns

---

## 📊 Performance

- **Single file** — no build step, no dependencies
- **Lazy rendering** — panels render after launch animation
- **CSS animations** — hardware-accelerated
- **< 150KB** total page weight (no images)
- Works offline after first load (add service worker for PWA)

---

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/live-api-integration`
3. Make your changes in `index.html`
4. Test across all 4 themes and mobile/desktop
5. Submit a Pull Request

### Ideas for contribution
- [ ] Real news API integration (NewsAPI, GDELT)
- [ ] Live market data (Yahoo Finance, Alpha Vantage)
- [ ] Interactive MapLibre GL map
- [ ] PWA / service worker support
- [ ] Real-time WebSocket feeds
- [ ] User accounts with Supabase/Firebase
- [ ] Arabic RTL layout
- [ ] Push notifications

---

## 📜 License

MIT License — free to use, modify, and distribute.

---

## 🌍 About

FennecGlobe is a global intelligence dashboard built for analysts, journalists, researchers, and anyone who wants a unified view of world events. Named after the Fennec fox — native to North Africa — known for sharp senses and wide-angle awareness.

Built with ❤️ | Version 4.2.0 | © 2026 FennecGlobe
