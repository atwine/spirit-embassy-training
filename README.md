<div align="center">
  <img src="images/logo.png" alt="Spirit Embassy / GoodNews Church" height="80" />
  <br/><br/>

  # Spirit Embassy Training

  **A static study resource site for Spirit Embassy / GoodNews Church,**  
  hosted on GitHub Pages.

  [![GitHub Pages](https://img.shields.io/badge/Live%20Site-GitHub%20Pages-222222?style=flat-square&logo=github)](https://atwine.github.io/spirit-embassy-training/)
  [![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
  [![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/CSS)
  [![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
  [![Tally](https://img.shields.io/badge/Forms-Tally.so-FF6B6B?style=flat-square)](https://tally.so)
  [![License](https://img.shields.io/badge/License-All%20Rights%20Reserved-lightgrey?style=flat-square)]()

</div>

---

## Live Site

> **https://atwine.github.io/spirit-embassy-training/**

---

## Current Course

### The God-Kind Faith Accelerator Course
Study Guide for **Chapters 6 & 7** of *The God-Kind of Faith* by Prophet Uebert Angel (the Ra'ah).

| Chapter | Title | Presenter |
|---------|-------|-----------|
| Chapter 6 | The Realm of Faith vs. The Realm of Senses | Cardinal Moses |
| Chapter 7 | How Faith Grows — The God-Kind Faith Accelerator | The Seer |

---

## Tech Stack

| Layer | Technology |
|-------|------------|
| Hosting | GitHub Pages (static, zero backend) |
| Pages | Pure HTML5 / CSS3 / Vanilla JS |
| Fonts | Google Fonts — Inter, Lora |
| Forms | Tally.so (registration + quiz) |
| Design | Custom CSS — Modern Ministry Light theme |
| Version Control | Git / GitHub |

---

## Site Structure

```
spirit-embassy-training/
├── index.html          # Landing / registration page
├── study.html          # Study content — sidebar nav + full material
├── images/
│   └── logo.png        # Spirit Embassy logo
├── README.md
└── CHANGELOG.md
```

### Page Flow

```
index.html  ──[Register button]──▶  Tally registration form (tally.so/r/1AxJZ1)
                                           │
                              [On submit, Tally redirects to]
                                           │
                                           ▼
                              study.html?first_name=...&last_name=...
                                           │
                              [JS reads URL params, appends to quiz link]
                                           │
                                           ▼
                              Tally quiz form (tally.so/r/PdgBde)
                              (first_name + last_name pre-filled)
```

---

## Tally Form Configuration

### Registration Form — `tally.so/r/1AxJZ1`
- Collects: First Name, Last Name
- On submit: redirects to `https://atwine.github.io/spirit-embassy-training/study.html`
- URL parameters passed: `first_name`, `last_name`

### Quiz Form — `tally.so/r/PdgBde`
- Hidden fields: `first_name`, `last_name`
- Visible name fields have **Default answer** set to pull from those hidden fields
- Parameters are forwarded from `study.html` via JavaScript

> **Important:** After any changes to a Tally form, you must click **Publish** inside Tally for changes to take effect.

---

## Design

The site uses the **Modern Ministry Light** theme:
- White background with warm gray surfaces
- Inter (sans-serif) for headings and body
- Lora (serif) for pull quotes and scripture blocks
- Dark (`#0F0F0F`) and gold (`#B8860B`) as primary accent colours
- Sticky left sidebar on `study.html` with 34 section anchors
- Responsive: sidebar collapses to horizontal strip on mobile

---

## Local Development

No build step required. Open files directly in a browser:

```bash
# Clone the repo
git clone https://github.com/atwine/spirit-embassy-training.git

# Open in browser
start index.html
```

Or use VS Code Live Server for hot reload.

---

## Deployment

Every push to `main` automatically deploys via GitHub Pages.

```bash
git add .
git commit -m "your message"
git push origin main
```

Allow 1–2 minutes for GitHub Pages to update after a push.

---

## Content Credits

All study material is based on *The God-Kind of Faith* by **Prophet Uebert Angel (the Ra'ah)**.  
Taught at Spirit Embassy / GoodNews Church by **Cardinal Moses** (Chapter 6) and **the Seer** (Chapter 7).

[uebertangel.org](https://uebertangel.org)
