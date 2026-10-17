# Downsave legal website

Static, dependency-free pages for the Downsave Android app. Target URL: <https://mohamedelsammn.github.io/Down-Save-Privacy-Policy/>.

## Status

**Redesigned website published on GitHub Pages.** The Privacy Policy and Terms remain visibly marked as drafts pending implementation review. They describe the owner-supplied feature summary and qualify unverified data handling rather than claiming it is confirmed. The support email is `mohamed.elsamman.dev@gmail.com`.

## Structure

- `index.html` — home
- `privacy/index.html` — privacy policy
- `terms/index.html` — terms and conditions
- `contact/index.html` — contact
- `assets/site.css` — shared responsive styles
- `assets/favicon.svg` — icon

All internal links are relative to the current page, so they work under the GitHub Pages project subpath. Each legal route is a real directory with an `index.html`, allowing direct navigation and refresh.

## Further verification

1. Obtain the path, repository, branch, or build artifacts for the redesigned Flutter app.
2. Verify exact import and editing functions, permissions, local file behavior, deletion and Clear Data semantics, network calls, and SDKs.
3. Replace the draft notices with confirmed practices and set a genuine effective date when the policies are finalized.
4. Keep the public policy aligned with later app changes and verify each GitHub Actions deployment.

## Local preview

Open `index.html` in a browser, or serve this directory with any local static file server. No package installation or build is required.

## Source of app behavior

The owner supplied the redesigned feature summary. The Flutter tree at `D:/creative_hub/DownSave/app/downsave` still contains the prior URL downloader and does not substantiate the new import and editing flows. The published pages retain draft notices and do not present those flows as verified implementation details.
