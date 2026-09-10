# 🇫🇷 French Memory Lab

A personal French-learning web app built with **React + Vite**.

It separates the material into 4 independent sections:

1. **Les jours de la semaine**
2. **Le verbe pronominal : s’appeler**
3. **Les nombres de 0 à 100**
4. **Communiquer en classe**

Each section uses repetition through:
- Flashcards
- French listening + writing
- Meaning multiple choice
- Scramble/rebuild
- Speaking/shadowing
- Matching (where useful)

## Important: French pronunciation

The app uses the browser's built-in Speech Synthesis API with `fr-FR`.
It automatically prefers an available French voice such as Google/Microsoft/other French voices, then falls back to the first `fr-FR` voice installed on the device.

For the best native-like practice:
- Chrome/Edge: check the installed French voices in your operating system/browser.
- On macOS/iPhone: install/select a French voice in System Settings if needed.
- Use **Slow** first, then **Normal**.

This app does not call a paid AI API for pronunciation.

## Run locally

Install Node.js 20+.

```bash
npm install
npm run dev
```

Open the local URL shown by Vite.

To test production:

```bash
npm run build
npm run preview
```

## Publish with GitHub + Vercel

### 1. Create a GitHub repository
Go to GitHub and create a new repository, e.g. `french-memory-lab`.

Keep it **Private** if this is only for you.

### 2. Upload this project

Either upload the files through GitHub's web UI, or use Git:

```bash
git init
git add .
git commit -m "Create French Memory Lab"
git branch -M main
git remote add origin YOUR_GITHUB_REPO_URL
git push -u origin main
```

### 3. Deploy on Vercel
1. Sign in to Vercel with GitHub.
2. Click **Add New → Project**.
3. Import `french-memory-lab`.
4. Framework: Vite should be detected automatically.
5. Build command: `npm run build`
6. Output directory: `dist`
7. Click Deploy.

Every future push to GitHub can trigger a new deployment.

## Make it personal/private

This starter version stores progress in **localStorage**, so it is not a public shared database.

If you want the site to be accessible only to you while still working across multiple devices, add **Supabase Auth + database** in the next version. Then:
- disable public sign-up
- allow only your account
- store vocabulary/progress in Supabase
- use Row Level Security so only your account can read/write its data

## Current scope

This version is intentionally simple and cheap:
- no paid AI API
- no database
- no account required
- French audio through the browser
- responsive on desktop and mobile

The 0–100 number set is fully included, with extra attention to 70/80/90 patterns.
