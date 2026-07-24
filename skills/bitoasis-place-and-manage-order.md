---
name: Place and manage a BitOasis order
description: Check a market, place a Pro exchange order on a pair (e.g. BTC-AED), then track or cancel it.
api: openapi/bitoasis-exchange-openapi.yml
operations: [getTicker, getOrderBook, placeOrder, getOrder, getOrders, cancelOrder]
---

# Place and manage a BitOasis order

Use the BitOasis Exchange API (`https://api.bitoasis.net/v1`) to place and manage
an order. Authentication is a Bearer API token (`Authorization: Bearer <token>`),
generated at Settings > Security > Token Management. The token needs order write
permission to place/cancel and Pro Order Read Access to read.

## Steps

1. **Check the market.** Call `getTicker` for the pair (e.g. `BTC-AED`) to read the
   current price, and `getOrderBook` to see bids/asks depth. Pairs are `BASE-QUOTE`
   with a fiat quote (AED and others).
2. **Validate before executing.** Call `placeOrder` with `test=true` in the query
   string to validate the order body (`pair`, `side` buy/sell, `type`
   limit/market/stop/stop_limit, `amount`, and `price`/`stop_price` where the type
   requires them) without executing it. Fix any 400 before proceeding.
3. **Place the order.** Call `placeOrder` (no `test` flag). This moves real funds —
   confirm with the user first. Capture the returned integer order `id`.
4. **Track it.** Call `getOrder` with the `id`, or `getOrders` for the pair filtered
   by `status` (OPEN/DONE/CANCELED).
5. **Cancel if needed.** Call `cancelOrder` with `{ "id": <order_id> }` to cancel an
   open order.

## Rules

- There is no idempotency key — never blindly retry `placeOrder` on a timeout;
  reconcile with `getOrders` first to avoid duplicate orders.
- Errors are plain HTTP status codes: 400 bad body, 401 missing/insufficient token,
  404 unknown pair/order, 429 rate limited. See `errors/bitoasis-problem-types.yml`.
- Market-data reads (`getTicker`, `getOrderBook`) need no token; everything else does.
