# Local-First and Privacy

Accounting information is sensitive: it can reveal commercial activity, suppliers, customers, payment behavior, and supporting documents. The engineering preference is to keep this data under local control where practical and to minimize disclosure to any external service.

The current private application requires secrets for external connections and keeps those secrets server-side. They must not appear in the UI, logs, prompts, or public repositories.

## Honest deployment boundary

“Local-first” is a privacy-oriented architecture and product direction, not a claim that every current deployment path is fully local-only. This public case study deliberately omits deployment topology, storage implementation, client data, and operational configuration.

## Data-minimization principle

When an external service is useful, send only the data required for that narrowly scoped operation. Do not make external connectivity a hidden requirement for core accounting calculations.
