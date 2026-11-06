# ⚡ Zip Receipt v1.0 – phone app

A small app for logging HOH expenses on a phone: the amount, what it was for, the shop, and a photo of the receipt. It works without signal and sends everything to the office's Google Sheet when the phone is back online. It works on iPhone and Android.

At the end of each month, it also reminds whoever looks after the safe to do a **safe count**: tap **🔒 Safe count**, enter the dinars and dollars in the safe, and it goes to the office with the expenses.

This repository only holds the app itself. It contains no expenses, names or access codes; those stay on each phone and in the Google Sheet. That's why it's safe for it to be public, which free GitHub Pages hosting requires.

## Publish it (once)

1. On github.com, create a **new repository** named `zip-receipt-phone`. Set it to **Public**.
2. Upload every file from this folder, then commit.
3. Go to **Settings → Pages**. Under *Build and deployment*, set **Source: Deploy from a branch**, **Branch: main**, folder **/ (root)**, then **Save**.
4. After a minute, the page shows your address, something like `https://YOUR-NAME.github.io/zip-receipt-phone/`.
5. Paste that address into Zip Receipt: **Settings → Phones & Google Sheet → Phone app address**.

## Give it to someone

1. In Zip Receipt, click **Settings → Make phone setup link** and send the link privately (WhatsApp is fine). It contains the access code.
2. On their phone, they open the link and type their name.
3. They add it to the Home Screen:
   - **iPhone (Safari):** Share button → **Add to Home Screen**.
   - **Android (Chrome):** ⋮ menu → **Add to Home screen** (or **Install app**).

After that it opens like a normal app, works offline, and remembers them.

## Updating

Change the files, then raise `VERSION` in `sw.js` (for example `zr-phone-v2`) so phones pick up the new version. Commit. Phones update the next time they open the app with internet.
