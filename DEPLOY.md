# Deploying to GitHub Pages (account: KarterGIT)

Run these from PowerShell. Your site folder is:
`C:\Users\krigz\Claude\KarterGIT.github.io`

---

## Step 0 — Switch the GitHub CLI to the KarterGIT account

The CLI is currently logged in as **KarterRiggs**. Add and switch to KarterGIT:

```powershell
gh auth login          # choose GitHub.com → HTTPS → login with browser, sign in as KarterGIT
gh auth switch --user KarterGIT
gh auth status         # confirm "Active account: true" is on KarterGIT
```

---

## Step 1 — Create the Pages repo (must be named EXACTLY this)

A "user site" repo must be named `<username>.github.io`:

```powershell
cd "C:\Users\krigz\Claude\KarterGIT.github.io"
git init
git add .
git commit -m "Initial portfolio site"
git branch -M main
gh repo create KarterGIT.github.io --public --source . --remote origin --push
```

That command creates the repo on GitHub AND pushes your code in one shot.

---

## Step 2 — Turn on GitHub Pages

For a `username.github.io` repo, Pages is usually on automatically. To confirm:

```powershell
gh repo view KarterGIT.github.io --web
```

In the browser: **Settings → Pages →** Source = "Deploy from a branch", Branch = `main`, folder = `/ (root)` → Save.

Wait ~1–2 minutes, then visit:  **https://kartergit.github.io**

---

## Step 3 — Set up your profile README

This special repo (named the same as your username) shows at the top of your profile.
Your ready-made README is at: `C:\Users\krigz\Claude\github-profile-README\README.md`

```powershell
cd "C:\Users\krigz\Claude\github-profile-README"
git init
git add README.md
git commit -m "Add profile README"
git branch -M main
gh repo create KarterGIT --public --source . --remote origin --push
```

---

## Step 4 — Polish the profile (in the browser)

- **Avatar:** add a clean headshot or a simple monogram.
- **Bio:** "AI student & builder · I learn AI by building it."
- **Add the website link:** put `https://kartergit.github.io` in your profile's website field.
- **Pin repos:** Profile → "Customize your pins" → pin `KarterGIT.github.io` and your best project repos.
- **Repo hygiene:** give each repo a one-line description + topics (e.g. `ai`, `python`, `automation`); archive anything unfinished.

---

## Updating the site later

Edit files in the site folder, then:

```powershell
cd "C:\Users\krigz\Claude\KarterGIT.github.io"
git add .
git commit -m "Describe your change"
git push
```

GitHub Pages redeploys automatically within a minute.
