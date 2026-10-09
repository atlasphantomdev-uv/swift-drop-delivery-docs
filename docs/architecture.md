# Swift Drop web architecture

The production website is a server-rendered Next.js application with a bilingual public
URL contract. The private application uses TypeScript, React, Tailwind CSS, Prisma,
Postgres, and managed deployment infrastructure.

This document describes the architectural boundaries that matter to integrators and
contributors. It does not publish the private application source or deployment secrets.

## Public URL model

English pages use the root public path:

```text
https://swiftdrop.express/
https://swiftdrop.express/services
https://swiftdrop.express/pricing
```

Arabic pages use the `/ar` prefix:

```text
https://swiftdrop.express/ar
https://swiftdrop.express/ar/services
https://swiftdrop.express/ar/pricing
```

The public URLs are the canonical contract. Internal framework directories are an
implementation detail and should never be linked to by external documentation.

## Rendering boundaries

The site separates stable public content from request-time data:

- Marketing, pricing, service, coverage, and route pages can be prerendered.
- Booking, checkout, payment, lead, chat, rating, and tracking operations remain dynamic.
- Order and payment information is never treated as ordinary cacheable marketing content.
- Blog data can be cached for a short period and invalidated when content is published.

This boundary protects customer-specific information while allowing public service
pages to load efficiently and be crawled by search engines.

## Data and integrations

The production application uses a Postgres-backed data layer for operational records.
Payment processing is provider-backed and server-authoritative. Hosting, analytics,
messaging, storage, and payment integrations are configured through environment
variables and managed services; credentials are not stored in this repository.

## Failure boundaries

The website should fail safely when an optional integration is unavailable:

- A marketing page should not expose a database credential or stack trace.
- A quote should be recomputed on the server before a booking is confirmed.
- A payment callback must be verified before it changes order state.
- A tracking lookup must not be cached as if it were static content.

