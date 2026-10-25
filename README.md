<p align="center">
  <img src="icon.png" alt="MonolithCV Logo" width="120"/>
</p>

<h1 align="center">MonolithCV</h1>

<p align="center">
  A web app that formats your CV to fit perfectly on a single A4 page.
</p>

---

MonolithCV is a static web app that runs entirely in your browser. I made it to help me build a professional CV that actually fits on a single A4 page without having to fight with margins and font sizes.

No sign-ups, no server, no cloud syncing. All data stays in your browser's local storage.

## AI Assistance

Some parts of the code, such as drag-and-drop behavior, auto-fit logic, and local storage handling, were written or improved with the help of an AI assistant. The design decisions and core product direction were human-led.

## Features

- **Live A4 preview**: What you see on the screen is exactly what the printed PDF will look like.
- **Auto-fit**: Font sizes, spacing, and margins are adjusted automatically so your content fits on one page.
- **Drag & drop sections**: Reorder your CV sections directly from the preview pane.
- **6 Templates**: Minimalist, Compact, Modern, Classic, Tech, and Creative.
- **Profile photo editor**: Upload your picture, pan, zoom, and crop it (square, rounded, or circle).
- **Two-column layout**: Toggle the sidebar on or off depending on how much horizontal space you need.
- **Dark mode** and **bilingual UI** (English / Spanish), remembered between visits.
- **Local & Private**: Everything is saved to your browser's local storage. Export to PDF through the browser's print dialog.

## Usage

1. Open the site and click **New CV** (or **Continue** to resume your last CV).
2. Edit your content; the preview updates live.
3. Click **Export PDF** and choose *Save as PDF* in the print dialog. For best results, keep margins at *None* and enable *Background graphics*.

### Saving and loading

Your CV is saved automatically in the browser you are using. To move it to another browser or keep a copy:

- **Save**: open the *Data* tab in the editor and click *Export Backup* to download a `.json` file.
- **Load**: click *Import* on the main menu (or *Data → Import Backup* in the editor) and pick that file.

Clearing your browser data deletes the saved CV, so export a backup for anything important.

## Limitations

- Reordering sections uses HTML drag and drop, which does not work on touch screens.
- Only one CV is stored per browser at a time; use backups to keep several.

## Deploy to GitHub Pages

The site is plain HTML with no build step.

1. Push these files to the root of a GitHub repository (`index.html` must be at the root).
2. In the repository, go to **Settings → Pages**.
3. Under **Build and deployment**, set **Source** to *Deploy from a branch*, select your branch (e.g. `main`) and the `/ (root)` folder, then **Save**.
4. After a minute the site is available at `https://<your-username>.github.io/<repository-name>/`.

## Run locally

Open `index.html` directly in a browser, or serve the folder:

```bash
python3 -m http.server 8000
# then open http://localhost:8000
```

## License

GPL-3.0. See [LICENSE](LICENSE).
