CEF Pakistan Portal V26.1

Changes:
- Fixed Punjab/Faisalabad filtering so Faisalabad is correctly treated as part of Punjab even when the saved budget province is blank or inconsistent.
- Improved staff information block in A4 ministry reports: staff photo and information now share a compact full-width profile card without the previous empty space.
- CEF logo and ministry banner are used across downloadable report designs.
- Staff name is automatically printed in the staff signature/declaration area of staff-generated A4 reports.
- Budget downloads are available from both Staff and ND Downloads pages as well as the budget pages.
- Added salary fields: Paid By and Bank Name.
- Salary receipts and ND salary reports include Paid By and Bank information.
- Added ministry banner beautification to report/download pages.

Database:
Run V25_SETUP.sql once after the update. It is safe to rerun because the new salary fields use IF NOT EXISTS.
