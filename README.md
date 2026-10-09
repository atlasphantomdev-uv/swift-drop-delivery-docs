# Swift Drop technical documentation

Swift Drop is a UAE express-delivery platform for time-sensitive documents, parcels,
business shipments, and specialist transport requests.

The live service is available at [swiftdrop.express](https://swiftdrop.express/).
This repository is the public technical companion to the private production application.
It explains the platform's public behavior, architecture, localization, and safety
principles without publishing private source code, credentials, customer data, or
operational secrets.

## Documentation

- [Platform overview](docs/platform-overview.md) — what Swift Drop does and who it serves
- [Architecture](docs/architecture.md) — the public web architecture and rendering model
- [Bilingual routing and SEO](docs/localization-and-seo.md) — English and Arabic URL behavior
- [Booking and payment safety](docs/booking-and-payment-safety.md) — quote, booking, and payment boundaries
- [Developer quickstart](docs/developer-quickstart.md) — how to reason about changes safely
- [Frequently asked questions](docs/faq.md) — concise answers about the platform

## What this repository is—and is not

This is documentation, not the production application and not a public API client.
The production repository remains private because it contains application code,
deployment configuration, and integrations that must not be exposed.

The documentation is intentionally high-level. Exact pricing, service availability,
delivery coverage, and payment availability should always be confirmed on the live
website before being relied on.

## Documentation principles

- Describe behavior that customers can verify.
- Keep English and Arabic URL guidance consistent with the live site.
- Never publish secrets, personal information, payment credentials, or internal tokens.
- Prefer durable architecture explanations over implementation details that may change.
- Link readers to the live service when they need to book, track, or contact Swift Drop.

## Contact

For delivery questions, booking support, or business enquiries, use the
[Swift Drop contact page](https://swiftdrop.express/contact).

