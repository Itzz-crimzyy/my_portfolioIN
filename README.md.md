# Pratham Pachapur — Engineering & Robotics Portfolio

A modern, high-performance personal portfolio website built with semantic HTML5, Tailwind CSS, and vanilla JavaScript. Designed with a dark mechatronics/engineering aesthetic, blueprint grid accents, interactive project modals, and an embedded resume viewer.

---

## 🚀 Overview

This repository contains the source code for the personal portfolio of **Pratham Pachapur**, a Mechatronics, Robotics & Automation engineering student at NMIMS MPSTME, Mumbai. The site showcases hardware and software projects, team roles, certifications, skills, and direct contact options.

### Live Highlights
- **Single-File Architecture**: Self-contained HTML, CSS, and JS with zero complex build tooling required.
- **Embedded Resume System**: Integrated Base64 PDF generation that allows direct download and in-browser preview without external hosting dependencies.
- **Interactive Project Modals**: Deep-dive modals with thumbnail galleries, technical specs, learning outcomes, and documentation downloads.
- **Responsive & Accessible**: Mobile-first navigation, fluid layouts, and smooth scroll behaviors.

---

## 🛠️ Tech Stack

- **Markup & Semantics**: HTML5 (native `<dialog>` element for accessible modals)
- **Styling**: [Tailwind CSS](https://tailwindcss.com/) via CDN with custom theme extensions
- **Typography**: Google Fonts ([Space Grotesk](https://fonts.google.com/specimen/Space+Grotesk), [Inter](https://fonts.google.com/specimen/Inter), [JetBrains Mono](https://fonts.google.com/specimen/JetBrains+Mono))
- **Scripting**: Vanilla JavaScript (ES6+) with `IntersectionObserver` scroll animations

---

## ✨ Features

1. **Hero & Status Header**: Technical callout badge, dynamic headline, quick links, and blueprint-framed portrait.
2. **About & Key Metrics**: Summary overview with quick-reference statistic cards.
3. **Experience & Education Timeline**: Dual-column timeline displaying leadership positions, campus teams, and academic history.
4. **Interactive Project Catalog**:
   - Card grid with project status badges and tech tags.
   - Click-to-open modal dialog containing image switcher, overview, role breakdown, technical specifications, and links to schematics/code.
5. **Categorized Toolbox**: Multi-category skill tags (Robotics, Design/CAD, Programming, AI).
6. **Verified Credentials**: Google certifications list with credential IDs and skill tags.
7. **Resume Hub**: Action buttons for instant PDF download and external tab viewing alongside an embedded preview card.
8. **Contact Section**: One-click email builder and direct links to GitHub and LinkedIn.

---

## 📁 Suggested Directory Structure

While `index.html` operates as a standalone file, you can organize your assets in the following structure for full image and document support:

```text
portfolio/
├── index.html                   # Core website file
├── Pratham_Pachapur_Resume.pdf  # Fallback resume PDF (optional)
├── images/                      # Project media & portraits
│   ├── me.jpg                   # Profile photo
│   ├── obstacle-1.jpg
│   ├── obstacle-2.jpg
│   ├── soccer-1.jpg
│   ├── builder-1.jpg
│   └── swarm-sar-1.jpg
└── docs/                        # Project reports & schematics
    ├── obstacle-report.pdf
    ├── obstacle-circuit.pdf
    ├── soccer-bom.pdf
    ├── soccer-circuit.pdf
    └── builder-design-report.pdf
```

---

## ⚙️ Configuration & Customization

All personal details, projects, skills, and links are managed centrally in the configuration object `D` located in the `<script>` tag inside `index.html`:

```javascript
const D = {
  email: "your-email@example.com",
  collegeEmail: "your-college-email@domain.edu",
  linkedin: "https://www.linkedin.com/in/your-profile",
  github: "https://github.com/your-username",
  resume: "Pratham_Pachapur_Resume.pdf",
  photo: "images/me.jpg", // Path to your portrait
  title: 'I build machines that <span class="text-accent">sense, think</span> and move.',
  sub: "Your bio headline...",
  chips: ["Robotics", "IoT", "CAD & Product Design"],
  about: [ /* Paragraphs for About section */ ],
  stats: [ /* [Value, Label] pairs */ ],
  exp: [ /* Experience entries */ ],
  edu: [ /* Education history */ ],
  projects: [
    {
      id: "unique-slug",
      name: "Project Name",
      short: "Short preview description.",
      tags: ["Arduino", "C++"],
      status: "Completed",
      images: ["images/photo-1.jpg", "images/photo-2.jpg"],
      overview: "Detailed overview...",
      role: "Your contributions...",
      specs: [["Controller", "Arduino UNO"], ["Drive", "DC Motors"]],
      learned: ["Takeaway 1", "Takeaway 2"],
      docs: [["Report (PDF)", "docs/report.pdf"]]
    }
  ],
  skills: { /* Skill category -> items */ },
  certs: [ /* Certificate items */ ]
};
```

---

## 🏃 Running Locally

Since this project requires no compiler or dependencies, you can run it using any simple local server:

### Option 1: VS Code Live Server
1. Open the project folder in [Visual Studio Code](https://code.visualstudio.com/).
2. Install the **Live Server** extension.
3. Right-click `index.html` and select **"Open with Live Server"**.

### Option 2: Python HTTP Server
```bash
# Python 3.x
python -m http.server 8000
```
Open `http://localhost:8000` in your web browser.

### Option 3: Node.js `npx serve`
```bash
npx serve .
```

---

## 🌐 Deployment

### GitHub Pages
1. Push your files to a GitHub repository.
2. Navigate to **Settings** > **Pages**.
3. Under **Branch**, select `main` (or `master`) and folder `/ (root)`.
4. Click **Save**. Your site will be live at `https://<username>.github.io/<repo-name>/`.

### Vercel / Netlify
- Drag and drop your project folder or connect your GitHub repository; deployment happens automatically with zero configuration.

---

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).