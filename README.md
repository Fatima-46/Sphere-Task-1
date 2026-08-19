<p align="center">
  <img src="assets/banner.svg" alt="Fatima Saleem — Cyber Security Student &amp; Web Developer" width="100%">
</p>

<h3 align="center">Personal portfolio — multi-page, Bootstrap 5, dark &amp; light mode</h3>

<p align="center">
  <a href="#live-demo"><strong>View Live Demo »</strong></a>
</p>

<p align="center">
  <img alt="HTML5" src="https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white">
  <img alt="CSS3" src="https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white">
  <img alt="JavaScript" src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black">
  <img alt="Bootstrap 5" src="https://img.shields.io/badge/Bootstrap-5.3.3-7952B3?style=flat-square&logo=bootstrap&logoColor=white">
  <img alt="No build step" src="https://img.shields.io/badge/Build%20step-none-6B8257?style=flat-square">
  <img alt="Made in Lahore" src="https://img.shields.io/badge/Made%20in-Lahore%2C%20Pakistan-3B4A32?style=flat-square">
</p>

<p align="center">
  <sub>Cyber Security undergrad (UMT Lahore) with a parallel habit of shipping full web products end to end.</sub>
</p>

---

## Table of contents

- [About](#about)
- [Live demo](#live-demo)
- [Preview](#preview)
- [Features](#features)
- [Tech stack](#tech-stack)
- [Project structure](#project-structure)
- [Pages](#pages)
- [Color palette](#color-palette)
- [Getting started](#getting-started)
- [Customizing the theme](#customizing-the-theme)
- [Projects featured on the site](#projects-featured-on-the-site)
- [Certifications](#certifications)
- [Connect](#connect)
- [License](#license)

---

## About

This repo is the source for my personal portfolio — a fast, static, dependency-light site built to showcase my cyber security coursework, web development projects, and certifications. It's built with plain **HTML, CSS, and a touch of vanilla JavaScript** on top of **Bootstrap 5**, with no framework, bundler, or backend — clone it and open it, no `npm install` required.

I'm a **BS Cyber Security** student at **UMT Lahore** (GPA 3.78/4.0), leaning toward offensive security, and currently working as a **Web Development Intern at Sphere Consulting** (Lahore, Pakistan). This site is where those two tracks meet.

## Live demo

> Replace this with your deployed link once it's live (GitHub Pages / Vercel / Render):

**[https://your-live-url-here](https://your-live-url-here)**

## Preview

<p align="center">
  <img src="assets/screenshot-home-light.png" alt="Home page — light mode" width="47%">
  <img src="assets/screenshot-home-dark.png" alt="Home page — dark mode" width="47%">
</p>
<p align="center">
  <img src="assets/screenshot-projects.png" alt="Projects page" width="47%">
  <img src="assets/screenshot-skills.png" alt="Skills page" width="47%">
</p>

<p align="center"><sub>Drop your own screenshots into <code>assets/</code> with these filenames (or update the paths above) — light mode, dark mode, and a couple of section pages make for a strong preview grid.</sub></p>

## Features

- **Multi-page architecture** — each section (Home, About, Interests, Skills, Projects, Certifications, Contact) is its own page, linked by a shared nav bar
- **Dark / light theme toggle** — persists across visits via `localStorage`, falls back to the visitor's OS preference on first load, and swaps with no flash-of-wrong-theme
- **Glassmorphism nav bar** — frosted, blurred, sticky navigation that adapts to both themes
- **Prev / Next page pager** — a bottom-of-page traversal control that walks through every section in order, looping from Contact back to Home
- **Animated hero entrance** — staggered fade/rise-in for the headline, subtext, and buttons on load
- **Animated skill bars** — progress bars that fill from 0 to their target percentage via CSS keyframes, driven by a single reusable `--fill` custom property per bar
- **Fully responsive** — Bootstrap 5's grid collapses gracefully down to mobile, with the nav folding into a hamburger menu
- **Accessible by default** — semantic landmarks, `aria-label`s on icon-only buttons, visible focus states, and `prefers-reduced-motion` support that disables all animation for users who ask for it

## Tech stack

| Layer | Tool |
|---|---|
| Markup | HTML5 |
| Layout & components | [Bootstrap 5.3.3](https://getbootstrap.com/) |
| Styling | Custom CSS (`style.css`) — CSS custom properties for theming, `@keyframes` for motion |
| Interactivity | Vanilla JavaScript (theme toggle only — no framework, no dependencies) |
| Typography | [Fraunces](https://fonts.google.com/specimen/Fraunces) (display) + [Manrope](https://fonts.google.com/specimen/Manrope) (body), via Google Fonts |
| Hosting | Static — deployable anywhere (GitHub Pages, Vercel, Netlify, Render) |

## Project structure

```
.
├── index.html              # Home / Hero
├── about.html               # About
├── interests.html           # Primary interests
├── skills.html               # Skills + progress bars
├── projects.html            # Project cards
├── certifications.html      # Credentials list
├── contact.html             # Contact links
├── style.css                 # Shared stylesheet — palette, layout, animation, theming
├── profile-pic.jpg          # Hero photo
├── Fatima Saleem CV -2.pdf  # Downloadable CV (linked from the hero button)
├── assets/
│   └── banner.svg            # This README's banner
└── README.md
```

Every page links to the **same** `style.css`, so editing one file re-styles the whole site.

## Pages

| Page | File | What's there |
|---|---|---|
| Home | `index.html` | Hero intro, photo, CV download, headline |
| About | `about.html` | Focus areas — offensive security leaning, web dev learning path |
| Interests | `interests.html` | Web Development & Offensive Security, as two focus cards |
| Skills | `skills.html` | Animated skill bars (Python & C++, HTML & CSS) + tool tags |
| Projects | `projects.html` | 5 shipped projects with live demo + GitHub links |
| Certifications | `certifications.html` | Completed certificates and courses |
| Contact | `contact.html` | Email, GitHub, LinkedIn, current internship |

Navigation between them works two ways: the **top nav bar** (jump to any page) and the **bottom pager** (walk sequentially, Home → ... → Contact → back to Home).

## Color palette

The whole site runs on CSS custom properties, so the palette lives in one place (`:root` in `style.css`) and flips entirely for dark mode via `:root[data-theme="dark"]`.

| Token | Light | Dark |
|---|---|---|
| `--bg` | ![#F5F7EF](https://placehold.co/14x14/F5F7EF/F5F7EF.png) `#F5F7EF` | ![#12160D](https://placehold.co/14x14/12160D/12160D.png) `#12160D` |
| `--violet` (headings) | ![#3B4A32](https://placehold.co/14x14/3B4A32/3B4A32.png) `#3B4A32` | ![#D9E4C7](https://placehold.co/14x14/D9E4C7/D9E4C7.png) `#D9E4C7` |
| `--teal` (accent) | ![#6B8257](https://placehold.co/14x14/6B8257/6B8257.png) `#6B8257` | ![#9BC17F](https://placehold.co/14x14/9BC17F/9BC17F.png) `#9BC17F` |
| `--amber` | ![#C0912F](https://placehold.co/14x14/C0912F/C0912F.png) `#C0912F` | ![#E0B563](https://placehold.co/14x14/E0B563/E0B563.png) `#E0B563` |

## Getting started

No build tools, no dependencies to install.

```bash
git clone https://github.com/Fatima-46/<this-repo>.git
cd <this-repo>
```

Then either:
- **Just open it** — double-click `index.html`, or
- **Serve it locally** (recommended, avoids any file:// quirks):

```bash
# Option A — Python
python3 -m http.server 8000

# Option B — Node
npx serve .
```

Then visit `http://localhost:8000`.

## Customizing the theme

Everything visual runs off CSS variables defined once in `style.css`:

```css
:root{
  --bg: #F5F7EF;
  --teal: #6B8257;
  --violet: #3B4A32;
  /* ... */
}

:root[data-theme="dark"]{
  --bg: #12160D;
  --teal: #9BC17F;
  --violet: #D9E4C7;
  /* ... */
}
```

Change a value here and it updates across every page, every component (buttons, cards, nav, badges) — nothing needs to be touched per-page.

## Projects featured on the site

| Project | Stack | Status |
|---|---|---|
| [rule-based-chat-assistant](https://github.com/Fatima-46/rule-based-chat-assistant) | Python, Streamlit, REST API | Deployed |
| [password-strength-breach-checker](https://github.com/Fatima-46/password-strength-breach-checker) | Flask, HIBP API, k-anonymity | In progress |
| [image-steganography-web](https://github.com/Fatima-46/image-steganography-web) | React, Flask, SQLite | Deployed |
| [nutrifind](https://github.com/Fatima-46/nutrifind) | Python, Streamlit, SQLite | Deployed |
| [brew-compass](https://github.com/Fatima-46/brew-compass) | HTML, CSS, JavaScript | Deployed |

## Certifications

- Introduction to Cybersecurity Awareness
- Coursera Python
- Agile Project Management
- Getting Started with Cybersecurity — IBM
- Data Science & Analytics

## Connect

<p align="left">
  <a href="mailto:fatimasocietien@gmail.com"><img alt="Email" src="https://img.shields.io/badge/Email-fatimasocietien%40gmail.com-3B4A32?style=flat-square&logo=gmail&logoColor=white"></a>
  <a href="https://github.com/Fatima-46"><img alt="GitHub" src="https://img.shields.io/badge/GitHub-Fatima--46-3B4A32?style=flat-square&logo=github&logoColor=white"></a>
  <a href="https://www.linkedin.com/in/fatima-saleem-533661392/"><img alt="LinkedIn" src="https://img.shields.io/badge/LinkedIn-Fatima%20Saleem-3B4A32?style=flat-square&logo=linkedin&logoColor=white"></a>
</p>

## License

This project is licensed under the [MIT License](LICENSE) — feel free to fork it, learn from it, or use it as a starting point for your own portfolio. If you do, a star ⭐ or a credit line is always appreciated.

---

<p align="center"><sub>Built with Bootstrap 5, a lot of CSS custom properties, and zero frameworks. Lahore, Pakistan.</sub></p>
