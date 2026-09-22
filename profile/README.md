## EmailCheckPro

**Real-time email deliverability and email avatar checks.**

Submit one email address and get its deliverability result in the same HTTP response. Works on any domain, from Gmail to a company's own. Up to 100 addresses per synchronous request. Whole lists go through the bulk task API.

[**Website**](https://emailcheckpro.com) · [**API documentation**](https://emailcheckpro.com/api-docs) · [**Pricing**](https://emailcheckpro.com/pricing) · [**Get an API key**](https://emailcheckpro.com/register)

### Official API example repositories

One repository per product, each mirroring its own product page.

| Repository | Shape | Product code | Contents |
|---|---|---|---|
| **[Email Deliverability Check](https://github.com/emailcheckpro/email-deliverability-checker-api)** | Realtime | `email` | OpenAPI contract, `product.json`, `llms.txt`, examples in 7 languages |
| **[Email Avatar Check](https://github.com/emailcheckpro/email-avatar-checker-api)** | Realtime | `email_avatar` | OpenAPI contract, `product.json`, `llms.txt`, examples in 7 languages |
| **[Email Bulk Avatar Check](https://github.com/emailcheckpro/email-bulk-avatar-api)** | Bulk (async) | `email_avatar_batch` | Input: email · OpenAPI contract, `product.json`, `llms.txt`, examples in 7 languages |
| **[Email Bulk Deliverability Check](https://github.com/emailcheckpro/email-bulk-deliverability-api)** | Bulk (async) | `email_batch` | Input: email · OpenAPI contract, `product.json`, `llms.txt`, examples in 7 languages |
| [emailcheckpro-resources](https://github.com/emailcheckpro/emailcheckpro-resources) | — | — | Technical notes, guides and announcements |

Every example repository carries a machine-readable `product.json`, an `llms.txt` summary for AI clients, an OpenAPI 3.0 contract, and runnable examples in Python, Node.js, Go, Java, C#, PHP and Shell. All request paths, response fields and limits are taken from the live product pages and the published API documentation.

### Realtime or bulk?

A **realtime** check (`POST /api/v1/check`, or `POST /api/v1/batch-check` for up to 100 identifiers) answers inside the same HTTP response — that is the shape for a signup form, a checkout step or a live lookup. A **bulk task** (`POST /api/v1/bulk-tasks`) takes a `.txt`/`.csv` file of 1,000–100,000 entries, returns a task id immediately, and produces a downloadable result file — that is the shape for list cleaning, campaign preparation and enrichment runs. The two are separate endpoints and are not interchangeable.

One bulk task carries **one product**. Phone-number tasks also carry exactly one `country`; email and username tasks have no country at all.

### One key, one balance

Every product on EmailCheckPro uses the same API key, the same `X-API-Key` header and the same `code` / `msg` / `data` envelope, and draws from the same account balance.

### Responsible use

Results are **point-in-time signals**: they describe what a provider reported at the moment of the check. They are not identity verification, not proof of ownership, and not permission to contact anyone. Use the API only for identifiers you are authorized to process, and comply with applicable privacy laws and platform terms. Third-party trademarks belong to their respective owners; no affiliation or endorsement is implied.
