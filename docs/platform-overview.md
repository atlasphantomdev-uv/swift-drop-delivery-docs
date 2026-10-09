# Swift Drop platform overview

Swift Drop is an express-delivery service in the United Arab Emirates. The platform
connects customers and businesses with delivery options for documents, parcels,
fragile items, medical transport, and other approved specialist requests.

The customer-facing experience is designed around four jobs:

1. Understand which delivery service fits the shipment.
2. Get a clear delivery quote based on the route, item, and requested speed.
3. Place a booking with the required collection and destination information.
4. Track the order and contact support when help is needed.

The service supports deliveries across the UAE. Availability, route timing, item
eligibility, and final pricing depend on the booking details and current operational
capacity; the website is the source of truth for a live request.

## Public customer journeys

### Get a quote

The quote flow collects the pickup location, destination, item type, and delivery
speed. The resulting price is calculated from the booking details rather than being
treated as a value supplied by the browser.

### Book a delivery

The booking flow collects the information needed to arrange collection and delivery.
Customers should provide accurate contact and address details so the delivery team can
coordinate the request.

### Track an order

Customers can use the tracking experience with their order reference. Tracking data is
request-time information and is handled separately from cacheable marketing content.

### Business delivery

Businesses can request a tailored rate for recurring or higher-volume delivery needs.
The business flow is a lead and pricing conversation, not a promise of an automatically
approved account or fixed commercial terms.

## Service language

Swift Drop serves English-speaking and Arabic-speaking customers. Service descriptions
should be read together with the live English or Arabic page because operational
details and availability can change.

