Allam Veterinary Clinic — Clean starter

Files in this folder:
- schema.sql: run in Supabase SQL Editor
- index.html: home page (owner + animal + examination + treatment form)
- search.html: separate search/history page
- styles.css: shared styling

Supabase setup:
1) Open the Supabase project you intend to use.
2) Go to SQL Editor > New query, paste the full contents of schema.sql, then Run.
3) In Authentication settings, disable public sign-ups. Create/keep only trusted clinic user accounts.
4) Ensure the login user exists in Authentication > Users. The website signs in with that user's email and password.
5) If using a different Supabase project, replace SUPABASE_URL and SUPABASE_KEY in BOTH index.html and search.html with that project's Project URL and publishable key.

GitHub Pages setup:
1) Download and extract all files from this ZIP.
2) In the repository mesho2/Allam-vet-clinic-, upload index.html, search.html, and styles.css directly to the repository root (not inside an extra folder).
3) Commit changes and wait for GitHub Pages to publish.
4) Open https://mesho2.github.io/Allam-vet-clinic-/ . Search page: https://mesho2.github.io/Allam-vet-clinic-/search.html

Notes:
- The code uses the previously supplied Supabase project URL and publishable key.
- Never put a service_role/secret key in browser code.
- This schema uses new clinic_* table names and does not drop old tables.
- The form currently saves a new owner, animal, visit, and its medicines as one workflow. For repeat visits to an existing animal, the next refinement should add an explicit “select existing owner/animal” flow to avoid duplicate profiles.
