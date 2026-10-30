# BeyBoss Tech — Certificate Verification

Public verification website for BeyBoss Tech certificates. This repository contains the static website only, not the private certificate register.

## Setup
1. In the private Google Sheet, open **Extensions → Apps Script** and add the BCVS Apps Script code supplied separately.
2. Initialize the register and review the Courses tab.
3. Deploy Apps Script as a Web app, executing as the owner and accessible to anyone. Its public endpoint must remain read-only.
4. Put the deployed `/exec` URL in `config.js` as `apiUrl`.
5. In GitHub **Settings → Pages**, select **Deploy from a branch**, branch `main`, folder `/ (root)`.
6. Set the published Pages URL as the site base URL in Apps Script.

Keep the Google Sheet private. Never put credentials, API keys, student contacts, or the register in this repository.

Certificate numbering: `BBM/COURSE/001/YY`, restarting per course and award year. Never reuse a number after revocation.

QR destinations use the published website plus the exact ID, e.g. `https://Mackachila.github.io/beyboss-certificate-verification/?id=BBM%2FPSD%2F001%2F26`. QR image generation/download is the next admin-workflow enhancement; scan-test each QR before printing.

Public result fields should be limited to student name, certificate number, course, award date, and status. Maintain independent backups. Free hosting does not guarantee perpetual availability; a BeyBoss-owned custom domain is recommended for long-term QR stability.
