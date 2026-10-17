# Downsave legal website

Static, dependency-free pages for the Downsave Android app. Target URL: <https://mohamedelsammn.github.io/Down-Save-Privacy-Policy/>.

## Status

**Legal draft — do not publish yet.** The privacy policy distinguishes the owner's report of no intentional application-database URL storage or server-side media storage from unverified logging, IP handling, temporary caching, provider retention, and deletion. The deployment workflow refuses to publish while draft markers remain. The official contact email supplied by the app owner is `mohamed.elsamman.dev@gmail.com`.

## Structure

- `index.html` — home
- `privacy/index.html` — privacy policy
- `terms/index.html` — terms and conditions
- `contact/index.html` — contact
- `assets/site.css` — shared responsive styles
- `assets/favicon.svg` — icon

All internal links are relative to the current page, so they work under the GitHub Pages project subpath. Each legal route is a real directory with an `index.html`, allowing direct navigation and refresh.

## Before publication

1. Obtain production backend and third-party provider answers: current access/error logs and IP-address handling; whether the documented 120-second request-coalescing cache is active and what it holds; provider URL and metadata retention or sharing; hosting-provider role; retention periods; and deletion mechanisms.
2. Reconcile those answers with the privacy policy and Google Play Data Safety declaration, including whether provider processing counts as sharing. Remove draft notices only after the text is accurate. Set a genuine effective date on the publication day.
3. Verify the support email is still correct. To change it, replace every occurrence of `mohamed.elsamman.dev@gmail.com` in the HTML pages.
4. In repository **Settings → Pages → Build and deployment**, set **Source** to **GitHub Actions**. Push the finalized site to `main`; the workflow will deploy it and redeploy on future commits.
5. Check the Actions run and all four public URLs over HTTPS before adding them to the app or Play Console.

## Local preview

Open `index.html` in a browser, or serve this directory with any local static file server. No package installation or build is required.

## Source of app behavior

The draft was checked against the local Downsave Flutter app and `doc/GOOGLE_PLAY_RELEASE_AUDIT.md` dated 15 October 2026. The app posts a submitted URL plus selected quality or format to `/resolve` on its configured HTTPS backend. The library index and settings use on-device preferences, and downloaded files use device storage. The release audit reports no analytics or advertising SDK. The owner reports no intentional application-database storage of submitted URLs or server-side media storage. Older implementation notes in `doc/Implementation Plan.md` describe a 120-second request-coalescing cache; current production behavior has not been verified. The backend implementation is outside this repository.
