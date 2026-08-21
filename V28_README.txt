CEF Pakistan Portal V28

Changes in V28
- Fixed downloadable report PDF header so the dedicated CEF report logo is visibly embedded.
- Removed the ministry picture/banner from the portal and report design.
- Replaced the banner with the CEF mission statement: "To evangelise every child."
- Added a National Director "Report Deadline" section.
- ND can set/send the monthly report deadline and an instruction message.
- Staff see the current deadline on their dashboard with remaining-days, due-today, or overdue status.
- The deadline recurs monthly using the configured deadline day; the default is the 25th.
- Saving a deadline sends a portal notification to approved staff.

Database
Run V25_SETUP.sql once in Supabase. It contains the V28 report_deadline_settings table, policies, default 25th deadline, and indexes.
