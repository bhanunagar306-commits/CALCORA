# CALCORA – Smart Calculator

**Precision Beyond Limits.**

CALCORA is an offline-capable progressive web calculator built with HTML, CSS and vanilla JavaScript.

## Features
- Basic arithmetic with operator correction, decimal validation and contextual percentage for addition/subtraction
- Scientific functions: trigonometry (DEG/RAD), inverse trigonometry, roots, logarithms, powers, factorial, constants and Ans
- Unit conversion: length, mass, area, volume, time, speed, digital storage and temperature
- Tools: discount + GST, EMI, age and binary/octal/decimal/hexadecimal converter
- Calculation history with copy, per-item notes, delete, clear confirmation and CSV export
- Royal, Neon, Light and System themes; sound toggle; adjustable precision, text and key sizes; reduced-motion setting
- Keyboard support, responsive layout, accessible focus states and PWA installation/offline shell

## Quick start (Windows)
1. Extract the ZIP file.
2. Open the `CALCORA` folder.
3. Open a terminal in this folder.
4. Run:

   ```bash
   py -m http.server 8000
   ```

5. Open `http://localhost:8000` in your browser.

Use a local web server rather than opening `index.html` directly, because service workers do not work from `file://`.

## Publish with GitHub Pages
1. Upload the **contents of this folder** to the root of your GitHub repository. Do not upload an extra enclosing `CALCORA` folder.
2. Keep `index.html` at the repository root.
3. In **Settings → Pages**, choose **Deploy from a branch**, select branch `main` and folder `/ (root)`, then save.
4. After deployment, open the HTTPS URL and test the calculator, installation and offline behaviour.

## Privacy
Calculations, history, theme and preferences are stored locally in the browser using `localStorage`. This project contains no analytics, account system or application backend. The app does not intentionally transmit calculator inputs. Browser/network requests required to load the hosted site are controlled by the hosting provider.

## Project layout
- `index.html` – application interface and page structure
- `css/style.css` – layout, responsive styles and themes
- `js/app.js` – calculator, converters, tools and local history
- `js/pwa.js` – install prompt and service-worker registration
- `manifest.webmanifest` – PWA name, display settings and icons
- `service-worker.js` – app-shell caching and offline support
- `assets/brand/` – source brand artwork
- `assets/icons/` – app icons in standard and maskable sizes
- `store-assets/` – Store promotional artwork and preview screenshots
- `docs/` – QA notes, bug-fix notes and manual testing checklist
- `privacy-policy.html` – app privacy policy

## Quality assurance
See `docs/QA-RESULTS.md` and `docs/TESTING-CHECKLIST.md`. Automated source-level checks are not a substitute for manual browser, device, accessibility, PWA and Store certification testing.

## License
MIT. See [LICENSE](LICENSE).
