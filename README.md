# NearbyUPI — Privacy Policy page

Standalone page for the Play Store listing ("Privacy policy" URL).
`index.html` is fully self-contained (no build step, no dependencies).

## Free hosting — pick ONE (easiest first)

### Option A — GitHub Pages (recommended)
1. Create a GitHub account if you don't have one, then a new **public** repo
   named e.g. `nearbyupi-privacy-policy`.
2. Upload this folder's `index.html` to the repo (Add file → Upload files).
3. Repo → Settings → Pages → Source: `main` branch, `/ (root)` → Save.
4. In ~1 minute your URL is live:
   `https://<your-username>.github.io/nearbyupi-privacy-policy/`

### Option B — Firebase Hosting (you already have the Firebase project)
```bash
npm i -g firebase-tools
firebase login
firebase init hosting      # use an EXISTING project, public dir = this folder
firebase deploy
```
URL: `https://<project-id>.web.app`

### Option C — Netlify Drop (zero account friction)
Open <https://app.netlify.com/drop>, drag this folder onto the page.
URL: `https://<random-name>.netlify.app` (renamable).

### Option D — Cloudflare Pages
Dashboard → Workers & Pages → Create → Pages → Upload assets, drag folder.
URL: `https://<project>.pages.dev`

## After hosting
1. Copy your live URL.
2. Update `PRIVACY_POLICY_URL` in
   `app/src/main/java/com/nearbyupi/app/AppLinks.kt`.
3. Rebuild (`./gradlew assembleRelease bundleRelease`) — done.
   (That constant is wired into the in-app Terms sheet.)
