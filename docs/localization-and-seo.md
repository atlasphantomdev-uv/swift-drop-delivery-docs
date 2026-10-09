# Bilingual routing and SEO

Swift Drop serves the UAE in English and Arabic. The public URL structure makes the
language explicit so that customers, crawlers, and assistive technologies can identify
the intended version of a page.

## URL rules

| Language | Example | URL prefix |
| --- | --- | --- |
| English | Services | `/services` |
| Arabic | Services | `/ar/services` |
| English home | Home | `/` |
| Arabic home | Home | `/ar` |

There is no public `/en` version. Internal route names are not public URLs.

## Discovery signals

The production site maintains the following signals for indexable public pages:

- A self-referencing canonical URL for each language version.
- Reciprocal English and Arabic `hreflang` alternatives where a translation exists.
- A sitemap generated from the site's single route registry.
- Robots rules that keep private and transactional paths out of ordinary crawling.
- Server-rendered page content so the primary copy is available without client interaction.

These signals help search engines understand the site, but they do not guarantee a
ranking. Useful, accurate pages and genuine references from relevant websites remain
the foundation of search visibility.

## Content rules

Public documentation and website copy should:

- Use natural delivery terminology for UAE customers.
- Keep claims about prices, coverage, timing, and payment availability verifiable.
- Avoid duplicating one thin page for every location and keyword combination.
- Keep Arabic content natively readable rather than relying on a URL-only translation.
- Link to the live booking and contact journeys when the reader needs to act.

## Canonical references

The live site is the source of truth for current service availability and customer
actions:

- [Swift Drop home](https://swiftdrop.express/)
- [Delivery services](https://swiftdrop.express/services)
- [Pricing](https://swiftdrop.express/pricing)
- [Coverage](https://swiftdrop.express/coverage)
- [Contact](https://swiftdrop.express/contact)

