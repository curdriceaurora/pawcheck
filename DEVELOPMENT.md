# Development

This repository contains the PawCheck Chrome extension runtime and the files
needed to package a release. It does not include the original test suites,
browser automation, demo generators, or internal architecture documents.

## Requirements

- Chrome 111 or later
- Node.js 20 or later
- The `zip` command-line utility

PawCheck has no runtime or development package dependencies. You do not need
to run `npm install` to build the extension.

## Repository layout

- `src/` — Chrome extension runtime and manifest
- `src/content/` — listing panels, search badges, and page integration
- `src/popup/` — toolbar popup
- `src/shared/` — shared extraction, formatting, caching, and request logic
- `src/sites/` — site-specific adapters
- `docs/` — user-facing images referenced by the README
- `store-assets/` — Chrome Web Store artwork and screenshots
- `tools/build-zip.js` — release archive builder

## Load the extension locally

1. Open `chrome://extensions` in Chrome.
2. Enable **Developer mode**.
3. Select **Load unpacked**.
4. Choose this repository's `src/` directory.
5. After changing runtime files, select **Reload** on the PawCheck extension
   card and refresh the page being checked.

## Validate runtime JavaScript

Run Node's syntax checker across the runtime before packaging:

```sh
find src -name '*.js' -print0 | xargs -0 -n1 node --check
```

Then verify the extension manually on supported listing pages. Confirm that
the listing summary, source links, popup, theme, and optional Vrbo search
badges behave as expected.

## Build a release

```sh
npm run build
unzip -t dist/pawcheck-v1.0.0.zip
```

The builder reads the product name and version from `src/manifest.json` and
creates `dist/pawcheck-vX.Y.Z.zip`. The archive root contains the contents of
`src/`, which is the layout Chrome expects.

The `dist/` directory and ZIP archives are intentionally ignored by Git.

## Prepare a new version

1. Update `version` in `src/manifest.json`.
2. Update `version` in `package.json` to match.
3. Add the release entry to `CHANGELOG.md`.
4. Update version-specific filenames in `README.md` and this document.
5. Run the syntax check and manually verify the unpacked extension.
6. Build the archive and run `unzip -t` against it.
7. Commit the release, create the matching `vX.Y.Z` Git tag, and attach the
   ZIP archive to the GitHub release.

## Privacy-sensitive changes

Keep `PRIVACY.md` aligned with any changes to permissions, host access,
storage, or network behavior. PawCheck must not add telemetry or transmit
user browsing data without a clear product decision and an updated policy.
