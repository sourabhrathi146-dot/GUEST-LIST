# Guest List App — Setup Guide

This turns your Guest List tool into a real app icon on your phone's home screen —
no app store, no account needed except a free GitHub account.

You only need to do this **once**. After that, updating it is quick (see bottom).

---

## Step 1 — Create a free GitHub account (skip if you already have one)

1. Go to https://github.com/signup
2. Follow the steps to create your account.

---

## Step 2 — Create a repository (a folder for your app's files)

1. Go to https://github.com/new
2. **Repository name**: type `guest-list-app` (or anything you like)
3. Leave it set to **Public**
4. Click the green **Create repository** button

---

## Step 3 — Upload the app files

1. On your new repository's page, click **Add file** → **Upload files**
2. Drag in all of these files (all included in this folder):
   - `index.html`
   - `manifest.json`
   - `sw.js`
   - `icon-192.png`
   - `icon-512.png`
   - `icon-192-maskable.png`
   - `icon-512-maskable.png`
3. Scroll down, click the green **Commit changes** button

---

## Step 4 — Turn on GitHub Pages (this makes it a live website)

1. On your repository page, click **Settings** (top menu)
2. In the left sidebar, click **Pages**
3. Under "Build and deployment":
   - **Source**: choose **Deploy from a branch**
   - **Branch**: choose **main**, folder **/ (root)**
4. Click **Save**
5. Wait about 1 minute.

Your app's live web address will be:

```
https://<your-github-username>.github.io/guest-list-app/
```

Replace `<your-github-username>` with your actual GitHub username (check the
top-left of any GitHub page to confirm it exactly — don't guess).

**To confirm it's actually live**: go to your repo → click the **Actions** tab →
look for a green checkmark next to "pages build and deployment". If it's green,
your site is live even if the Settings page still looks unchanged.

---

## Step 5 — Install it on your phone

### On Android (Chrome)
1. Open the live web address above in Chrome
2. Tap the **⋮** menu (top right) → **Add to Home screen** → **Install**
3. A "Guest List" icon appears on your home screen — tap it to open like any app

### On iPhone (Safari)
1. Open the live web address above in Safari
2. Tap the **Share** icon (square with an arrow, bottom of screen)
3. Scroll down, tap **Add to Home Screen** → **Add**
4. A "Guest List" icon appears on your home screen

Once installed, it opens full-screen — no browser address bar — and works
**offline**. Your guest list is saved directly on your phone.

> **Note on voice entry**: The 🎤 Speak Name button works well in Chrome on
> Android. On iPhone, in-browser voice recognition is unreliable — typing
> names still works perfectly everywhere.

---

## Updating the app later

If you ever ask me to change something in the app:

1. I'll give you a new `index.html` (and possibly a new `sw.js`)
2. Go to your repo → **Add file** → **Upload files** → drop in the new file(s)
   with the **same names** → GitHub will ask to confirm replacing them → confirm
3. **Important**: if `sw.js` was updated, make sure you upload the new version —
   its cache version number changes, which is what tells phones to fetch the
   fresh copy instead of an old saved one.
4. On your phone, fully close the app and reopen it (or reinstall the icon) to
   see the update.

---

## Troubleshooting

- **Blank page or old version showing**: fully close the app (swipe it away
  from recent apps), reopen it. If still stuck, remove the home screen icon
  and reinstall it from Step 5.
- **Site shows a 404**: double-check the web address — the `guest-list-app`
  part must match your actual repository name exactly.
- **Install option missing**: make sure you're using Chrome (Android) or
  Safari (iPhone) — other browsers may not show the install prompt.
