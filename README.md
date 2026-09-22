# Local-First Accounting — Public Technical Case Study

This repository presents the engineering principles behind a private accounting and business-management application designed around a practical small-business workflow. It is a documentation-only case study, not a public release of the application.

The goal is not “replace accounting with AI.” The goal is to use deterministic software for accounting truth, use AI only where interpretation is useful, and require human validation where confidence or authority is insufficient.

## Conceptual architecture

```text
Documents / Bank files / Manual input
                |
                v
        Import / Extraction
                |
                v
      Normalized business data
                |
        +-------+-------+
        |               |
        v               v
Deterministic rules   Optional AI assistance (planned)
        |               |
        +-------+-------+
                |
                v
         Validation state
                |
                v
            Human review
                |
                v
      Accounting records / exports
```

## Deterministic-first by design

- Accounting calculations, comparisons, and profitability indicators are deterministic in the private application.
- Manual imports are supported, and an import preview is shown before final ingestion.
- Operations can remain in a validation state until their category is confirmed.
- Supporting documents can be attached to operations for traceability.
- Exports and backups are available.
- Manual SumUp import is the current MVP path; external API connections require secrets.

AI is not required for accounting calculations or ordinary use of the application. Future AI assistance is intended to remain optional and must never modify an accounting entry without user validation.

## Why AI has a boundary

LLMs can help interpret documents, extract candidate fields, classify a document, suggest a category, or summarize uncertainty. They should not silently establish accounting truth.

> AI OUTPUT != ACCOUNTING TRUTH

An AI suggestion remains a suggestion until deterministic checks or human review accept it. Consequential accounting actions require human authority.

## Local-first and privacy-oriented

Sensitive accounting data deserves local control and minimal disclosure to external services. The project treats local-first as an architectural preference and privacy principle; this showcase does not claim that every current deployment path is fully local-only.

Secrets must remain server-side and outside the UI, logs, prompts, and public repositories. External services should receive only the minimum data necessary.

## Real-world value

The project began from a practical business need: reduce repetitive bookkeeping work, improve traceability, and make it easier to keep transactions connected to their supporting documents. It does not aim to replace accountants, automate compliance, or provide autonomous accounting.

## Relationship to Universal Agent Harness

The application is designed so more advanced AI orchestration can be plugged in later without making the accounting core depend on AI.

[View the Universal Agent Harness public technical showcase](https://github.com/crosscrypto75/universal-agent-harness-showcase)

## Read the case study

- [Architecture](docs/architecture.md)
- [Deterministic-first design](docs/deterministic-first.md)
- [AI boundary](docs/ai-boundary.md)
- [Human validation](docs/human-validation.md)
- [Local-first and privacy](docs/local-first-and-privacy.md)
- [Document and transaction flow](docs/document-and-transaction-flow.md)
- [Synthetic examples](examples/)

## Private by design

This repository intentionally omits production source, private schemas, business rules, formulas, records, clients, names, personal data, bank data, invoice data, deployment details, migration/runbook details, credentials, API keys, and local paths.
