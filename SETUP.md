# Setup guide — premium GitHub profile

## 1. Create the special repo
Create a **public** repo named exactly **`felicia-sw`** (same as your username) at github.com/new. GitHub shows a hint that it's a special repository — its README appears on your profile.

## 2. Push these files
```bash
cd felicia-sw
git init
git add .
git commit -m "✨ premium animated profile"
git branch -M main
git remote add origin https://github.com/felicia-sw/felicia-sw.git
git push -u origin main
```
(Delete this SETUP.md before pushing, or leave it — it won't show on your profile.)

## 3. Activate the snake 🐍
The workflow in `.github/workflows/snake.yml` generates the contribution snake.

1. Go to the repo → **Actions** tab → enable workflows if prompted
2. Repo **Settings → Actions → General → Workflow permissions** → select **Read and write permissions** → Save
3. Actions tab → **generate contribution snake** → **Run workflow**

Until the first run finishes, the snake image will show as broken — that's expected. It refreshes daily afterward.

## 4. Customize
- **Typing phrases**: edit `assets/typing-dark.svg` / `typing-light.svg`. When changing a phrase, update its clip `width` and caret `x` values: width ≈ `characters × 12`, caret end ≈ `50 + width`.
- **Tagline**: "WEB · DATA · RESEARCH" lives in both `hero-*.svg` files.
- **Tech stack icons**: edit the `i=` list in the skillicons.dev URLs in README.md ([full icon list](https://skillicons.dev)).
- **LinkedIn badge**: replace `https://www.linkedin.com/` in README.md with your profile URL (or delete the badge).
- **Colors**: dark palette is cyan `#22d3ee` / purple `#a855f7` / pink `#ec4899`; light is `#0891b2` / `#7c3aed` / `#db2777`. Find-and-replace in the SVGs and stats URLs to retheme.

## How light/dark works
Every visual is wrapped in a `<picture>` tag with `prefers-color-scheme` sources, so GitHub serves the matching variant automatically. Animations are pure SMIL/CSS inside the SVGs — no JavaScript, works in any GitHub theme, no external fonts.
