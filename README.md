# 🎉 Surprise For My Friend  

![GitHub license](https://img.shields.io/github/license/imaakarsh/SurpriseForMyFrnd) ![GitHub stars](https://img.shields.io/github/stars/imaakarsh/SurpriseForMyFrnd) ![GitHub forks](https://img.shields.io/github/forks/imaakarsh/SurpriseForMyFrnd) ![GitHub last commit](https://img.shields.io/github/last-commit/imaakarsh/SurpriseForMyFrnd)  

**A tiny, pure‑HTML/CSS web page that delivers a personalized surprise to a friend.** Open the page in any modern browser and watch the magic happen!  

---  

## Table of Contents  

- [Overview](#overview)  
- [Features](#features)  
- [Tech Stack](#tech-stack)  
- [Architecture & Directory Layout](#architecture--directory-layout)  
- [Getting Started](#getting-started)  
  - [Prerequisites](#prerequisites)  
  - [Installation](#installation)  
  - [Running the Project](#running-the-project)  
- [Usage](#usage)  
- [Development](#development)  
- [Contributing](#contributing)  
- [Roadmap](#roadmap)  
- [Troubleshooting & FAQ](#troubleshooting--faq)  
- [License & Credits](#license--credits)  

---  

## Overview  

**Surprise For My Friend** is a lightweight, zero‑dependency web page that displays a custom surprise message (image, animation, and text) when opened. It is ideal for:

- Sending a quick, heartfelt digital surprise without the overhead of a backend.  
- Demonstrating basic front‑end techniques (CSS animations, responsive layout).  
- Learning how to package a static web project for easy sharing (GitHub Pages, email attachment, etc.).  

The project is currently at **v1.0.0** and works in all modern browsers (Chrome, Edge, Firefox, Safari).  

---  

## Features  

| Feature | Description | Status |
|---------|-------------|--------|
| 🎨 **Responsive Design** | Layout adapts gracefully from mobile to desktop. | ✅ Stable |
| ✨ **CSS Animations** | Fade‑in, slide‑up, and subtle hover effects. | ✅ Stable |
| 📸 **Embedded Image** | Displays `q1.png` (the surprise image) with a decorative border. | ✅ Stable |
| 🖱️ **Interactive Button** | Click to reveal a hidden message with a smooth transition. | ✅ Stable |
| 📱 **Touch Friendly** | All interactions work with mouse clicks and touch taps. | ✅ Stable |
| 🌐 **Zero Dependencies** | Pure HTML + CSS – no JavaScript, no external libraries. | ✅ Stable |

---  

## Tech Stack  

| Layer | Technology | Reason |
|-------|------------|--------|
| Markup | **HTML5** | Semantic structure, easy to host anywhere. |
| Styling | **CSS3** (Flexbox, Grid, Transitions) | Enables responsive layout and animations without JS. |
| Assets | **PNG** image (`q1.png`) | High‑quality surprise picture. |
| Hosting | Any static file server (GitHub Pages, Netlify, local `file://`) | No backend required. |

---  

## Architecture & Directory Layout  

```
SurpriseForMyFrnd/
├── index.html      # Main entry point – contains markup and inline meta tags
├── style.css       # All visual styling, animations, and responsive rules
└── q1.png          # The surprise image displayed on the page
```

*`index.html`* references `style.css` via a `<link>` tag and loads `q1.png` as a background/inline image. No additional assets or scripts are required.  

---  

## Getting Started  

### Prerequisites  

| Requirement | Minimum Version |
|-------------|-----------------|
| Web browser | Any modern browser (Chrome ≥ 80, Firefox ≥ 78, Edge ≥ 85, Safari ≥ 13) |
| Git (optional) | 2.20+ for cloning the repo |
| Node.js (optional) | Not required – only needed if you want to run a local dev server (e.g., `live-server`) |

### Installation  

1. **Clone the repository** (or download the ZIP)  

   ```bash
   git clone https://github.com/imaakarsh/SurpriseForMyFrnd.git
   cd SurpriseForMyFrnd
   ```

2. **(Optional) Install a static dev server** – helpful for live‑reload while editing  

   ```bash
   npm install -g live-server   # one‑time global install
   ```

### Running the Project  

- **Quick view** – just double‑click `index.html` and open it in your default browser.  

- **Local server (recommended for development)**  

  ```bash
  live-server
  ```

  This will launch `http://127.0.0.1:8080` (or similar) and automatically reload on file changes.  

---  

## Usage  

1. Open `index.html` in a browser.  
2. The page loads with a welcoming heading and a **“Reveal Surprise”** button.  
3. Click (or tap) the button – the hidden image (`q1.png`) fades in, accompanied by a short congratulatory message.  

### Example Screenshot  

![Surprise page preview](q1.png)  

*(The screenshot above shows the final revealed state.)*  

---  

## Development  

If you wish to customize the look or add new features:

1. **Edit `style.css`** – experiment with colors, fonts, or additional animations.  
2. **Edit `index.html`** – change the text, replace the image, or add extra sections.  
3. **Live reload** – run `live-server` (or any static server) to see changes instantly.  

### Code Style  

- **HTML** – Use semantic tags (`<header>`, `<main>`, `<section>`, `<footer>`).  
- **CSS** – Follow BEM‑like naming (`.surprise__button`, `.surprise__image`).  
- Keep indentation to **2 spaces** for consistency.  

---  

## Contributing  

Contributions are welcome! Follow these steps:

1. **Fork** the repository.  
2. **Create a feature branch**  

   ```bash
   git checkout -b feature/awesome-animation
   ```

3. **Make your changes** and ensure the page still works in a modern browser.  
4. **Commit** with a clear message  

   ```bash
   git commit -m "Add bounce animation to the surprise button"
   ```

5. **Push** to your fork and open a **Pull Request** against `main`.  

### Pull Request Checklist  

- [ ] Code follows the existing style (2‑space indentation, BEM naming).  
- [ ] All changes are reflected in the README (if you added a new feature).  
- [ ] The page renders correctly when opened directly (`file://`).  

---  

## Roadmap  

| Milestone | Planned Enhancements |
|-----------|----------------------|
| **v1.1** | Add optional background music (HTML5 `<audio>`). |
| **v1.2** | Provide a small configuration JSON to swap messages & images without code changes. |
| **v2.0** | Turn the project into a reusable NPM package that generates a custom surprise page from a CLI. |

---  

## Troubleshooting & FAQ  

| Problem | Solution |
|---------|----------|
| **Page looks unstyled** | Ensure `style.css` is in the same folder as `index.html` and the `<link rel="stylesheet">` path is correct. |
| **Image does not appear** | Verify that `q1.png` exists and is not corrupted. Check the console for 404 errors. |
| **Button click does nothing** | The button uses a CSS `:checked` trick; make sure you are not opening the file in a very old browser (IE ≤ 11). |
| **I want to host on GitHub Pages** | Push the repo to GitHub, enable Pages from the repository settings (source: `main` branch, root folder). The site will be available at `https://<username>.github.io/SurpriseForMyFrnd/`. |

---  

## License & Credits  

**License:** MIT License – see the [LICENSE](LICENSE) file for details.  

**Author:** *Karsh* – [GitHub profile](https://github.com/imaakarsh)  

**Acknowledgments**  

- The CSS animation technique is inspired by the **MDN Web Docs** examples.  
- Image `q1.png` is a personal photo (all rights reserved).  

---  

*Happy surprising!*  