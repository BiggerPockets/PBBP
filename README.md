# PBBP Widget Test Pages

Test pages for the [Powered by BiggerPockets (PBBP)](https://biggerpockets.atlassian.net/wiki/spaces/Product/pages/402391041/PBBP+-+OfferSheet+Lender+Marketplace) embeddable widgets, hosted on GitHub Pages at an external domain to verify cross-origin functionality.

## Live URL

https://biggerpockets.github.io/PBBP/

## Purpose

The PBBP widgets are embedded on partner sites via iframe. Since they enforce domain allowlisting, we need a non-BiggerPockets domain to test the full embed experience. This repo provides that via GitHub Pages.

## Setup

1. The partner's allowed domains must include `biggerpockets.github.io` in the [PBBP Partners admin panel](https://www.biggerpockets.com/admin/pbbp_partners).
2. The PBBP feature flag (`2026_02:marketplace:pbbp`) must be enabled.
3. The partner record must exist and be enabled with a valid slug.

## Current Test Pages

- **`index.html`** — Lender Finder widget for Offer Sheet (`the-offer-sheet`), defaulting to Short-Term Rental strategy

## Adding a New Test Page

1. Create an HTML file with the widget embed snippet:
   ```html
   <script
     src="https://www.biggerpockets.com/lender-finder.js"
     data-partner-id="partner-slug"
   ></script>
   ```
2. Commit and push to `main` — GitHub Pages deploys automatically.
3. Ensure the partner's allowed domains include `biggerpockets.github.io`.

## Available Widgets

| Widget | Script URL |
| --- | --- |
| Agent Finder | `https://www.biggerpockets.com/agent-finder.js` |
| Lender Finder | `https://www.biggerpockets.com/lender-finder.js` |
| Property Manager Finder | `https://www.biggerpockets.com/property-manager-finder.js` |

## Related Resources

- [Partner Onboarding Runbook (Internal)](https://biggerpockets.atlassian.net/wiki/spaces/Product/pages/443416588/PBBP+-+Partner+Onboarding+Runbook+Internal)
- [Offer Sheet Installation Guide](https://biggerpockets.atlassian.net/wiki/spaces/Product/pages/443973633/Offer+Sheet+-+Lender+Finder+Widget+Installation+Guide)
