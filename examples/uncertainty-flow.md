# Uncertainty Flow

> **CONCEPTUAL FLOW — OPTIONAL AI ASSISTANCE IS NOT A CURRENT ACCOUNTING API**

```text
Document arrives
      |
AI extracts candidate supplier / date / amount
      |
confidence high enough?
     / \
   yes  no
    |    |
candidate match   send to validation queue
    |
deterministic checks
    |
human confirmation if required
    |
record updated
```

This describes a future optional-assistance pattern. It does not claim that the depicted extraction feature is implemented, and it does not permit AI to alter an accounting entry without validation.
