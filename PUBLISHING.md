# Publishing Codebusters Speed Guide

This folder is an installable offline web app (PWA). It's hosted on GitHub Pages at
`https://maitreyeesingh2012-arch.github.io/codebusters-speedpractise/` (once the repo is pushed), and the same site becomes
both the Android app and the desktop app.

To update the app: edit `../cipher-speed-guide.html`, run `python make_app.py` in the codebusters
folder, then commit and push this folder. Installed copies update the next time they open online.

## Desktop app (Windows, Mac, Chromebook)

**Quickest (free):** open the site in Chrome or Edge and click the install icon in the address bar
(or menu → *Cast, save and share → Install page as app* in Chrome, *Apps → Install this site as an app* in Edge).
It opens in its own window, gets a Start-menu / dock icon, and works offline.

**Microsoft Store (optional, free developer account for individuals):**
1. Go to https://www.pwabuilder.com, enter the site URL, choose **Package for stores → Windows**.
2. Create the app in Microsoft Partner Center to get the publisher details PWABuilder asks for.
3. Upload the generated `.msixbundle` in Partner Center and submit.

## Google Play

1. Open https://www.pwabuilder.com, enter the site URL, choose **Package for stores → Android**.
2. Package id: `io.github.maitreyeesingh2012arch.codebusters`. Download the zip and **keep the signing key and its passwords safe**.
3. Create a repo named `maitreyeesingh2012-arch.github.io` in the same account (if it doesn't exist) and put the
   zip's `assetlinks.json` in it at `.well-known/assetlinks.json`, with GitHub Pages on. Android checks this file
   at the root of the domain to let the app open the site full screen, with no browser bar.
   After Play App Signing is on, also add the SHA-256 fingerprint from Play Console → App integrity.
4. In Play Console (one-time US$25 developer fee), create the app, upload the `.aab`, and fill in:
   - Privacy policy: `https://maitreyeesingh2012-arch.github.io/codebusters-speedpractise/privacy.html`
   - Data safety: no data collected or shared.
   - Target audience: 13+ (or include younger ages, which puts it under the Families policy; the app has
     no ads, analytics or accounts, so that's already satisfied).
   - Content rating questionnaire, store listing text, phone screenshots, 512 px icon (`icons/icon-512.png`).
5. New personal developer accounts must run a closed test with at least 12 testers for 14 days before
   the app can go public.

## Store listing text (draft)

**Short description:** Practice every Codebusters cipher with real tournament questions.

**Full description:** Train for Science Olympiad Codebusters with over 3,000 questions from real
2021–2026 tournaments: Aristocrats, Patristocrats, Xenocrypts, Homophonic, Hill, Porta, Baconian,
Nihilist, Checkerboard, Columnar, Fractionated Morse, Cryptarithms and more. Time yourself and see how
you compare with competitive solvers, warm up with one-minute speed drills, learn Morse and Baconian with
flashcards, and turn solving helpers on or off to match tournament conditions. Works offline. No ads,
no accounts, nothing collected.
