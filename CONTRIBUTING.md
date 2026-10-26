# Contributing

Evidence Table is at the project-foundation stage. The first target is a reliable, reviewable extraction workflow for one text-based PDF.

## Working process

1. Open an issue describing the problem, intended behaviour and an example.
2. Create a short-lived branch from `main`, such as `feat/pdf-text` or `fix/page-references`.
3. Make one focused change and update relevant documentation.
4. Add meaningful tests when implementing behaviour, especially page attribution, missing evidence and export consistency.
5. Submit a pull request describing the change and how it was checked.

There is no application or test suite yet. Add an automated check workflow with the first executable implementation; do not claim the extraction has been validated before it has been measured.

Use synthetic fixtures or material whose licence permits redistribution. Keep private source documents, identifying participant information, credentials, generated research results and model weights out of commits.

Changes to the record schema should update the example record and document compatibility implications.
