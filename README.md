# spnd. — PWA Setup & Deploy Guide

## Files in this folder
```
index.html      ← The app
manifest.json   ← PWA metadata (name, icon, theme)
sw.js           ← Service worker (offline support)
icon-192.png    ← App icon
icon-512.png    ← App icon (large)
```

---

## Deploy in 2 minutes (Netlify — Free)

1. Go to https://netlify.com and sign up (free)
2. Drag and drop this entire folder onto the Netlify dashboard
3. You'll get a live URL like `https://spnd-abc123.netlify.app`
4. Done ✅

---

## Install on Android as an App

1. Open your Netlify URL in **Chrome on Android**
2. Tap the **⋮ menu** (top right)
3. Tap **"Add to Home screen"**
4. Tap **"Install"**
5. App icon appears on your home screen — opens fullscreen, no browser chrome, works offline 🎉

---

## Other free deploy options

| Platform     | How |
|-------------|-----|
| Vercel      | `npm i -g vercel` → `vercel` in this folder |
| GitHub Pages | Push to repo → Settings → Pages → Deploy from main |
| Cloudflare Pages | Drag & drop at pages.cloudflare.com |

---

## Want to publish to the Play Store?

Use **Bubblewrap** (Google's official PWA → Android APK tool):

```bash
npm i -g @bubblewrap/cli
bubblewrap init --manifest https://your-url.netlify.app/manifest.json
bubblewrap build
```

This generates a signed `.aab` file you upload to Google Play Console.
You need a Google Play developer account ($25 one-time fee).
