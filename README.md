# Centre for Research in Tamil Nadu (CRTN)

Static website for **CRTN** — A Progressive Knowledge Collective for Social Transformation.

---

## Host on GitHub Pages as `crtn.github.io`

To get the URL **https://crtn.github.io**, GitHub requires:

1. A **user account** or **organization** named exactly **`crtn`**
2. A **repository** named exactly **`crtn.github.io`** (not just `crtn`)

GitHub only serves `crtn.github.io` when the repo is **crtn/crtn.github.io**. Your current repo [TN-Center-For-Research/crtn](https://github.com/TN-Center-For-Research/crtn) will always be **tn-center-for-research.github.io/crtn/**.

### Option A: Create a new account/org `crtn` and use `crtn.github.io`

1. **Create a GitHub account or organization named `crtn`**
   - New user: [github.com/signup](https://github.com/signup) — choose username **crtn** (if still available).
   - Or create an org: [github.com/organizations/plan](https://github.com/organizations/plan) — create organization **crtn**.

2. **Create the Pages repository**
   - Go to [github.com/new](https://github.com/new) **while logged in as `crtn`**.
   - **Repository name:** `crtn.github.io` (must be exactly this).
   - Visibility: **Public**. Do not add README, .gitignore, or license.
   - Click **Create repository**.

3. **Push this project to the new repo**

   From your project folder:

   ```bash
   cd /path/to/crtn

   git init
   git add index.html styles.css README.md asset/
   git commit -m "Add CRTN static website"
   git remote add origin https://github.com/crtn/crtn.github.io.git
   git branch -M main
   git push -u origin main
   ```

4. **Enable Pages**
   - Repo **Settings** → **Pages**.
   - Source: **Deploy from a branch**.
   - Branch: **main**, Folder: **/ (root)** → Save.

   The site will be at **https://crtn.github.io** (may take 1–2 minutes).

### Option B: Keep TN-Center-For-Research and use a custom domain

If you want to keep the repo under [TN-Center-For-Research](https://github.com/TN-Center-For-Research/crtn):

- Buy a domain like **crtn.in** or **crtn.org**.
- In repo **Settings** → **Pages**, set **Custom domain** to that domain and follow GitHub’s DNS instructions.
- The site will then be reachable at **https://crtn.in** (or your chosen domain), while still being hosted from the same repo.

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
