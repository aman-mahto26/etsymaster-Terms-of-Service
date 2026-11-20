# EtsyMaster Pro: Listing Scraper & SEO Auditor

> A Manifest V3 Chrome Extension for high-speed Etsy listing extraction, algorithmic competitor SEO diagnostics, multi-page automated crawling, media asset packaging, and AI prompt synthesis.

---

## 🌟 Key Features

- **Single Listing Scraper:** One-click extraction of product titles, multi-tier pricing, shop sales, listing age, favorites, and 13 competitor tags.
- **Algorithmic SEO Diagnostics:** Calculates Etsy SERP Score, Google SERP Score, 20-character tag compliance, keyword synergy, and stem waste.
- **High-Resolution Media Downloader:** Download listing images bundled in a single ZIP file or exported directly into a media folder.
- **Multi-Page Search Crawler:** Dynamic relative pagination starting from any search page (e.g. Page 5 with 2 pages crawls Pages 5 & 6) with randomized human jitter (1.5s–3.5s).
- **Master Excel Export:** Exports a 4-tab native `.xlsx` workbook (Master Data, SEO Analysis, Winning Tags Matrix, Shop Benchmarks).
- **AI Research Prompts:** Pre-synthesized prompts for ChatGPT/Claude and 1-click copy for top 13 competitor tags.
- **Google Sheets Live Analytics:** Serverless backend with automated user authorization, 19-column telemetry tracking, and a live aggregate dashboard.

---

## 🚀 Installation (Chrome Developer Mode)

1. Clone or download this repository.
2. Open Google Chrome and navigate to `chrome://extensions/`.
3. Enable **Developer mode** using the toggle in the top-right corner.
4. Click **Load unpacked** and select the repository directory.
5. Pin **EtsyMaster Pro** to your Chrome toolbar.

For a full interactive walkthrough, open `docs/user-guide.html` in your browser.

---

## 📁 Repository Structure

```
├── manifest.json              # Chrome Extension Manifest V3 configuration
├── assets/                    # Icons (16px, 32px, 48px, 128px)
├── background/
│   └── service-worker.js      # Background service worker & crawler loop
├── content/
│   ├── schema.js              # Data models and structures
│   ├── scraper-core.js        # DOM extraction engine
│   ├── seo-analyzer.js        # Algorithmic SEO evaluation logic
│   └── strategy-engine.js     # Tag recommendation & prompt generation
├── export/
│   └── excel-builder.js       # Native 4-tab Excel workbook generator
├── popup/
│   ├── popup.html             # Glassmorphic extension popup UI
│   ├── popup.css              # Styling & animations
│   └── popup.js               # Extension controller & OAuth handling
├── vendor/
│   ├── jszip.min.js           # Client-side ZIP packaging library
│   └── xlsx.full.min.js       # Client-side SheetJS Excel engine
├── backend/
│   └── google-apps-script.js  # Google Sheets Apps Script backend
├── docs/
│   └── user-guide.html        # Interactive user manual and visual guide
├── .gitignore                 # Standard Git ignore rules
└── README.md                  # Project overview and documentation
```

---

## 🔒 Security & Privacy

- Manifest V3 compliant with zero `eval()` or obfuscated code.
- Operates under strict host permissions limited to Etsy and Google Sheets backend endpoints.
- Google OAuth 2.0 (`chrome.identity`) gatekept strictly on file download/export actions.

---

## 📄 License

This project is licensed under the MIT License.
