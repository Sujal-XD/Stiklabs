# Stiklabs Firebase integration starter

## Files
- `firebase-config.js`: add the Firebase web app configuration from Project settings > Your apps.
- `order/index.html`: order request form using Google sign-in and Firestore.
- `firestore.rules`: restrictive starter rules; replace the admin email placeholder before publishing.
- `admin/index.html`: setup placeholder only, not a working admin dashboard.

## Add to the existing GitHub repository
Copy `firebase-config.js`, `firestore.rules`, `order/`, and `admin/` into the root of the existing repository. Do not overwrite the current homepage, `CNAME`, or logo.

## Required setup before testing
1. Replace placeholders in `firebase-config.js` using the Firebase web app config.
2. In Firebase Authentication, enable Google sign-in and add `stiklabs.tech` to authorized domains.
3. In Firestore, open Rules, replace the rules with `firestore.rules` after replacing `REPLACE_WITH_YOUR_GOOGLE_EMAIL` with the exact verified Google account email that should be the admin, then publish.
4. Commit the files to GitHub and wait for Pages deployment.
5. Test sign-in and create a test order. If an error occurs, inspect the browser console.

## Safety and current limitations
- This creates quote-request documents in Firestore only.
- The artwork field records file names only; it does not upload files.
- No payments, refunds, WhatsApp messages, slot approval UI, customer order history, or admin order management are implemented yet.
- The admin page is intentionally only a placeholder.
- Do not use live customer data until the rules are installed and tested.
- Do not put service-account credentials or private keys in the repository.
- Keep the Firebase project on Spark. Do not enable billing for this starter.
