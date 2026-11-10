# LightOn Academy — installable app

These files are the **LightOn Academy app** (a PWA) that runs at **https://lightonacademy.github.io**.

- Students, parents, sponsors and staff open the link, sign in, and can **install it on their phone or computer** like a normal app.
- The data and logic live in Google Apps Script plus the Google Sheet. These files are only the screens.
- **The app keeps working even if the WordPress hosting or the lightonacademy.com domain expires.**

| File | Purpose |
|---|---|
| `index.html` | All the screens (built from the Apps Script `Index.html`) |
| `config.js` | **The only file you edit**: your Apps Script web app URL |
| `manifest.webmanifest` | App name, colours and icons, so it can be installed |
| `sw.js` | Offline support and fast loading |
| `icons/` | App icons made from the LightOn logo |

## Updating the app later
1. Upload the new `index.html` (keep your `config.js`).
2. In `sw.js`, change `VERSION = 'lighton-v6.0.0'` to a new value (e.g. `v6.0.1`).
3. Commit. Phones show **"A new version of the app is ready — Update"**.

Your Apps Script URL is visible in `config.js`. That is expected and safe: every request still needs a valid login and PIN, and the only public functions are the registration form and course list.
