CEF Pakistan Portal V34

Changes:
- Staff registration training selections are saved by the Supabase Auth signup trigger.
- Staff cannot access the portal until ND approval.
- Rejected and deleted staff are blocked from portal access.
- ND can safely delete/deactivate approved staff from Staff Applications or Staff Directory. Historical ministry, budget and salary records remain for ND records.
- ND signature included at assets/nd-signature.png and embedded as a PDF fallback.
- Staff application PDF includes training/qualifications and ND approval signature.

Run V34_SETUP.sql once in Supabase SQL Editor.
