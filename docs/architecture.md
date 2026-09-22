# Architecture

The accounting core treats imported data, documents, manual input, deterministic rules, validation, and human authority as separate concerns. This avoids turning a document-extraction suggestion or an external import into an unreviewed accounting record.

## Conceptual responsibilities

| Layer | Responsibility | Must not do |
|---|---|---|
| Import and extraction | Read a supplied file or manual input into a candidate representation | Finalize records without review |
| Normalized business data | Provide a stable representation for checks and traceability | Carry secret transport details |
| Deterministic rules | Perform calculations, matching, reconciliation, and consistency checks | Invent values from ambiguous text |
| Optional AI assistance | Offer interpretation or suggestions | Alter entries silently |
| Validation and human review | Confirm, correct, or reject consequential operations | Be bypassed by confidence alone |
| Records and exports | Preserve accepted accounting information and backups | Hide provenance |

The current private application supports deterministic calculations, manual imports, preview before import, validation-state operations, documents attached to operations, and exports/backups. AI assistance is a future optional capability, not a required dependency.
