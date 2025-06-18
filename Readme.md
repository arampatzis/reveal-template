
# Reveal.js Presentation Template

This repository provides a minimal and clean setup for creating Reveal.js presentations using:

- Markdown (`slides.md`)
- LaTeX math (via MathJax)
- Live preview in the browser
- Custom themes and vertical slides

No need for Keynote — this works on any platform using free, open-source tools.

---

## Getting Started

### 1. Clone the repository

```bash
git clone git@github.com:arampatzis/reveal-template.git
cd reveal-template
```

Make sure you have Git and Node.js installed. Use SSH to avoid authentication issues.

---

### 2. Install Node.js and npm

Follow the official instructions based on your operating system:

- **Windows & macOS**: Download from [https://nodejs.org](https://nodejs.org)
- **Linux (Debian/Ubuntu)**:
  ```bash
  sudo apt update
  sudo apt install nodejs npm
  ```
- **Linux (Arch/Manjaro)**:
  ```bash
  sudo pacman -S nodejs npm
  ```

After installation, confirm with:

```bash
node -v
npm -v
```

---

### 3. Install project dependencies

```bash
npm install
```

This sets up everything needed to run Reveal.js locally.

---

### 4. Start the presentation

```bash
npm start
```

Then open your browser and go to:

```
http://localhost:3000
```

Slides will live-reload whenever you save changes to `slides.md`.

---

## Writing Slides

Edit the file `slides.md`. Use Markdown syntax and LaTeX for math support.

### Example:

```markdown
# Welcome

This is my presentation.

---

# Math

Einstein's formula: $E = mc^2$

---

# Vertical Slides

Slide 1

--
Slide 1.1

--
Slide 1.2

---

# The End
```

---

## Changing Themes

To change the visual style, edit this line in `index.html`:

```html
<link rel="stylesheet" href="dist/theme/moon.css" id="theme">
```

Available themes: `black`, `white`, `league`, `moon`, `night`, `solarized`, and others.

---

## Tips

- Use `---` for horizontal slides, `--` for vertical slides.
- Add speaker notes using `Note:` followed by your comment.
- Use `$$ ... $$` for block equations and `$...$` for inline math.
- Press `S` during the presentation to view speaker notes in presenter mode.

---

## For Students

To start your own presentation:

1. Go to the GitHub repository page: https://github.com/arampatzis/reveal-template
2. Click the green **"Code"** button, then choose **"Download ZIP"**
3. Extract the ZIP file to a folder on your computer
4. Open the folder in your terminal or code editor
5. Run:
   ```bash
   npm install
   npm start
   ```
6. Open `http://localhost:8000` in your browser
7. Start editing `slides.md` to build your presentation

---

## Requirements

- Git
- Node.js and npm (see installation section above)
- Modern browser (Chrome, Firefox, Safari)
