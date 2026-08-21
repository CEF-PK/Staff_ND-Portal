CEF Pakistan Staff Ministry Portal V25

This is an upgrade of the uploaded V24 portal. The existing login-page design is preserved.

MAJOR V25 FIXES / FEATURES

1. STAFF APPLICATION DELIVERY
- Staff signup information is also created by a Supabase Auth trigger.
- The application is created as PENDING even when email verification means there is no browser session yet.
- This prevents the common problem where a new staff member registers but the ND cannot see the application.
- Duplicate application rows are avoided by the portal.

2. STAFF / ND LOGIN ROLE FIX
- The portal no longer decides that every account in national_directors must open the ND dashboard.
- The selected login role is remembered during the authenticated session.
- A staff account can therefore open the Staff dashboard even if the same Auth account has ND access.
- The National Director tab is explicitly required for ND login.
- Logout clears the remembered role.

3. ND APPLICATIONS
- New ND registration form is available from the National Director tab.
- ND information is saved in national_director_registration_requests.
- A new ND is not automatically granted privileges.
- Existing ND can approve an ND request; approval securely adds the account to national_directors.

4. PROFESSIONAL STAFF MINISTRY PDF
- A4 portrait layout.
- CEF logo.
- Staff information.
- Staff photo when available.
- Ministry activity summary.
- Detailed report table.
- Ministry highlights / testimony.
- Staff declaration/signature area.
- Monthly, quarterly, annual and complete downloads.

5. EXCEL
- CEF logo.
- Staff Information sheet.
- Ministry Reports sheet.
- Staff Registration No., name, city, region, phone, email, designation, employment and report information.

6. CEF PROMOTION
Only CEF Promotion activities are shown:
- CEF promotional meetings
- Personal visits to promote CEF
- CEF conferences
Metrics:
- People Reached
- People Now Involved in CEF Ministry
No children reached / accepted-Jesus fields.

7. TEACHING MINISTRY
- Teacher/people training records only.
- Total People / Teachers Trained.
- Now Involved in CEF Ministry.
- No children-reached metrics.

8. BUDGETS
Staff budget now includes:
- Event location
- Participants and children expected
- Travel
- Refreshments
- Staff food
- Other CEF staff/helper and helper expense
- Other expense
- Detailed expense explanation
- Purpose / ministry plan
- Budget file upload

ND budget dashboard now provides:
- Total requested
- Pending requests
- Approved amount
- Approved budgets
- Staff information
- Detailed expenses
- Approve Full
- Approve Selected Amount / partial approval
- Reject
- A4 Budget PDF with CEF logo

9. ND MINISTRY REPORT FILTERS
ND Ministry Reports has:
- City filter (for example Faisalabad or Lahore)
- Region / Province filter (for example Punjab)
- Staff Registration No.
- Staff Name
- City
- Region
- Date
- Ministry
- Activity
- Location
- Reach / trained
- CEF involvement
Filtered Excel and A4 PDF downloads are available.

SETUP
1. Keep your existing V24 database and portal data.
2. Run V25_SETUP.sql once in Supabase SQL Editor.
3. Replace the old app.js and styles.css with the V25 files from this ZIP.
4. Keep config.js with your existing Supabase URL and anon key.
5. Hard-refresh the browser (Ctrl+F5) after replacing the files.

IMPORTANT
- Do not delete existing staff, Auth users, applications, ministry reports, budgets or ND records.
- V25 is additive and is designed to preserve existing data.


V25.1 ADDITIONS
- Staff Salary sidebar: staff can record salary month, amount received, payment date and method.
- An official A4 salary receipt is automatically generated after each salary entry, with staff information and receipt number.
- ND Staff Salaries sidebar shows all salary records with staff information and City/Region filters, plus Excel/PDF downloads.
- ND Ministry Reports now includes a Budget Report panel using the same City/Province filters, with requested/approved totals and Excel/PDF downloads.
- Prayer Meetings and CEF Promotion now use the same structured reporting questions/metrics as Teaching Ministry.
- Added light UI animations and hover transitions without changing the existing portal workflow.
- Run V25_SETUP.sql once more in Supabase SQL Editor to create the new salary table/policies.

V25.2 UPDATE – Budget, Reports & UI
- Fixed Punjab/Faisalabad filtering so Faisalabad is treated as Punjab even when an older budget record has a blank/incorrect province field.
- Improved ND budget and ministry report filtering with normalized city/province matching.
- Added downloadable budget reports for staff and ND (A4 PDF + formatted Excel).
- Added CEF logo/header to PDF reports and receipts.
- Improved staff information/photo layout in A4 ministry reports to remove unnecessary empty space.
- Staff name is automatically printed at the staff-signature area at the bottom of generated reports and salary receipts.
- Improved budget/report tables and hover/transition UI styling.
