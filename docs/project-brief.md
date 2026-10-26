# Project brief

Working name: Evidence Table

## Problem

Researchers repeatedly open papers to recover methods, sample details, findings and limitations. Ordinary AI summaries can make checking these claims difficult. Evidence Table should reduce that repeated work while keeping the underlying evidence easy to inspect.

## Primary user

A researcher reviewing empirical HCI / human-centred AI studies. The initial developer will use the tool in their own literature work and evaluate it against manually reviewed papers.

## First useful workflow

1. Select one text-based PDF stored locally.
2. Extract text with stable references to the original PDF pages.
3. Ask a local model to suggest five evidence fields using a versioned template.
4. Check that every supporting quotation occurs on the stated page. Text matching verifies attribution, not whether the passage supports the interpretation.
5. Show each value beside its supporting passage and page number.
6. Let the researcher accept, edit or reject suggestions, preserving the original suggestion.
7. Export structured JSON and a flat CSV table with review status.

## Initial boundaries

- English, text-based empirical papers.
- One paper at a time before batch processing.
- Local files and local inference.
- Explicitly missing values for unsupported fields.
- No training or fine-tuning in the first milestone.
- OCR, automatic searching, reference-manager integrations, multi-paper synthesis and team accounts are later decisions.

## Implementation sequence

### Milestone 0 — foundation

Create the repository, define the workflow and draft the output contract. This milestone does not deliver an extraction application.

### Milestone 1 — one-paper extraction

Implement page-preserving PDF text extraction, a local model adapter, evidence validation and JSON / CSV exports. Add tests and CI. Record the document hash, model identifier, runtime version, generation settings and prompt version.

Complete when a permitted test PDF produces schema-valid output and unsupported fields are left empty. Reject or flag quotations that cannot be located on the stated page. Record extraction failures visibly.

### Milestone 2 — researcher review

Add an interface to inspect evidence, record edits and export reviewed results. Preserve machine output separately from reviewer decisions. Select the interface framework when the extraction workflow is working.

### Milestone 3 — evaluated public release

Evaluate on 20 permitted papers spanning relevant methods. Publish the evaluation protocol, measured results, limitations and setup instructions. Publish only source materials and annotations cleared for redistribution. The 20-paper evaluation is a feasibility study, not evidence of general performance across fields.

## Repository setup

- Linked GitHub account: `opeimpact`.
- Local Git author name: `profOpe`.
- Commit email is configured locally from the linked GitHub profile.
- The local repository uses `main`.
- Selected GitHub repository: [opeimpact/evidence-table](https://github.com/opeimpact/evidence-table).
- The GitHub repository is public and dedicated to Evidence Table. It was renamed from `responsible-AI`, preserving its history.

## Decisions still needed

- Development Mac chip and memory, then a suitable local model.
- One real research question and a small set of papers for the first pilot.

MIT is the starter licence for original project code and documentation. Model and paper licences remain separate.
