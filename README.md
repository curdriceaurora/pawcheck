# PawCheck: Dog Policy Callout

PawCheck is a Chrome extension that finds dog-policy details on Vrbo, Airbnb,
and Expedia listings and presents them in a compact summary.

## Features

- Shows whether dogs are allowed.
- Extracts dog-count and weight limits, fees, deposits, and approval rules.
- Links each value back to its source text when possible.
- Warns when listing sections contain contradictory rules.
- Adds optional policy badges to Vrbo search results.
- Stores settings and a short-lived policy cache locally in Chrome.
- Follows the operating system's light or dark theme.

## Install a release

1. Download `pawcheck-v1.0.0.zip` from
   [GitHub Releases](https://github.com/curdriceaurora/pawcheck/releases).
2. Unzip the archive.
3. Open `chrome://extensions` in Chrome.
4. Enable **Developer mode**.
5. Select **Load unpacked** and choose the unzipped folder.

## Supported pages

PawCheck supports property listing pages on Vrbo, Airbnb, and Expedia. Search
result badges are available on Vrbo and are disabled by default.

PawCheck is independent software and is not affiliated with or endorsed by
Vrbo, Airbnb, Expedia, or their parent companies. Always verify the original
property rules before booking.

- [Release notes](CHANGELOG.md)
- [Development guide](DEVELOPMENT.md)
- [Privacy policy](PRIVACY.md)
- [MIT license](LICENSE)
