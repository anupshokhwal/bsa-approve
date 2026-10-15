# bsa-approve

The approval page for the **Before She Asks** app, served by GitHub Pages at
https://anupshokhwal.github.io/bsa-approve/

The app shows a QR code (or shares a link) ending in `#<token>`. This page shows the
reminder list and lets the partner tap **Approve**; the app then shows the stamp.

- Single static file: `index.html`. No build step.
- No secrets here: it uses Supabase's public *publishable* key, and the database only acts on a valid, random, short-lived token.
- Nothing is stored by this page. The list lives in Supabase until it's approved (or skipped), at most 7 days.
- Source of truth: `approve-page/index.html` in the app repo. Copy it here when it changes.
