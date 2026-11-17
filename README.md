# 🏎️ BMW Digital Experience — Spider Hackathon Showcase

[![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Live%20Demo-brightgreen?logo=github)](https://nachiket1311.github.io/Spider-hackathon/)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/CSS)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![Firebase](https://img.shields.io/badge/Firebase-Hosting-FFCA28?logo=firebase&logoColor=black)](https://firebase.google.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

An immersive, high-performance web portal built during the **Spider Hackathon**. This project delivers a sleek digital showroom and interactive experience celebrating BMW automotive engineering, bespoke tuning powerhouses (**G-POWER** & **ALPINA**), the **BMW M Driving Experience**, and modern model lineups.

🌐 **Live GitHub Pages URL**: [https://nachiket1311.github.io/Spider-hackathon/](https://nachiket1311.github.io/Spider-hackathon/)

---

## 🌟 Key Features & Pages

### 1. 🏎️ Hero & Brand Showcase (`index.html`)
- **Cinematic Ambient Video Hero**: Fullscreen background video player (`bmw.mp4`) with typography overlay *"Experience the Ultimate Driving Machine"*.
- **Interactive Navigation Bar**: Translucent glass-effect header with fluid hover animations and glowing accent underlines.
- **Tuning House Showcases**:
  - **G-POWER Manufactur**: Highlights bespoke German engine craftsmanship, power modifications, and vehicle uniqueness.
  - **ALPINA**: Custom configurator overview detailing exterior colors, bespoke upholstery, and high-performance equipment.
- **Brand Heritage & Contact Footer**: Comprehensive company details, limited edition history, and inquiries.

### 2. 🚗 Interactive Vehicle Showroom (`models.html`)
- **Animated Speedometer Preloader**: Pure CSS speedometer animation with a dynamic sweeping tachometer needle (`pegIt` keyframe rotation), dual spinning gauge rings, and loading indicators that dismiss upon asset load.
- **Card-Based Model Grid**:
  - **BMW X3** — Luxury Sports Activity Vehicle (SAV)
  - **The All-New BMW M2 Coupé** — Compact high-performance sports coupé
  - **The Fully Electric BMW i4** — Next-generation emission-free Gran Coupé
  - **The New BMW M4 Competition Coupé with M xDrive** — Motorsport DNA with intelligent all-wheel drive
  - **The New BMW Z4 M40i** — Pure open-top roadster performance
  - **The New BMW X5** — Flagship luxury executive SAV
- **Interactive Micro-Interactions**: Smooth `1.8x` scale zoom effects on hover with pricing information and *"Book Now"* call-to-action triggers.

### 3. ⚡ Bespoke Limited Edition Portal (`Limited_edition.html`)
- **High-Octane Video Backdrop**: Showcasing the BMW M3 CS (`THE M3 CS (2023)..mp4`).
- **Exclusive Tuning Profiles**: Deep dive into the heritage, limited-run production numbers, and aerodynamic upgrades of Alpina and G-Power custom builds.

### 4. 🏁 BMW M Driving Experience (`driving experiene.html`)
- **Track & Training Dynamics**: Exploring track day training, drift academy, and performance mastery.
- **Global Experience Network**: World map integration showcasing international BMW Driving Experience centers and certified instructors.
- **Multimedia Highlights**: Curated media galleries showing high-speed circuit driving and electric M performance.

### 5. 🛡️ Custom Error Route (`404.html`)
- Branded, styled 404 error page ensuring a smooth fallback and quick return routes back to the main portal.

---

## 🛠️ Technology Stack

| Layer | Technologies |
|---|---|
| **Markup & Semantics** | HTML5 (Semantic elements, `<video>`, `<source>`, `<nav>`, `<section>`) |
| **Styling & Effects** | CSS3 (Keyframe animations, Flexbox, Backdrop blur, Custom scrollbars, Responsive media queries) |
| **Client Scripting** | Vanilla JavaScript (Dynamic video playback controls, window load event listeners, loader dismissals) |
| **CI/CD & Hosting** | **GitHub Pages** (via GitHub Actions workflow) & **Firebase Hosting** |
| **Media Assets** | High-definition MP4 video streams, WebP compressed imagery, PNG transparent vehicle renders |

---

## 📂 Project Structure

```plaintext
Spider-hackathon/
├── .github/
│   └── workflows/
│       ├── deploy-pages.yml               # GitHub Actions workflow for automated GitHub Pages deployment
│       ├── firebase-hosting-merge.yml     # Firebase Hosting workflow for main branch
│       └── firebase-hosting-pull-request.yml
├── public/                                # Public web root served by GitHub Pages & Firebase
│   ├── index.html                         # Main landing page & brand experience
│   ├── models.html                        # Model showroom with animated speedometer loader
│   ├── Limited_edition.html               # Limited edition Alpina & G-Power showcase
│   ├── driving experiene.html             # BMW M Driving Experience page
│   ├── driving-experience.html            # URL-friendly alias redirect
│   ├── Home.html                          # Fallback redirect to index.html
│   ├── 404.html                           # Custom 404 error page
│   ├── styles.css                         # Supporting stylesheets
│   ├── .nojekyll                          # Disables Jekyll processing on GitHub Pages
│   ├── bmw.mp4                            # Ambient brand video asset
│   ├── THE M3 CS (2023)..mp4              # Limited edition M3 CS video asset
│   ├── logo.png                           # BMW badge
│   ├── Alpina_logo.svg.png                # Alpina badge
│   ├── map.png                            # World branch map
│   ├── BMW_Group_Branches_Map.jpg         # Global branch network diagram
│   ├── img/                               # High-resolution vehicle model renders
│   │   ├── BMW M2/
│   │   ├── BMW X3/
│   │   ├── THE ALL-NEW BMW M2 COUPÉ/
│   │   ├── THE FULLY ELECTRIC BMW i4/
│   │   ├── THE NEW BMW M4 COMPETITION COUPÉ WITH M xDRIVE/
│   │   └── THE NEW BMW Z4 M40i/
│   └── *.jpg / *.webp / *.jpeg            # Engine, interior, and showroom photography
├── index.html                             # Root redirect for branch-based GitHub Pages deployment
├── firebase.json                          # Firebase Hosting configuration
├── .firebaserc                            # Firebase project mapping
├── .gitattributes                         # Git line-ending normalization
├── .gitignore                             # Ignored dependencies and cache files
├── .nojekyll                              # Root Jekyll bypass for GitHub Pages
└── README.md                              # Project documentation
```

---

## 🚀 Getting Started & Local Development

No heavy build steps or npm installations are required. You can serve the static site locally with any static web server:

### Option 1: Python Simple HTTP Server (Recommended)
```bash
# Clone the repository
git clone https://github.com/Nachiket1311/Spider-hackathon.git
cd Spider-hackathon

# Serve the public directory
python3 -m http.server 8000 --directory public
```
Open your browser and navigate to `http://localhost:8000`.

### Option 2: VS Code Live Server
1. Open the `Spider-hackathon` folder in VS Code.
2. Install the **Live Server** extension.
3. Right-click `public/index.html` and select **"Open with Live Server"**.

### Option 3: Node.js `npx serve`
```bash
npx serve public
```

### Option 4: Firebase CLI
```bash
firebase emulators:start
# or
firebase serve
```

---

## 🌐 Deploying to GitHub Pages

This repository is pre-configured with a GitHub Actions workflow (`.github/workflows/deploy-pages.yml`) for instant zero-configuration GitHub Pages hosting.

### Enabling GitHub Pages on GitHub:
1. Navigate to your repository on GitHub: `https://github.com/Nachiket1311/Spider-hackathon`
2. Click **Settings** (top navigation).
3. In the left sidebar, click **Pages** (under the *Code and automation* section).
4. Under **Build and deployment**:
   - **Source**: Select **`GitHub Actions`**.
5. Push any commit to the `main` branch (or go to **Actions** tab -> **Deploy to GitHub Pages** -> click **Run workflow**).
6. Your live site will be deployed and available at:
   👉 **`https://nachiket1311.github.io/Spider-hackathon/`**

> **Note**: An `index.html` redirect is also provided in the repository root so that if you choose **Source: Deploy from a branch** (`main` branch, `/ (root)` folder), the page will still load seamlessly.

---

## 👥 Authors & Credits

Created for the **Spider Hackathon** by:

- **Nachiket Palekar** — [@Nachiket1311](https://github.com/Nachiket1311)
- **Ashok Thaniyath** — [@ashokthaniyath](https://github.com/ashokthaniyath)

---

## 📄 License & Disclaimer

This project was developed for educational and hackathon competition purposes. All BMW trademarks, logos, vehicle names, and related visual assets are property of **Bayerische Motoren Werke AG (BMW)**, **ALPINA Burkard Bovensiepen GmbH + Co. KG**, and **G-POWER GmbH**.
