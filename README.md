# Ideas in the Clouds — GitHub Pages + Firebase

A small bilingual (English/Korean) site. Visitors choose one of five social issues and submit **only the idea text**. Submissions are stored in Cloud Firestore and displayed as floating cloud bubbles for everyone. Default language is English.

## Files

- `index.html` — the whole front end
- `firestore.rules` — recommended Firestore security rules

## 1. Set up Firebase

1. Open [Firebase Console](https://console.firebase.google.com/) and create a project.
2. Add a **Web app** to the project and copy its Firebase config.
3. Go to **Build → Firestore Database** and create a database.
4. In Firestore **Rules**, paste the contents of `firestore.rules` and publish.
5. In `index.html`, replace the four `YOUR_...` values in `firebaseConfig` with your actual web app values:
   - `apiKey`
   - `authDomain`
   - `projectId`
   - `appId`

Firebase web config is intended to be included in a client-side app. The security rules—not secrecy of the config—control database access.

## 2. Publish with GitHub Pages

1. Create a GitHub repository, for example `ideas-in-the-clouds`.
2. Upload `index.html`, `firestore.rules`, and this README to the repository root.
3. In the repository, open **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Select the `main` branch and `/ (root)`, then save.
6. Wait for GitHub Pages to publish and open the displayed site URL.

## Important notes

- The site defaults to English. The top-right button switches between English and Korean.
- Visitors do not enter names or other profile details. Only the selected category and idea text are saved.
- Ideas are public. Do not invite visitors to share personal, private, or identifying information.
- The included rules prevent edits/deletions and restrict the shape and length of new entries, but they do **not** prevent spam or automated submissions. For a public or widely shared site, add App Check and/or a moderation/approval workflow, and monitor Firebase usage and billing.
- The background shows the latest 45 submissions. The clouds are decorative; they are not a word cloud or a ranking.
- If the database has no entries yet, the cloud background will remain empty until visitors submit ideas.
