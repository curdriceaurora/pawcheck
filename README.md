# PawCheck: Dog Policy Callout

PawCheck finds dog-policy information in Vrbo, Airbnb, and Expedia listings.
It shows this information in a compact summary beside the property.

![PawCheck — dog policy details, right where you need them](store-assets/marquee-promo-tile-1400x560.png)

## Why

Booking sites do not show pet policies in a consistent location. Hosts can
put restrictions in house rules, amenities, property descriptions, policy
sections, or structured page data. One listing can contain conflicting rules.

A pet-friendly property can still limit dog count, weight, or breed. It can
also require fees or prior approval. PawCheck collects these details for you.

## What PawCheck shows

When you open a supported listing, PawCheck reads the available pet-policy
data. It shows a summary that contains:

- Whether dogs are allowed
- Maximum dog count and weight limits
- Pet fees and refundable deposits
- Registration or prior-approval requirements
- Other guidelines, including leash or breed restrictions

When possible, source links open the applicable listing text. PawCheck
identifies conflicting rules. It supports light and dark themes. It can also
add optional dog-policy badges to Vrbo search results.

The quantity of available policy information is different for each listing.
PawCheck shows only the available information.

![Sparse, medium, and dense PawCheck policy summaries in light mode](store-assets/screenshot-light-density-comparison-1280x800.png)

## Listing examples

### Vrbo listing

![PawCheck on a Vrbo listing](docs/listing-gifs/vrbo-9793597ha.gif)

### Vrbo search results

![PawCheck badges on Vrbo search results](docs/listing-gifs/vrbo-search-navarre.gif)

Search badges are experimental. The setting is off by default. Search badging
makes more property-page requests than standard browsing. PawCheck limits
concurrent requests, sets a session limit, caches results, and increases the
delay after errors or challenges. These controls reduce traffic, but they do
not remove the risk. Vrbo can throttle or challenge your browser. Enable this
feature only when necessary. Disable it when you finish.

To enable search badges:

1. Open PawCheck from the Chrome toolbar.
2. Turn on **Enable search listings badges**.

When this setting is on, PawCheck requests public property pages directly
from Vrbo. PawCheck uses these pages to summarize each listing's dog policy.

### Airbnb

![PawCheck in light mode on an Airbnb listing](store-assets/screenshot-4-airbnb-light-1280x800.png)

### Expedia

![PawCheck in light mode on an Expedia listing](store-assets/screenshot-5-expedia-light-1280x800.png)

## Install a release

1. Download the latest `pawcheck-v*.zip` from
   [GitHub Releases](https://github.com/curdriceaurora/pawcheck/releases/latest).
2. Unzip the archive.
3. Open `chrome://extensions` in Chrome.
4. Enable **Developer mode**.
5. Select **Load unpacked**.
6. Choose the unzipped folder.

## Supported pages

PawCheck supports property listing pages on Vrbo, Airbnb, and Expedia. Search
badges are available only on Vrbo.

PawCheck is independent software. PawCheck has no affiliation with Vrbo,
Airbnb, Expedia, or their parent companies. These companies do not endorse
PawCheck. Always verify the original property rules before you book.

- [Release notes](CHANGELOG.md)
- [Development guide](DEVELOPMENT.md)
- [Privacy policy](PRIVACY.md)
- [MIT license](LICENSE)
