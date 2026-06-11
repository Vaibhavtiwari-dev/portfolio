<div align="center">

# Vaibhav Tiwari — Portfolio

**Editorial-style personal portfolio with 3D interactions, glassmorphic surfaces, and gyroscope-aware mobile tilt.**

[![Live Site](https://img.shields.io/badge/Live-vaibhav--portfolio-000?style=for-the-badge&logo=firebase&logoColor=FFCA28)](https://vaibhav-portfolio-930c6.web.app)
[![Status](https://img.shields.io/badge/Status-Active-34d058?style=for-the-badge)]()
[![Zero Build](https://img.shields.io/badge/Build_Step-None-blue?style=for-the-badge)]()

[**View Live →**](https://vaibhav-portfolio-930c6.web.app)

</div>

---

## About

A single-page portfolio built from scratch with zero frameworks and zero build tooling. The site pairs editorial typography (Playfair Display, DM Sans, DM Mono) with hardware-inspired UI — metallic tactile buttons, 3D perspective cards, etched circuit-board overlays, and a scrolling timeline with winding SVG ribbon connectors.

On mobile, the portfolio detects device orientation and applies real-time gyroscope-driven 3D tilt to cards and the tech stack carousel, creating a physically responsive experience without any library.

## Key Features

| Feature | Description |
|---|---|
| **3D Perspective Cards** | CSS `perspective` + `transform-style: preserve-3d` with mouse-tracking tilt on desktop |
| **Mobile Gyroscope Tilt** | `DeviceOrientationEvent` with LERP smoothing applies physical tilt to all 3D elements |
| **Glassmorphic Project Cards** | `backdrop-filter: blur()` with etched SVG circuit-board overlays on dark section |
| **Tactile Metallic Buttons** | Multi-layer `box-shadow` + inset highlights simulating pressed/raised hardware buttons |
| **Editorial Typography** | Three-font system — serif headlines, sans body, monospace labels and code |
| **Contact Modal** | Formspree-powered form with AJAX submission, success state, and error fallback |
| **Scroll Reveal Animations** | Intersection Observer–driven entrance animations for every section |
| **Print-Ready Resume** | Separate `resume.html` with `@media print` styles and PDF export |
| **SEO & Structured Data** | Open Graph, Twitter Cards, JSON-LD `Person` schema, canonical URL, sitemap |
| **Accessibility** | Skip-to-content link, `aria-*` attributes, `inert` background on drawer/modal, `:focus-visible` outlines |

## Tech Stack

```
Frontend    HTML5 · CSS3 (Custom Properties) · Vanilla JavaScript
Typography  Playfair Display · DM Sans · DM Mono (Google Fonts)
Hosting     Firebase Hosting (CDN, redirect rules, security headers)
Forms       Formspree (AJAX POST)
SEO         JSON-LD · Open Graph · Twitter Cards · sitemap.xml · robots.txt
```

## Project Structure

```
Vaibhav-Portfolio/
├── index.html          Main portfolio — editorial single-page layout (~2,700 lines)
├── resume.html         Print-optimised resume with PDF export
├── resume.css          Resume-specific styles
├── 404.html            Custom 404 page (editorial theme)
│
├── profile.jpg         Profile photo
├── og-image.png        Open Graph share image (1200×630)
├── favicon.png         Compressed favicon (64×64)
├── favicon.svg         SVG favicon
│
├── robots.txt          Crawler directives
├── sitemap.xml         Sitemap for search engines
├── firebase.json       Hosting config — redirects, cache headers, security headers
└── .firebaserc         Firebase project reference
```

## Design Decisions

- **No framework, no build step.** The entire site is a single HTML file with inline `<style>` and `<script>` blocks. This keeps deployment trivial (static hosting), eliminates JS bundle overhead, and ensures the page loads in a single round-trip.

- **Inline styles over external CSS (for `index.html`).** Avoids a render-blocking stylesheet request. The resume page uses an external `resume.css` because it has a distinct visual identity and benefits from cache separation.

- **3D transforms as the primary design language.** Every major surface — the hero stats card, project cards, tech stack carousel, and timeline boxes — uses CSS `perspective` and `rotateX/Y` to create depth without WebGL or canvas.

- **Gyroscope as progressive enhancement.** Mobile 3D tilt is opt-in on iOS (permission badge) and auto-detected on Android. If the sensor is unavailable, cards render flat — no functionality is lost.

- **Security headers in hosting config.** `X-Content-Type-Options: nosniff`, `X-Frame-Options: DENY`, `Referrer-Policy: strict-origin-when-cross-origin`, and aggressive asset caching are set at the Firebase Hosting layer.

## Running Locally

```bash
git clone https://github.com/Vaibhavtiwari-dev/portfolio.git
cd portfolio
npx serve .
```

No install step. No build. Open `http://localhost:3000`.

> **Note:** The contact form submits to Formspree and will work locally without any backend configuration.

## Deployment

The site is deployed to [Firebase Hosting](https://firebase.google.com/docs/hosting). To deploy your own changes:

```bash
npm install -g firebase-tools    # one-time
firebase login
firebase deploy --only hosting
```

Hosting configuration lives in [`firebase.json`](firebase.json) — redirects, cache headers, and security headers are all defined there.

## Performance

- **Zero JavaScript frameworks** — no React, no Vue, no Alpine. Total JS is ~180 lines of vanilla code (mobile menu, contact modal, scroll reveal, 3D tilt).
- **No external CSS frameworks** — all styles are hand-written custom properties with `clamp()` for fluid responsive sizing.
- **Aggressive caching** — images and CSS are cached for 7 days (`max-age=604800`); HTML is `no-cache` for instant updates.

## Contact

<div align="center">

[![Portfolio](https://img.shields.io/badge/Portfolio-vaibhav--portfolio-000?style=flat-square&logo=firebase&logoColor=FFCA28)](https://vaibhav-portfolio-930c6.web.app)
[![GitHub](https://img.shields.io/badge/GitHub-Vaibhavtiwari--dev-000?style=flat-square&logo=github)](https://github.com/Vaibhavtiwari-dev)
[![X (Twitter)](https://img.shields.io/badge/X-@AsterismVaibhav-000?style=flat-square&logo=x&logoColor=white)](https://x.com/AsterismVaibhav)
[![Email](https://img.shields.io/badge/Email-vaibhav09012007-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:vaibhav09012007@gmail.com)

</div>

---

<div align="center">
  <sub>Designed and built by Vaibhav Tiwari · 2025</sub>
</div>
