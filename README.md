# CEF Pakistan Portal V19

## What changed

- Preserves the Version 17/18 login page design.
- GNC Add screen shows only GNC activities:
  - Regular GNC
  - Live Online GNC
  - School GNC
  - Preschool GNC
  - Church-Related GNC
  - GNC Started from CPC
  - Children Attending Church
  - Subtotal GNC (calculated summary, not a separate ministry record)
- 5-Day Club Add screen shows only 5-Day Club activities and a calculated Subtotal 5DC.
- Party Clubs and Evangelism & Outreach remain separated into their own sections.
- Teaching Ministry is teacher-focused: teachers trained and teachers involved in CEF ministry. Child-reach fields are not shown there.
- Training records are displayed inside Teaching Ministry; there is no separate Training Records navigation item.
- Detailed budget/application form includes event location, participants, children, travel, refreshments, helper CEF staff name/expense, other expenses, detailed expense explanation, purpose, and optional budget file upload.
- Staff downloads now include Excel (.xlsx) and PDF reports with staff information and the CEF logo.
- National Director authorization no longer queries a non-existent `email` column in `national_directors`; it checks `auth_user_id` only.
- ND budget review can view detailed expenses and securely open uploaded budget files.

## Setup

1. Keep the same `config.js` Supabase URL and anon/public key used by your working portal.
2. Run `V16_SETUP.sql` if the ministry tables have never been created.
3. Run `V18_MINISTRY_UPGRADE.sql` if it has not already been run.
4. Run `V19_SETUP.sql` once.
5. Do not use the Supabase service-role key in the browser.

The login page is intentionally preserved. The changes are inside the Staff and National Director portals.

V30 additions: Staff Leave Applications, ND Leave Review, secure password change/reset page, and Supabase redirect configuration notes. Run V30_SETUP.sql once.
