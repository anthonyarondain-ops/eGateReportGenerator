# H.A.Z.E. — e-Gate Intelligence & Report Generator (v1.0)

This is a replacement front-end package for the existing GitHub Pages repository:

- Repository: https://github.com/anthonyarondain-ops/eGateReportGenerator
- Live site: https://anthonyarondain-ops.github.io/eGateReportGenerator/

## Features
- Full H.A.Z.E. rebrand and responsive desktop/mobile interface.
- Smart, offline, rule-based symptom analyzer with ranked possible causes and safe next checks.
- Knowledge base covering passport scanner, sensors, door module, vDesk/application, network, power, and upstream-service issues.
- Report generator preserving Technician ID (default `A007`), date/time, area, gate, issue, Action Taken, Root Cause, Resolution, and Recommendation.
- Philippine time formatting (`Asia/Manila`) for report output.
- Additional Details field, quick issue templates, copy report, browser-local saved history, and JSON export.
- PWA manifest and service worker for supported offline use.
- No active network scanning or production gate configuration changes.

## Test locally on Kali Linux
1. Extract the ZIP.
2. Open a terminal in the extracted `eGateReportGenerator-HAZE-v1.0` folder.
3. Run:
   ```bash
   python3 -m http.server 8080
   ```
4. Open `http://127.0.0.1:8080`.

## Update the existing GitHub Pages site
1. Open the repository above and create a backup/branch before changing files.
2. Download and extract this ZIP.
3. Replace the repository's `index.html`, `manifest.webmanifest`, and `sw.js` with these versions. Keep unrelated files such as LICENSE or repository settings.
4. Test locally first. Check the report generator, date/time, copy, save/history, export, and mobile layout.
5. Commit and push the changes to the branch configured for GitHub Pages (commonly `main`).
6. Wait for the Pages deployment to finish, then reload the live website. If an old version remains, do a hard refresh or clear the site's cached data/service worker.

## Data and safety notes
- H.A.Z.E. currently uses transparent keyword/rule matching. Scores are not probabilities and cannot confirm the root cause.
- Only enter actions actually performed and causes verified on site.
- Saved reports are kept in the current browser's local storage. They do not automatically sync between PC and Android.
- PWA/service-worker behavior requires localhost or HTTPS; plain HTTP LAN addresses may not qualify as a secure context.
- Network diagnostics are intentionally not implemented. Production-network testing requires explicit authorization and approved procedures.
