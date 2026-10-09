# Booking and payment safety

Swift Drop treats a delivery quote as an input to a booking conversation, not as an
instruction to trust browser-supplied totals.

## Server-authoritative pricing

The browser can display an estimate to make the customer journey useful, but the
server recalculates the price from the submitted route, service, speed, and item data
before confirmation. This protects customers and the business from stale or modified
client-side totals.

The same principle applies to discounts, surcharges, tax treatment, and payment state:
they must be decided by trusted server logic and persisted with the booking record.

## Payment boundaries

Payment availability can depend on the current production configuration. The website
should show only payment methods that are actually enabled for the environment. A
payment provider callback must be authenticated and verified before it changes the
status of an order.

Sensitive payment details belong with the payment provider. The application should not
store raw card numbers, secret keys, webhook signing secrets, or credentials in source
control.

## Customer data

Delivery bookings can contain names, phone numbers, addresses, and shipment details.
Public documentation must not contain real customer records, order references, screen
captures with personal data, or production logs. Use synthetic examples such as
`SD-EXAMPLE` when explaining a flow.

## Safe operational checklist

Before changing a booking or payment flow:

1. Confirm the server recomputes the amount.
2. Confirm the API validates the input shape and allowed values.
3. Confirm transactional routes are not added to a public cache.
4. Confirm payment callbacks are verified and idempotent.
5. Confirm logs and test fixtures contain no customer secrets or personal data.

