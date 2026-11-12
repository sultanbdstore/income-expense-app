<p align="center"><img src="logo.png" alt="Income & Expense logo" width="160"></p>

# আয়-ব্যয় হিসাব · Income & Expense

A mobile-friendly income and expense app in **Bangla and English**. It runs entirely in your browser, works **offline**, and keeps your data on your own device. No account, no server, no libraries.

## Features

**Fast entry**
- Built-in calculator keypad: type `120+30×2` and the total is worked out for you. Bangla digits are shown if you choose them.
- One-tap **Quick add** buttons for your most used categories, remembers your last wallet, suggests your recent notes.
- Long-press the installed app icon for *Add expense* / *Add income* shortcuts.
- **Undo** after deleting a record.
- **Recurring entries** (rent, salary, bills) are added automatically when the date comes.

**Money overview**
- Colourful wallet cards (cash, bKash, Nagad, bank; add your own) with separate balances and transfers between wallets.
- Hide / show balance, "you can spend about X per day" from your monthly budget, last-7-days chart, comparison with last month.
- Reports: expense donut chart, income by category, 6-month chart, and insights (biggest category, biggest expense, daily average).

**Planning**
- Monthly budget per category and overall, with progress bars (yellow at 80%, red when exceeded).
- Savings goals, and debts (দেনা-পাওনা) with due dates, part payments and reminders.

**Your data**
- Excel (`.xlsx`, 5 sheets), CSV and print-ready PDF report; JSON backup, restore and a share button for Google Drive / WhatsApp.
- PIN lock (4-6 digits).
- First-run welcome screen to set the language and what is in each wallet right now.
- Bangla / English switch, Bangla or English digits, custom currency symbol, light / dark theme, installable on the phone home screen (PWA).

Debt and savings entries change wallet balances but are not counted as income or expense in the reports.

## Honest notes

- **Data lives in the browser storage of the device.** Clearing browser data erases it, so download a backup regularly (the app reminds you after 7 days). Different phones and browsers do not sync with each other. To move data, restore the backup file on the other device.
- **PIN** locks the app screen. It does not encrypt the data, so keep backup files safe.
- **Cloud backup** is manual: use *Share / save to Drive* (phones) or download the file and upload it yourself. Automatic cloud sync would need an account and a server, which this project deliberately avoids.

## Run it

Open `index.html` in Chrome, Edge, Firefox or Safari. Or serve the folder:

```bash
python3 -m http.server 8000
```

**GitHub Pages:** push the repo, then *Settings → Pages* → source **GitHub Actions** (the included workflow publishes on every push to `main` or `master`), or **Deploy from a branch** → `main` → `/ (root)`. Open `https://YOUR-USERNAME.github.io/REPO-NAME/` on your phone, then use *Add to Home screen*.

If you edit `index.html` after publishing, change `VERSION` in `sw.js` so phones pick up the new version.

## Project structure

```
index.html              the whole app in one self-contained file
sw.js                   offline cache (service worker)
manifest.webmanifest    installable-app manifest
logo.png, icons/        logo, favicons, apple-touch and maskable icons
.github/workflows/      optional GitHub Pages deployment
```

## License

MIT, see [LICENSE](LICENSE).
