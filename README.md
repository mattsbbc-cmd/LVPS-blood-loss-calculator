# Theatre Blood Loss: installable phone app

A progressive web app (PWA). It installs to the home screen like an app, runs full screen, and works offline once opened. It costs nothing, and you don't need to go through an app store.

## 1. Host it (free, about 10 minutes)

**Option A: GitHub Pages**
1. Create a free account at github.com and a new **public** repository (e.g. `blood-loss`).
2. Use "Add file → Upload files" to upload everything in this folder.
3. Go to Settings → Pages, set Source to "Deploy from a branch", choose `main` and `/ (root)`, then click Save.
4. After a minute the app is live at `https://<username>.github.io/blood-loss/`.

**Option B: Netlify Drop**
Go to app.netlify.com/drop and drag this folder onto the page. A free account keeps the link permanent.

The app needs to be served over https, which both options do. Opening the file directly from a phone's file manager won't let it install.

## 2. Install on phones

- **iPhone (Safari):** open the link, tap Share, then tap "Add to Home Screen".
- **Android (Chrome):** open the link, open the ⋮ menu, then tap "Install app" (or "Add to Home screen").

Open the app once while online. After that it works without a signal.

## 3. Before clinical use

- Calibrate each swab type using **Calibrate swabs** at the top of the app. Tap "Start calibration" and follow the five steps. Repeat whenever a new box or brand arrives. The app warns if a reading differs by more than 10% from the last calibration.
- Check the species blood volume defaults (Patient → "Species blood volume defaults"). They ship as dog 90 mL/kg and cat 66 mL/kg (Jutkowitz et al., JAVMA 2002). Change them if your service uses a different reference.
- Tap "Start new case" to clear the example case.
- Data is saved only on each phone. Patient identifiers are never entered or stored.

## Exporting a case to the patient file

At the end of the case, scroll to **Report for patient file**. Enter the patient name and hospital number and the procedure. Then both the **anaesthetist** and the **theatre technician** add their names to authorise the record. Export is blocked until both names are entered. Then:

- **Email PDF:** opens the phone's share menu. Choose Mail or Outlook, add the recipient (e.g. the records inbox) and send.
- **Save PDF to phone:** saves the file so it can be attached or uploaded later.

The PDF includes patient details, the inputs used, the totals, a time-stamped swab log, the calibration status of each swab type used, the anaesthetist's and technician's names, and the method and references.

Patient details go only into the PDF and are not stored in the app. Export works only in the installed app, not the claude.ai preview.

## Updating

Edit the files, change `VERSION` in `sw.js` (e.g. `tbl-v1.1`), and upload them again. Phones pick up the update the next time the app is opened online.
