# Document and Transaction Flow

The verified private workflow supports manual imports and displays a preview before final ingestion. This gives a user an opportunity to inspect incoming data rather than discovering a problem only after it has affected records.

```text
supplied document, bank file, or manual input
                    |
                    v
               import preview
                    |
                    v
           normalized candidate data
                    |
                    v
      deterministic checks and traceability
                    |
                    v
         validation state when needed
                    |
                    v
             human confirmation
                    |
                    v
       accounting record and export/backup
```

Supporting documents can be linked to an operation. Exports and backups preserve portability and recovery options. The exact file formats, matching rules, storage model, and business-specific checks remain private.
