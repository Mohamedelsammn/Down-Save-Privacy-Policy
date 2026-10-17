# Downsave legal website

Static, dependency-free pages for the Downsave Android app. Target URL: <https://mohamedelsammn.github.io/Down-Save-Privacy-Policy/>.

## Status

**Publication candidate.** The privacy page states the owner's confirmed data practices and explicitly discloses unknown infrastructure and provider practices without promising that they retain no data. The official support email is `mohamed.elsamman.dev@gmail.com`. Backend and provider retention still need confirmation for accurate Google Play Data Safety answers.

## Structure

- `index.html` — home
- `privacy/index.html` — privacy policy
- `terms/index.html` — terms and conditions
- `contact/index.html` — contact
- `assets/site.css` — shared responsive styles
- `assets/favicon.svg` — icon

All internal links are relative to the current page, so they work under the GitHub Pages project subpath. Each legal route is a real directory with an `index.html`, allowing direct navigation and refresh.

## Operational follow-up

1. Confirm current access/error logs and IP-address handling, temporary processing or caches, provider URL and metadata retention or sharing, hosting-provider role, retention periods, and deletion mechanisms. Update the policy if the answers differ from its current disclosures.
2. Reconcile confirmed practices with Google Play Data Safety, including whether provider processing counts as sharing. Do not claim a server-side deletion period until one is verified.
3. Verify the support email is still correct. To change it, replace every occurrence of `mohamed.elsamman.dev@gmail.com` in the HTML pages.
4. In repository **Settings → Pages → Build and deployment**, set **Source** to **GitHub Actions**. Commits to `main` trigger the workflow and future redeployments.
5. Check the Actions run and all four public URLs over HTTPS before adding them to the app or Play Console.

## Local preview

Open `index.html` in a browser, or serve this directory with any local static file server. No package installation or build is required.

## Source of app behavior

The site was checked against the local Downsave Flutter app and `doc/GOOGLE_PLAY_RELEASE_AUDIT.md` dated 15 October 2026. The app posts a submitted URL plus selected quality or format to `/resolve` on its configured HTTPS backend. The library index and settings use on-device preferences, and downloaded files use device storage. The release audit reports no analytics or advertising SDK. The owner reports no intentional application-database storage of submitted URLs or server-side media storage. Current infrastructure and external-provider retention are not verified. The backend implementation is outside this repository.
