# ⚡ ZIPPY v2.0 – phone app

A small app for logging HOH expenses on a phone: the amount, what it was for, the shop, and a photo of the receipt. It works without signal and sends everything to HOH cloud when the phone is back online. It works on iPhone and Android.

Tick **Reimbursable** on an expense you paid from your advance or your own money, so the office counts it against your advance instead of the safe.

At the end of each month, it also reminds whoever looks after the safe to do a **safe count**: tap **🔒 Safe count**, enter the dinars and dollars in the safe, and it goes to the office with the expenses.

This repository only holds the app itself. It contains no expenses, names or access codes; those stay on each phone and in HOH cloud. That's why it's safe for it to be public, which free GitHub Pages hosting requires.

## Publish it (once)

1. On github.com, create a **new repository** named `zip-receipt-phone`. Set it to **Public**.
2. Upload every file from this folder, then commit.
3. Go to **Settings → Pages**. Under *Build and deployment*, set **Source: Deploy from a branch**, **Branch: main**, folder **/ (root)**, then **Save**.
4. After a minute, the page shows your address, something like `https://YOUR-NAME.github.io/zip-receipt-phone/`.
5. Paste that address into ZIPPY: **Settings → Phone app address**.

## v2: joining with an invite link

With HOH cloud set up, people no longer need a setup link with an access code. In ZIPPY on the computer, use **People → Add person**, then send them the invite link it shows:
- **Staff** tap the link and they're in. No email or password needed. They see their advance balance at the top, and **Reimbursable** starts ticked on every expense (untick it when they paid with safe cash).
- **Admins and bookkeepers** tap the link and choose a password. They also get the **Safe count** button.

Then add it to the Home Screen (below).

## Updating

Change the files, then raise `VERSION` in `sw.js` (for example `zr-phone-v2`) so phones pick up the new version. Commit. Phones update the next time they open the app with internet.
