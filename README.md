# Dispatch Board

A priority-based daily task scheduler. Fully static — no backend, no accounts, works completely on its own.

## What's in this folder
- `index.html` — the whole app (task scheduler, sleep/gym/run/weight tracking, analytics, daily motivation, light/dark theme, share-my-day image export)
- `manifest.json` — makes it installable as a home screen app
- `sw.js` — service worker (required by Android for install prompts)
- `icons/` — app icons

## How to put this on GitHub (one time)

1. Go to [github.com/new](https://github.com/new) and create a repository (e.g. `dispatch-board`). Keep it **Public** — Vercel's free plan needs that for personal projects, and you already decided that's fine.
2. On your computer/phone, unzip this folder.
3. Upload all the files (`index.html`, `manifest.json`, `sw.js`, and the `icons` folder) into that new GitHub repo — easiest way on mobile: open the repo page → **Add file → Upload files** → select everything → **Commit changes**.

## How to deploy it on Vercel (one time)

1. Go to [vercel.com](https://vercel.com) and sign up using your GitHub account (one tap — no separate password needed).
2. Click **Add New → Project**.
3. Select the `dispatch-board` repository you just created.
4. Leave all settings as default (it's a static site, Vercel figures it out automatically) and click **Deploy**.
5. In under a minute, you'll get a real link like `https://dispatch-board-yourname.vercel.app` — this is your permanent, public, real HTTPS website.

## Adding it to your phone's home screen

Open your new Vercel link in your phone's browser:

- **Android (Chrome):** tap **⋮** → **Add to Home screen** (or you may see an automatic "Install app" banner — even better, tap that)
- **iPhone (Safari):** tap the **Share** icon → **Add to Home Screen**

Because this is now a real HTTPS site with a proper manifest and service worker, the icon and install prompt will work reliably — this was the missing piece before.

## Making future changes

Whenever you want to change something (colors, features, tasks), edit `index.html` in this project and re-upload it to GitHub. Vercel automatically redeploys your site within a minute or two of any GitHub update — no extra steps needed on Vercel's side once it's connected.

## About your data

This version saves your tasks and progress using `localStorage`, which keeps everything **on your own device, in your own browser** — nothing is sent to any server. That also means: if you clear your browser data or switch phones, your history won't carry over automatically. Back up important progress if that ever matters to you.
