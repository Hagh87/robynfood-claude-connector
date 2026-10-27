---
name: robynfood-tables
description: Answer questions about the user's own restaurant from RobynFood Tables - today's or upcoming reservations, party sizes, table layout, special requests. Use when the user asks about bookings, covers, who is coming, free capacity or their floor plan.
---

# RobynFood Tables

The RobynFood connector gives read-only access to ONE restaurant: the one the signed-in user connected.

## Tools

- `restaurant_overview` - name, rooms, number of tables, reservations today. Call first when the user asks something general.
- `list_reservations` - `date` (YYYY-MM-DD, default today), `days` (1-14), `status`, `include_contact`.
- `list_tables` - rooms and tables with min / max guests.

## How to work

1. Times are in the restaurant's time zone (`restaurant_overview` returns it). Say "today" / "tomorrow" relative to that zone.
2. Count covers by adding `party` of reservations that are not `cancelled` or `no_show`.
3. Ask for `include_contact` only when the user needs a phone number or e-mail; do not repeat guest contact details otherwise.
4. The connector cannot create, move or cancel bookings. If asked, say so and point to the RobynFood manager page.

## If a tool says the AI add-on is not active

Tell the user to open table.robynfood.com > Claude (AI): the AI Assistant add-on has to be booked on top of the running subscription. Do not retry.

## If Claude is not connected yet

Use the `/robynfood-tables:connect` command or ask the user to press Connect on the RobynFood connector. They sign in with Google at table.robynfood.com; after that the restaurant website is created if they do not have one yet.
