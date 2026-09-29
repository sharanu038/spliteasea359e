# SplitEase – shared expense tracker (PWA)

Static web app (GitHub Pages) + Firebase Firestore for live shared groups. Includes **Simplify debts**.

## 1. Firebase (free Spark plan, ~5 min)
1. https://console.firebase.google.com → **Add project**.
2. **Build → Authentication → Get started → Sign-in method → Anonymous → Enable.**
3. **Build → Firestore Database → Create database** (production mode, nearest region).
4. Firestore → **Rules** tab → paste the contents of `firestore.rules` → **Publish**.
5. **Project settings (gear) → Your apps → Web (`</>`)** → register app → copy the `firebaseConfig` values into `config.js`.
6. **Authentication → Settings → Authorized domains → Add** `<your-github-username>.github.io`.

## 2. GitHub Pages
1. Create a new public repo, upload all files here (keep `icons/` folder), commit to `main`.
2. Repo → **Settings → Pages → Deploy from a branch → main / (root) → Save.**
3. After a minute your app is at `https://<username>.github.io/<repo>/`.

## 3. Use it
Open the link on your phone → Chrome menu → **Add to Home screen** (iPhone: Share → Add to Home Screen).
Create a group, tap **Share** and send the invite link on WhatsApp. Friends open it, pick their name, and everything syncs live.

Notes: the Firebase config in `config.js` is safe to be public. Anyone with a group's link can edit that group (link = password), so share it only with friends.
