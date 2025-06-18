# Reveal.js Template for Students

This repository provides a ready-to-use template for writing slides in Markdown using [Reveal.js](https://revealjs.com/) and hosting them via GitHub Pages.

---

## 🚀 Getting Started

### 1. Install Node.js and npm

You need Node.js (which includes npm) installed on your system.

#### Windows / macOS / Linux:
- Visit: https://nodejs.org/
- Download the **LTS** version and install it

To verify:
```bash
node -v
npm -v
```

---

### 2. Get the Template

**Do not clone this repository.**  
Instead:

1. Visit: https://github.com/arampatzis/reveal-template
2. Click **Code → Download ZIP**
3. Extract it on your computer
4. Rename the folder as you wish

---

### 3. Install Required Packages

Inside the extracted folder, open a terminal and run:

```bash
npm install
```

This installs local development tools like the server (`gulp`).

---

### 4. Run the Presentation Locally

```bash
npm start
```

Open your browser at:
```
http://localhost:8000
```

You should see your slides rendered.

---

## 📝 Editing Your Slides

Slides are written in `slides.md` using Markdown.

Use `---` to separate horizontal slides, and `--` for vertical slides:

```markdown
# Welcome

---

## Slide 1

Some text

--

- Vertical slide 1

--

- Vertical slide 2
```

---

## 🎨 Customizing Theme

Reveal.js themes are in the `dist/theme` folder.

To change the theme, edit `index.html` and modify this line:

```html
<link rel="stylesheet" href="dist/theme/black.css" id="theme">
```

Try other themes like `white.css`, `night.css`, `moon.css`, etc.

---

## 🌐 Hosting Slides on GitHub Pages

You can publish your presentation online for free using GitHub Pages.

### Step-by-step:

1. Make sure your repository includes:
   - `index.html`
   - `slides.md`
   - `dist/` and `plugin/` folders from Reveal.js
   - empty `.nojekyll` file (prevents GitHub from using Jekyll)

2. Go to your GitHub repository → **Settings** → **Pages**

3. Under **Build and deployment**, set:
   - **Source**: `Deploy from a branch`
   - **Branch**: `main`
   - **Folder**: `/ (root)`
   - Click **Save**

4. Wait 1–10 minutes. GitHub will show a green message:
   ```
   Your site is live at https://<your-username>.github.io/<repo-name>/
   ```

5. If the green message does not appear:
   - Add a `.nojekyll` file (empty file with that name)
   - Make a small commit to trigger a rebuild:
     ```bash
     git commit --allow-empty -m "Trigger rebuild"
     git push
     ```

6. Visit your live slides in the browser!

This allows you and your students to share presentations with a link.

---

## 🔒 Public vs Private Repos and Ways to Share Slides

### ✅ Option 1: GitHub Pages (Public Repo)
- If your repository is **public**, GitHub Pages will host your presentation at:
  ```
  https://<your-username>.github.io/<repo-name>/
  ```
- This is the easiest and recommended way to publish Reveal.js slides.

### 🚫 Option 2: GitHub Pages (Private Repo)
- GitHub Pages **does not** work for private repos unless you are on a **GitHub Enterprise** plan.
- You will see a 404 or the site won’t build.

### 🛠 Option 3: Local Server (for Private Sharing)
- You can run your slides locally with:
  ```bash
  npm start
  ```
- Then access them at:
  ```
  http://localhost:8000/
  ```
- This works for development or sharing over a local network.

### 📤 Option 4: Export to PDF
- Reveal.js can export slides to PDF:
  ```bash
  npm install -g decktape
  decktape reveal http://localhost:8000 slides.pdf
  ```
- Useful for email, offline viewing, or submissions.

### 🧪 Option 5: Self-host on your own server
- Upload your site to any static host (e.g. Netlify, Vercel, your own Apache/Nginx server).
- Make sure the folder has:
  - `index.html`
  - All assets (`dist/`, `plugin/`, etc.)

These options allow flexibility depending on your privacy needs.
