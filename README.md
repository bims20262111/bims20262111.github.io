# Minimal Ideas in the Clouds

A simple black-and-white HTML site with English/Korean language switching and Firebase Firestore support.

## Setup
1. Create a Firebase project at https://console.firebase.google.com/
2. Add a web app and create a Cloud Firestore database.
3. Publish the contents of `firestore.rules` in Firestore > Rules.
4. Replace the placeholder values in `index.html` under `firebaseConfig` with your Firebase web app config.
5. Upload `index.html` and `firestore.rules` to the root of a GitHub repository.
6. Open Settings > Pages, choose Deploy from a branch, then select `main` and `/(root)`.

Submissions are public. This starter has basic shape/length validation but no spam prevention or moderation. For a public site, consider Firebase App Check and moderation.
