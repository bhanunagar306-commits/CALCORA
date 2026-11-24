# CALCORA – Start Here

## Keep this folder safe
This is the organized project copy. Keep the ZIP as your backup and extract a working copy before editing files.

## Main files
- `index.html` – app page
- `css/style.css` – design and responsive layout
- `js/app.js` – calculator features
- `js/pwa.js` – PWA installation behaviour
- `manifest.webmanifest` – PWA metadata and icons
- `service-worker.js` – offline caching

## Local preview on Windows
Open PowerShell in this folder and run:

```powershell
py -m http.server 8000
```

Then visit `http://localhost:8000`.

## GitHub upload reminder
Upload the contents of this folder into the repository root. `index.html` must appear at the top level of the repository.

## Before publishing
1. Test all calculator modes and settings.
2. Test the app on a desktop and a phone-sized viewport.
3. Test installation and offline mode on the deployed HTTPS site.
4. Review the QA and testing documents in `docs/`.
5. Verify current Microsoft Store artwork and package requirements before submission.
