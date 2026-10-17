# Downsave legal website

Static, dependency-free pages for the Downsave Android app. Target URL: <https://mohamedelsammn.github.io/Down-Save-Privacy-Policy/>.

## Status

**Redesigned-app content draft (local branch only).** The public site still describes the previous app. The only Flutter source currently available beside this website is the old downloader implementation, so the new import, editing, permissions, storage, and Clear Data claims are awaiting code verification. The deployment workflow blocks the draft legal pages. The confirmed support email remains `mohamed.elsamman.dev@gmail.com`.

## Structure

- `index.html` — home
- `privacy/index.html` — privacy policy
- `terms/index.html` — terms and conditions
- `contact/index.html` — contact
- `assets/site.css` — shared responsive styles
- `assets/favicon.svg` — icon

All internal links are relative to the current page, so they work under the GitHub Pages project subpath. Each legal route is a real directory with an `index.html`, allowing direct navigation and refresh.

## Before publishing the redesigned policy

1. Obtain the path, repository, branch, or build artifacts for the redesigned Flutter app.
2. Verify exact import and editing functions, permissions, local file behavior, deletion and Clear Data semantics, network calls, and SDKs.
3. Replace the draft verification notes with confirmed practices and set the genuine effective date on publication day.
4. Merge the reviewed content into `main`, then verify the GitHub Actions deployment and all four public URLs.

## Local preview

Open `index.html` in a browser, or serve this directory with any local static file server. No package installation or build is required.

## Source of app behavior

The owner supplied the redesigned feature summary. The Flutter tree at `D:/creative_hub/DownSave/app/downsave` still contains the prior URL downloader and does not substantiate the new import and editing flows. No claim about those flows should be published as verified until the redesigned source is available. The published `main` site remains unchanged while this draft branch is reviewed.
