CEF Pakistan Portal V30

NEW IN V30
1. Staff can submit Leave Applications to the National Director.
2. ND has a Leave Applications section to approve/reject requests and add notes.
3. Staff receive an in-portal notification when ND approves/rejects a leave request.
4. ND users receive a notification when a new staff leave application is submitted.
5. Staff can change their password from Settings after confirming their current password.
6. Forgot Password now opens reset.html instead of redirecting to the current localhost page.

PASSWORD RESET SETUP
A. Put the portal on its real HTTPS domain/hosting (not localhost).
B. In config.js, set SITE_URL to the public portal URL, for example:
   SITE_URL: "https://your-domain.example"
   If SITE_URL is blank, the portal automatically uses the current origin.
C. In Supabase Dashboard → Authentication → URL Configuration:
   Site URL: https://your-domain.example
   Redirect URL: https://your-domain.example/reset.html
D. If you use a different hosting path, add that exact reset.html URL to Supabase Redirect URLs.

DATABASE
Run V30_SETUP.sql once in Supabase SQL Editor after your existing setup scripts.

SECURITY
Leave applications are protected by RLS: staff can create/read only their own requests; only National Directors can review all requests and change status.
