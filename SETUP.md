# Setup guide — GitHub profile (text-first)

## 1. Create the special repo
Create a **public** repo named exactly **`felicia-sw`** (same as your username) at github.com/new. GitHub shows a hint that it's a special repository — its README appears on your profile.

## 2. Push these files
```bash
cd felicia-sw
git add .
git commit -m "✨ text-first profile"
git push
```
(Delete this SETUP.md before pushing, or leave it — it won't show on your profile.)

## 3. Activate the snake 🐍
The workflow in `.github/workflows/snake.yml` generates the contribution snake.

1. Go to the repo → **Actions** tab → enable workflows if prompted
2. Repo **Settings → Actions → General → Workflow permissions** → select **Read and write permissions** → Save
3. Actions tab → **generate contribution snake** → **Run workflow**

Until the first run finishes, the snake image will show as broken — that's expected. It refreshes daily afterward.

## 4. Customize
- **ASCII hero**: the FELICIA banner and tagline live in the first code block of README.md. Regenerate with any FIGlet tool (font: "ANSI Shadow") if you want different text.
- **Terminal intro**: edit the `whoami` / `status` lines in the second code block.
- **Tech stack**: plain text in the `## ⚡ tech stack` code block — edit freely.
- **LinkedIn badge**: already set to `https://www.linkedin.com/in/feliciasword-976870276`.
- **Stats colors**: dark palette is cyan `#22d3ee` / purple `#a855f7` / pink `#ec4899`; light is `#0891b2` / `#7c3aed` / `#db2777` — encoded in the github-readme-stats URLs.

## Design notes
Everything except the stats cards and the snake is plain text/ASCII, so it renders instantly in any theme, on mobile, and even when image services are down. The two stats cards and the snake are kept because they're dynamic (auto-updating) and can't be replicated in text. The `assets/` folder (old SVG hero/dividers/footer) is no longer referenced — safe to delete.
