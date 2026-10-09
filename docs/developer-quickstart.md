# Developer quickstart

This repository contains public documentation only. It does not boot the private
production application and it does not require database, payment, analytics, or cloud
credentials.

## Read first

Start with:

1. [Platform overview](platform-overview.md)
2. [Architecture](architecture.md)
3. [Bilingual routing and SEO](localization-and-seo.md)
4. [Booking and payment safety](booking-and-payment-safety.md)

## Documentation changes

Use plain Markdown and keep each page focused on one topic. Before opening a pull
request:

- Check all links.
- Remove secrets, personal information, internal hostnames, and private identifiers.
- Mark examples as examples.
- Confirm claims about the live service against [swiftdrop.express](https://swiftdrop.express/).
- Keep English and Arabic URL examples consistent with the public routing rules.

## Private application changes

Changes to the production application belong in the private application repository.
Before shipping an application change, the project verification gates include TypeScript
checking, SSR/hydration linting, a production build, report verification, and the
appropriate English and Arabic route checks.

This public repository should receive a documentation update only when the public
behavior or supported architecture has actually changed.

