# TaskBoard Mobile 1.0

A small tasks + notes app for your Android phone. It installs from Chrome, opens full-screen like a normal app, works offline, and keeps all data on the phone.

## One-time setup (about 10 minutes, easiest from a laptop)

1. **Create the repository**
   - Go to github.com, click **New repository**.
   - Name it `taskboard-mobile`.
   - Choose **Public**. Free GitHub Pages needs a public repo. Only the app's code is public; your tasks and notes never leave your phone.
   - Click **Create repository**.
2. **Upload the files**
   - Click **uploading an existing file**, or **Add file → Upload files**.
   - Drag in all 7 files from this folder: `index.html`, `sw.js`, `manifest.webmanifest`, the three `icon-*.png` files and this README.
   - Click **Commit changes**.
3. **Turn on GitHub Pages**
   - Go to **Settings → Pages**.
   - Under *Build and deployment*, set Source to **Deploy from a branch**, Branch to **main**, and folder to **/ (root)**.
   - Click **Save**, then wait 1–2 minutes. The page shows your site link.
4. **Install on your phone**
   - Open `https://<your-username>.github.io/taskboard-mobile/` in **Chrome** on the phone.
   - Tap **⋮** → **Install app** (on some phones it says **Add to Home screen → Install**).
   - Open TaskBoard from the home-screen icon. From now on it works without internet.

## Using it

- **Tasks:** tap **+** and type, e.g. `Pay electricity bill #home !A1 +bills due:fri`.
  - `#project` sets the project, `!A1` the priority and `+label` a label.
  - Due dates: `due:today`, `due:tmr`, `due:fri`, `due:nw` (next Monday), `due:+3` (in 3 days), `due:25/10`.
  - Status: `s:started`, `s:inprogress`, `s:blocked`, `s:later`, and so on.
- **Gestures:** swipe a task right to complete it and left to delete it. Every action has **Undo**.
- **View options** (the sliders icon): sort, group, hide completed and delete completed.
- **Notes:** Notebook → Section → Note, with bold, italic, underline, bullets, numbering, checklists and highlight.
  - Put the cursor on a line and tap **→ Action** to turn it into a task linked to the note.
  - **⋮ → Copy content** gives email-ready text, and **Share** sends to WhatsApp, Gmail and similar apps.
- **Android back button** closes whatever is open, just like a native app.

## Keeping your data safe

- Data lives in the app's storage on this phone. **Uninstalling the app or clearing Chrome's site data erases it.**
- **Settings → Backup:**
  - **Save backup to phone** saves a `.json` file to Downloads.
  - **Share backup** sends it to Drive or Gmail.
  - **Restore from backup file** brings a backup back.
- The app reminds you if you haven't backed up for a week.
- It also keeps **daily snapshots** for 7 days, and a **Trash** that holds deleted items for 30 days.
- To move to a new phone: back up on the old phone, install on the new one, then restore.

## Updating later

Replace the changed files in the GitHub repo. Then change the version in `sw.js` (for example `taskboard-mobile-v1.0.1`). Phones pick up the update the next time the app opens, and a **Reload** prompt appears.
