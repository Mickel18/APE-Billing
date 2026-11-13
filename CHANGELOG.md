Changes since the last upload:

Billing
- Two billing types: Company-Billed and HMO-Billed.
- Per-patient HMO (member) and Company tick boxes. Members' package tests
  go to the HMO statement; members' other tests and all non-members' tests
  go to the company statement.
- Select-all tick boxes above the HMO and Company columns.
- Serial-number ranges to set HMO members and non-members in one step.
- Serial numbers are stored per patient, so they stay fixed when rows are
  deleted. New patients (late attendees) take the next number.
- Provider is set once per company (company block on the Inventory tab).
- Provider packages are set per provider with tick boxes. Default is
  Basic 5, ECG and Pap Smear.
- Separate transmittal sequences for company-billed statements and for each
  HMO (for example 20260709-CHEM-MAXI-001).
- Statement archive: each issued statement is saved as a read-only copy
  with View, Download and print options.
- Download statement as a standalone HTML file.
- Statement layout: repeating header on each page, Confidential and page
  numbers in the footer, signature sizes per signatory.

Inventory and prices
- Company block redesigned: company, address and APE date on the left;
  transmittal code and provider on the right.
- HMO and life insurance list with 38 providers, editable table (add, rename,
  remove). Renaming updates patients and packages.
- Add tests in the price list (flag code, name, price); remove tests you added.
- Price list, provider packages, provider list, letterhead, logo and
  e-signature blocks collapse and expand; the state is remembered.

Appearance
- Sidebar in green (#96C93D) with the clinic name and department.
- Logo and e-signature images are trimmed automatically, with transparent
  backgrounds.

Access
- Sign-in screen with administrator creation on first run.
- Users can be added or removed, and passwords changed, from Data & Storage.
- Passwords are stored as salted PBKDF2 hashes.

Notes
- The sign-in is a browser-level gate. It is not secure enough for live
  patient records. A server version with a database is needed for live use.
- Data remains in each browser until a server version is added.
