# 🛡️ PNB CyberShield — Cybersecurity 

> **Live Demo:** [https://c-navy-sigma.vercel.app](https://c-navy-sigma.vercel.app)

A full-stack cybersecurity dashboard prototype built for the **Punjab National Bank Cybersecurity Hackathon 2026**, featuring Post-Quantum Cryptography (PQC) readiness assessment, asset discovery, certificate generation with QR verification, and AI-powered threat analytics.

---

## 📸 Preview

| Login Page | Dashboard | Certificate |
|---|---|---|
| 3D animated background with globe, matrix rain, stars | KPI cards, asset inventory, crypto overview | Canvas-rendered cert with QR code |

---

## ✨ Features

### 🔐 Authentication
- Email/password login with validation and shake animation
- **Google Sign-In** (OAuth 2.0 via Google Identity Services)
- User avatar + dropdown menu in header
- Sign out with session reset

### 🏠 Dashboard
- KPI cards — Total Assets, Public Web Apps, APIs, Servers, Expiring Certs, High Risk Assets
- Asset Type Distribution donut chart
- Asset Risk Distribution bar chart
- Certificate Expiry Timeline
- IP Version Breakdown
- Asset Inventory table with scan status, cert validity, key length
- Nameserver Records resolver
- Crypto & Security Overview table
- Live activity bar

### 🛸 Asset Inventory
- Full asset table with risk badges, cert status, key length
- Add Asset modal
- Scan All — animated per-asset scanning with TLS/key/risk results
- Apply scan results back to table

### 🏛 Asset Discovery
- **Domain/URL input** — enter any domain or URL to discover assets
- **Time period selector** — 24h / 7d / 30d / 90d / Custom date range
- Animated scan progress (DNS → subdomains → ports → TLS → risk)
- Dynamic network graph — root domain at center, discovered assets orbiting
  - Node border color = risk level (green/amber/red/critical)
  - Animated data packets flowing along edges
- Discovered assets table with IP, type, open ports, TLS version, risk, first-seen date

### 🧬 CBOM (Cryptographic Bill of Materials)
- Key Length Distribution bar chart
- Cipher Usage breakdown with progress bars
- Top Certificate Authorities
- Encryption Protocols donut chart
- Per-application CA table

### 🚶 PQC Posture Dashboard
- Elite-PQC Ready / Standard / Legacy / Critical breakdown
- Assets by Classification Grade
- Application Status donut
- Risk Overview grid
- PQC Support table per asset
- Improvement Recommendations

### ⭐ Cyber Rating
- Consolidated score: **755/1000 — Elite-PQC**
- Tier table (Legacy < 400, Standard 400–700, Elite > 700)

### 📊 Reporting
- Executive Summary
- Scheduled Reports
- On-Demand Reports

### 🏅 Certificate Generation
- Multi-step wizard (Form → Progress → Result)
- Canvas-rendered certificate with:
  - Shield logo, gold borders, corner ornaments, diagonal watermark
  - Domain, org, cert type, key size, issued/expiry dates, cert ID, status
  - **Verified seal** (bottom-left)
  - **QR code** (bottom-right) — auto-generated, links to verify page
- Side QR panel with "Save QR" button
- Download PNG + PEM
- Share / Copy PEM

### 🔍 Certificate Verification (`verify.html`)
- Standalone page — opens instantly when QR is scanned
- Shows: Cert ID, Domain, Org, Type, Key Size, Issued Date, Expiry Date, Status
- Live scan timestamp
- No app loading — pure HTML + URL params

### 🌐 Global Search
- Search assets, domains, IPs, certificates from header
- Fuzzy match with highlighted results
- Click to navigate to relevant page

### 🎨 3D Login Background
- Deep space nebula with drifting color blobs
- 200 twinkling stars
- Matrix rain (crypto characters: `01`, katakana, `∑∆Ω`)
- 3D rotating globe with 4 orbital rings of colored nodes
- Expanding pulse rings from center
- Floating shield particles drifting upward
- Hex grid overlay
- Vignette effect

---

## 🗂 Project Structure

```
├── index.html      # Main app (single-page application)
├── verify.html     # Certificate verification page (opened by QR scan)
└── README.md       # This file
```

---

## 🚀 Getting Started

### Run Locally
Just open `index.html` in any modern browser — no build step, no dependencies.

```bash
# Or serve with any static server
npx serve .
# → http://localhost:3000
```

### Deploy to Vercel
```bash
npm i -g vercel
vercel deploy --yes --prod
```

---

## 🔑 Login Credentials

| Email | Password |
|-------|----------|
| `hackathon_user@pnb.bank.in` | `password` |
| `admin@pnb.bank.in` | `admin123` |
| `admin` | `admin` |

Or use **Continue with Google** (any Gmail account).

---

## 🔧 Google OAuth Setup

1. Go to [console.cloud.google.com](https://console.cloud.google.com)
2. APIs & Services → Credentials → Create OAuth 2.0 Client ID
3. Application type: **Web application**
4. Authorised JavaScript origins: `https://your-domain.vercel.app`
5. Replace `data-client_id` in `index.html` with your Client ID

Current Client ID is configured for `https://c-navy-sigma.vercel.app`.

---

## 🛠 Tech Stack

| Layer | Technology |
|-------|-----------|
| Frontend | Vanilla HTML5, CSS3, JavaScript (ES6+) |
| Charts | Canvas 2D API (custom drawn) |
| Fonts | Google Fonts — Orbitron, Rajdhani, Share Tech Mono |
| QR Code | Google Chart API + qrserver.com fallback |
| Auth | Google Identity Services (GSI) |
| Deployment | Vercel |

---

## 📱 Certificate QR Flow

```
Generate Certificate
       ↓
QR encodes: https://c-navy-sigma.vercel.app/verify.html
            ?verify=PNB-XXXXX
            &domain=portal.pnb.bank.in
            &org=Punjab+National+Bank
            &type=TLS%2FSSL
            &bits=4096
            &issued=29+Mar+2026
            &expires=29+Mar+2027
            &serial=3E:25:F7
       ↓
User scans QR → verify.html opens instantly
       ↓
Shows full certificate details + live scan timestamp
```

---

## 🏆 Hackathon Context

- **Event:** PNB Cybersecurity 
- **Theme:** Post-Quantum Cryptography Readiness
- **Focus Areas:** Asset Discovery, CBOM, PQC Posture, Cyber Rating
- **Collaboration:** Punjab National Bank · IIT Kanpur · Department of Financial Services · IBA

---

## 📄 License

MIT — free to use, modify and distribute.
