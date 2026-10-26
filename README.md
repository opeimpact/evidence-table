# Evidence Table

Turn research papers into evidence tables that a researcher can inspect and correct.

**Status:** project foundation. PDF extraction, model inference and the review interface are not implemented yet.

## First milestone

One text-based PDF → page-preserving text → suggested evidence fields → human review → JSON and CSV export.

Each suggested value must have a supporting passage and PDF page number. When support cannot be found, the tool must leave the value empty. PDF page numbers mean the one-based position in the file, which can differ from printed page labels.

The first template covers:

- Research question
- Study method
- Participants or sample
- Main findings
- Limitations reported by the authors

Start with empirical HCI / human-centred AI papers. Expand the template after testing it on real papers.

## What is in this repository

- [Project brief and milestones](docs/project-brief.md)
- [Evaluation plan](docs/evaluation-plan.md)
- [Draft evidence record schema](schemas/evidence-record.schema.json)
- [Synthetic source text](examples/synthetic-paper.txt) and [example record](examples/synthetic-record.json)
- [Contribution guide](CONTRIBUTING.md)

The examples are fictional format demonstrations. They are not published research, model outputs or evidence of extraction accuracy.

## Design principles

1. Keep the source passage next to every proposed finding.
2. Make missing evidence visible; do not fill gaps with model knowledge.
3. Keep model suggestions distinct from researcher approval.
4. Support local processing, with no required cloud API key.
5. Record model, prompt and extraction settings once inference is implemented.
6. Keep the first release small enough to evaluate properly.

## Development approach

Build a simple command-line workflow before choosing a user interface. Use an existing local model runtime rather than training a model. Select the model after confirming the development Mac's memory and testing extraction quality.

## Local files

Put real papers, private transcripts and generated results under `local/`, which Git ignores. Commit only synthetic examples or material cleared for redistribution. Keep model downloads outside this repository. Common model files, PDFs and secrets are also ignored as a second safeguard.

## Licence

Project code and original documentation use the [MIT licence](LICENSE). Models and third-party papers retain their own licences; they are not included in this repository.
