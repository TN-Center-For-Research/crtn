# Centre for Research in Tamil Nadu (CRTN)

Static website for **CRTN** — A Progressive Knowledge Collective for Social Transformation.

---

## Host on GitHub Pages as `crtn.github.io`

Follow these steps to publish the site at **https://crtn.github.io**.

### 1. Create a GitHub repository

- Go to [github.com/new](https://github.com/new).
- **Repository name:** `crtn` (must be exactly `crtn` for the URL `crtn.github.io`).
- Set visibility to **Public**.
- Do **not** add a README, .gitignore, or license (you already have files locally).
- Click **Create repository**.

### 2. Initialize git and push your site

In a terminal, from your project folder:

```bash
cd /home/zs-khaleel/Documents/crtn

# Initialize git (if not already)
git init

# Add all files (index.html, styles.css, asset/banner.png)
git add index.html styles.css asset/
git commit -m "Add CRTN static website"

# Add GitHub as remote (replace YOUR_USERNAME with your GitHub username)
git remote add origin https://github.com/YOUR_USERNAME/crtn.git

# Push to GitHub (main branch)
git branch -M main
git push -u origin main
```

**Important:** Ensure `asset/banner.png` exists in the `asset` folder before running `git add asset/`. If the folder is empty, create it and add your banner image there.

### 3. Turn on GitHub Pages

- Open your repo: **https://github.com/YOUR_USERNAME/crtn**
- Go to **Settings** → **Pages** (left sidebar).
- Under **Build and deployment**:
  - **Source:** Deploy from a branch
  - **Branch:** `main` (or `master`)
  - **Folder:** `/ (root)`
- Click **Save**.

### 4. Wait and open your site

- GitHub may take 1–2 minutes to build.
- Your site will be at: **https://crtn.github.io**

If you used a different branch or folder, adjust the **Branch** and **Folder** options in Settings → Pages accordingly.

---

## Project structure

```
crtn/
├── index.html      # Main page
├── styles.css      # Styles
├── asset/
│   └── banner.png # Banner image
└── README.md      # This file
```

## Local preview

Open `index.html` in a browser, or use a simple server:

```bash
cd /home/zs-khaleel/Documents/crtn
python3 -m http.server 8000
```

Then visit: **http://localhost:8000**
