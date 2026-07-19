# Functions Exploration V8 Professional

## Key features
- 100 syllabus-aligned questions.
- Strict duplicate-option validation.
- 15 random questions per attempt.
- Real-time class monitor through Firebase Firestore.
- Cloud leaderboard.
- CSV export.
- Local fallback mode when Firebase is not configured.

## Firebase setup
1. Create a Firebase project.
2. Create a Web App.
3. Enable Firestore Database.
4. Copy the Firebase web configuration into `firebase-config.js`.
5. Paste the content of `firestore.rules` into Firestore Rules and publish.
6. Upload `index.html` and `firebase-config.js` to GitHub Pages, Netlify, Cloudflare Pages, or Firebase Hosting.

## Important security note
The included Firestore rules are intentionally open for a classroom prototype.
Before long-term public deployment, add Firebase Authentication and restrict teacher-only delete access.

## Duplicate-option protection
The game runs a strict audit during startup. Every question must have exactly four unique answer options.
If a duplicate remains, the game throws a clear error identifying the question ID instead of showing an ambiguous question.
