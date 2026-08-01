---
name: Sync a supplier catalog to REKKI
description: Publish and maintain a supplier's product catalog, inventory, and pricing on REKKI.
api: openapi/rekki-supplier-api-openapi-original.json
operations: [ReplaceCatalogV3, UpdateCatalogItemsV3, GetCatalogItemsV3, GetCatalogItemV3, DeleteCatalogItemsV3, UpdateCatalogInventory, UpdatePriceList, UpdateCatalogItemAvailabilityV3]
---

# Sync a supplier catalog to REKKI

Keep a supplier's catalog, stock, and prices current on REKKI (base URL `https://api.rekki.com`, base path `/api`).

## Auth
Every request needs two headers:
- `Authorization: Bearer <TOKEN>`
- `X-REKKI-Authorization-Type: supplier_api_token`

Request a token from integrations@rekki.com. A missing/invalid token returns `401`.

## Steps
1. **Full load (first sync):** call `ReplaceCatalogV3` (`POST /integration/v3/catalog/replace`) to drop all existing items and upload the complete catalog. Use this for the initial import or a full re-sync.
2. **Incremental upserts:** call `UpdateCatalogItemsV3` (`POST /integration/v3/catalog/items`) to create or update items by `product_code`. Prefer this for ongoing changes rather than repeated full replaces.
3. **Verify:** read back with `GetCatalogItemsV3` (`GET /integration/v3/catalog/items`) or a single item with `GetCatalogItemV3` (`GET /integration/v3/catalog/items/{id}`).
4. **Stock:** push availability with `UpdateCatalogInventory` (`POST /integration/v3/catalog/inventory`) or toggle a single item with `UpdateCatalogItemAvailabilityV3`.
5. **Pricing:** update prices with `UpdatePriceList` (`POST /integration/v3/catalog/pricelist`).
6. **Removals:** delete discontinued items with `DeleteCatalogItemsV3` (`POST /integration/v3/catalog/items/delete`).

## Rules
- Items are keyed by `product_code`; reuse it across updates so you upsert rather than duplicate.
- There is no idempotency-key header — `ReplaceCatalogV3` is a destructive full overwrite, so only use it when you truly have the complete catalog.
- Errors come back as `{"error": "<message>"}` with a `400`/`500` status; see `errors/rekki-problem-types.yml`.
