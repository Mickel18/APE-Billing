# Inventory & Billing — Exact Check Diagnostic Center

Medical Field Operations tool for APE (annual physical exam) rosters, price lists, provider (HMO / life insurance) billing, statements of account, and print or download of statements.

The whole app is one file, `index.html`. No build step and no server are needed to open it.

## Features

- **Inventory:** company block (company, address, APE date, transmittal code, provider), patient roster with test flags, physician column when present.
- **Breakdown:** derived matrix of tests per patient with bill prices.
- **Billing:** company-billed or HMO / life-billed statements, downpayment, transmittal numbers (`YYYYMMDD-CODE-NNN`, HMO statements carry the provider code), print, and download as a standalone HTML file.
- **Archive:** each issued statement is saved as a read-only copy with its company.
- **Prices & Letterhead:** price list with added tests, provider packages (tick boxes per provider), HMO and life insurance list, logo, letterhead, e-signatures. Blocks collapse and expand.
- **Data & Storage:** import a workbook (.xlsm / .xlsx) or CSV, export and import a company as JSON, users (sign-in).
- **Print:** repeating header on every page, page numbers and "Confidential" footer.

## Run it

1. Open `index.html` in Chrome, Edge, or Firefox.
2. The first run asks you to create an administrator account.
3. The Excel reader loads from a CDN (`cdn.jsdelivr.net`), so an internet connection is needed for importing workbooks.

## Where the data lives

Everything is stored in the browser's local storage, one record per company. Nothing is sent to a server. Export a company as JSON from Data & Storage to back it up or move it to another computer.

## Sign-in: limits

The sign-in is a browser-level gate. Passwords are stored as salted PBKDF2 hashes, but the app runs entirely in the browser, so it is not secure enough for live patient records. A live deployment needs server-side accounts and a database. Keep this in mind before publishing.

## Publishing with GitHub Pages

This repository is static, so it can be published with GitHub Pages:

1. Push the repository to GitHub.
2. In the repository, open **Settings → Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**, select the `main` branch and the `/ (root)` folder, and save.
4. The site is served at `https://<your-username>.github.io/<repository-name>/`.

GitHub Pages on a free account requires a **public** repository. The repository contains the app code only and no patient data, but anything committed to a public repository is visible to everyone.

## Project files

- `index.html` — the whole application.
- `README.md` — this file.
- `.nojekyll` — tells GitHub Pages to serve files as-is.
- `.gitignore` — keeps workbooks, CSVs, PDFs, and exports out of the repository.
- `LICENSE` — Apache License 2.0.

## Licence

Licensed under the Apache License, Version 2.0. See `LICENSE`.

The licence covers the code. The clinic's name, logo, signatures, letterhead, and price list are not part of the licence grant and should not be published with a public copy.

## Privacy

Patient information is health data under the Philippines' Data Privacy Act of 2012 (RA 10173). Do not commit rosters, statements, or exports to this repository.
