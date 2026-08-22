[![Fatima Saleem banner](https://capsule-render.vercel.app/api?type=soft&color=0:0A0E27,50:12315C,100:0FA3A3&height=220&section=header&text=Fatima%20Saleem&fontSize=52&fontColor=E8FFF9&animation=twinkling&fontAlignY=35&desc=Cyber%20Security%20Student%20%E2%80%A2%20Offensive%20Track%20%E2%80%A2%20Full-Stack%20Builder&descAlignY=58&descSize=17&descColor=6FE7DD)](https://fatima-46.github.io/Sphere-Task-1/)

<p align="center">
  <img src="https://img.shields.io/badge/HTML5-0A0E27?style=for-the-badge&logo=html5&logoColor=6FE7DD" alt="HTML5" />
  <img src="https://img.shields.io/badge/CSS3-12315C?style=for-the-badge&logo=css3&logoColor=6FE7DD" alt="CSS3" />
  <img src="https://img.shields.io/badge/JavaScript-0A0E27?style=for-the-badge&logo=javascript&logoColor=F4D35E" alt="JavaScript" />
  <img src="https://img.shields.io/badge/Google%20Fonts-12315C?style=for-the-badge&logo=googlefonts&logoColor=6FE7DD" alt="Google Fonts" />
</p>

<p align="center">
  <img src="https://img.shields.io/badge/No%20Framework-E8FFF9?style=flat-square&labelColor=0A0E27" alt="No Framework" />
  <img src="https://img.shields.io/badge/Status-Active-E8FFF9?style=flat-square&labelColor=12315C" alt="Status Active" />
  <img src="https://img.shields.io/badge/License-MIT-E8FFF9?style=flat-square&labelColor=0FA3A3" alt="MIT License" />
</p>

### 🛡️ A single-page portfolio, built like a system I'd want to defend

Dark, glass-and-glow interface for a Cyber Security student who also ships full web
products — hero intro, about, skill gauges, a project showcase, and a contact panel,
all in one scrolling page with smooth anchor navigation.

<!-- Replace the # below with your live deployment URL once hosted -->
[![View live site](https://capsule-render.vercel.app/api?type=rect&color=0:12315C,100:0A0E27&height=70&section=header&text=VIEW%20LIVE%20SITE&fontSize=24&fontColor=6FE7DD&animation=fadeIn&fontAlignY=55&width=380)](https://fatima-46.github.io/Sphere-Task-1/)
![Source](https://img.shields.io/badge/📦%20Source-Sphere--Task--1-0A0E27?style=for-the-badge&labelColor=0FA3A3)

## 📌 Table of Contents

|                                                    |                                                          |
| -------------------------------------------------- | -------------------------------------------------------- |
| 📁 [Project Structure](#-project-structure)         | 🧩 [Page Sections](#-page-sections)                       |
| ▶️ [Running It Locally](#️-running-it-locally)       | 🎨 [Design System](#-design-system)                       |
| 🗂️ [Projects Featured](#️-projects-featured)         | 🚀 [Deploying It](#-deploying-it)                         |
| 🛠️ [Editing Content](#️-editing-your-own-content)    | 🧭 [Roadmap](#-roadmap--ideas)                             |

---

- **Frontend only**: plain HTML + CSS (no framework, no build step, no backend)
- **Fonts**: [Fraunces](https://fonts.google.com/specimen/Fraunces) for headings, [Manrope](https://fonts.google.com/specimen/Manrope) for body text, loaded from Google Fonts

## 📁 Project Structure

```
Sphere-Task-1/
├── index.html   → all markup: nav, hero, about, skills, projects, contact
└── style.css    → all styling: layout, glow effects, gauges, chips, cards
```

Everything lives in two files on purpose — this was built as a self-contained
task/portfolio piece, so there's no build tooling to install and nothing to
compile before you can open it.

## ▶️ Running It Locally

No dependencies, no package manager. Just serve the folder:

```bash
git clone https://github.com/Fatima-46/Sphere-Task-1.git
cd Sphere-Task-1
python3 -m http.server 8080
```

Then open `http://localhost:8080` in your browser.

> [!TIP]
> You *can* double-click `index.html` directly and it'll mostly work, since
> there's no `fetch()` call to a backend here — but serving it over `http://`
> avoids any font-preconnect or relative-path quirks some browsers apply to
> `file://` pages.

## 🧩 Page Sections

| Section | What's there |
|---|---|
| **Nav** | Sticky header with logo mark and anchor links to each section |
| **Hero** | Name, tagline, and two CTAs (`View projects`, `Contact me`), with soft ambient glow shapes behind the text |
| **About** | Short bio split across offensive-security focus and the parallel full-stack learning habit, plus quick-glance chips (`Red Team leaning`, `Full-stack learning`, `UMT Lahore`) |
| **Skills** | Two circular gauge cards (Python & C++, HTML & CSS) driven by a CSS custom property (`--pct`), plus a row of tool tags (Git, SQL/SQLite, REST APIs, Render, Vercel, Linux) |
| **Projects** | Card grid pulling in real shipped projects with live status badges and outbound links |
| **Contact** | Current role blurb plus Email / GitHub / LinkedIn links |

### How the skill gauges work

Each gauge card sets a `--pct` custom property inline:

```html
<div class="gauge" style="--pct:85;">
  <span class="gauge-value">85%</span>
</div>
```

`style.css` reads that variable in a `conic-gradient` (or similar) to fill the
ring to the right percentage — so adding a new skill is just copying the card
and changing one number and one label, no JS required.

## 🗂️ Projects Featured

| Project | Stack | Status |
|---|---|---|
| [rule-based-chat-assistant](https://rule-based-chat-assistant-vugiaxwlw65fryjymeq3tr.streamlit.app/) | Python, Streamlit, REST API | 🟢 Deployed |
| password-strength-breach-checker | Next.js, React, entropy checks | 🟡 In progress |
| [image-steganography-web](https://fatimasaleem.pythonanywhere.com/) | React, Flask, SQLite | 🟢 Deployed |
| [nutrifind](https://nutrifind-cae5w7swywmxdymrxoxviw.streamlit.app/) | Python, Streamlit, SQLite | 🟢 Deployed |
| [brew-compass](https://yourcoffeematch.netlify.app/) | HTML, CSS, JavaScript | 🟢 Deployed |

## 🛠️ Editing Your Own Content

Everything is hand-authored in `index.html`, no CMS or data file — so updates
are direct edits:

- **Bio / focus area**: `<section id="about">`
- **Skill gauges**: `<section id="skills">` — duplicate a `.gauge-card` block, set `--pct` and the label
- **Projects**: `<section id="projects">` — duplicate a `.project-card` `<article>`, update the status badge class (`status-live` / `status-progress`), title, description, stack tags, and link
- **Contact links**: `<section id="contact">` — update the `mailto:`, GitHub, and LinkedIn `href`s

## 🎨 Design System

The interface leans into a dark, "security console" feel — deep charcoal-navy
backgrounds with soft cyan/teal glow accents behind the hero and contact
panels, rather than flat cards:

| Role | Feel |
|---|---|
| Page background | Deep charcoal / near-black navy |
| Glow accents (`.glow-a`, `.glow-b`, `.glow-c`) | Soft cyan-teal ambient light, blurred behind key sections |
| Headings (`Fraunces`) | Serif display type for contrast against the technical subject matter |
| Body text (`Manrope`) | Clean geometric sans for readability |
| Status badges | Green for `Deployed`, amber/yellow for `In progress` |

> If your actual `style.css` palette differs from the banner colors above,
> swap the hex codes in the badge/banner URLs at the top of this README to
> match — they're just query parameters.

## 🚀 Deploying It

Static two-file sites like this deploy anywhere that serves plain HTML:

| Host | How |
|---|---|
| **GitHub Pages** | Settings → Pages → deploy from `main` branch, root folder |
| **Netlify** | Drag-and-drop the folder, or connect the repo — no build command needed |
| **Vercel** | Import the repo, framework preset "Other", no build step |

Once it's live, drop the URL into the banner link and the `View live site`
badge near the top of this README.

## 🧭 Roadmap / Ideas

- [ ] Split into multiple pages (About / Skills / Projects / Contact) with a shared nav, if the single page starts feeling long
- [ ] Add a dark/light theme toggle
- [ ] Pull project cards from a small JSON file instead of hard-coded HTML, so new projects are a data entry instead of a markup edit
- [ ] Add a downloadable resume/CV link in the contact section

## 📄 License

Released under the [MIT License](./LICENSE).

---

`#CyberSecurity` `#Portfolio` `#HTML` `#CSS` `#WebDev` `#UMTLahore`

[![footer banner](https://capsule-render.vercel.app/api?type=soft&color=0:0A0E27,50:12315C,100:0FA3A3&height=100&section=footer)](#fatima-saleem)
