# Playdate website

Static site for the Playdate app: landing page, [privacy policy](privacy/index.html),
[terms of service](terms/index.html), and the `.well-known/` files for Android App
Links + iOS Universal Links.

Deployed automatically to GitHub Pages on push to `main`:
**https://crhymes.github.io/playdate-site/**

When a custom domain is registered:
1. Add it in repo Settings → Pages → Custom domain (creates the CNAME).
2. Fill in the SHA-256 fingerprint in `.well-known/assetlinks.json` (`eas credentials --platform android`).
3. Fill in the Apple Team ID in `.well-known/apple-app-site-association`.
4. Replace the placeholder contact emails in `privacy/index.html` and `terms/index.html`.
5. Follow the app-side steps in the main repo's App Links checklist (app.json hosts, `EXPO_PUBLIC_APP_DOMAIN`, `APP_URL` secret).
