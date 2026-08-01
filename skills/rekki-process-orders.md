---
name: Process restaurant orders from REKKI
description: Pull restaurant orders, confirm them, and report integration status back to REKKI.
api: openapi/rekki-supplier-api-openapi-original.json
operations: [ListOrdersBySupplierV4, ListNotIntegratedOrders, ConfirmOrdersV3, MarkOrdersIntegratedV4, MarkIntegrationErrorV3]
---

# Process restaurant orders from REKKI

Fetch orders placed by restaurants, acknowledge them, push them into the supplier's ERP/OMS, and report the result back (base URL `https://api.rekki.com`).

## Auth
- `Authorization: Bearer <TOKEN>`
- `X-REKKI-Authorization-Type: supplier_api_token`

## Steps
1. **Poll for orders:** call `ListOrdersBySupplierV4` (`POST /integration/v4/orders/list`) with a date/status filter body to fetch orders. To get only orders not yet pulled into your system, use `ListNotIntegratedOrders` (`POST /integration/v1/orders/list_not_integrated`).
2. **Confirm receipt:** acknowledge pending orders by reference with `ConfirmOrdersV3` (`POST /integration/v3/orders/confirm`).
3. **Integrate:** create the orders in the supplier's ERP/OMS.
4. **Report success:** call `MarkOrdersIntegratedV4` (`POST /integration/v4/orders/set_integrated`) so REKKI knows the order landed.
5. **Report failure:** if integration fails, call `MarkIntegrationErrorV3` (`POST /integration/v3/orders/set_error`) with the `error`, `product_code`/`reference`, and attempt count so it can be retried/triaged.

## Rules
- Orders are keyed by `reference`; each order carries `items[]` (with `product_code`, `quantity`, `units`) and a `customer_account_no`.
- Always close the loop: every order you pull should end in either `set_integrated` or `set_error`.
- Error envelope is `{"error": "<message>"}`; bulk calls return per-item error arrays. See `errors/rekki-problem-types.yml` and `conventions/rekki-conventions.yml`.
