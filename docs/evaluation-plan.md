# Evaluation plan

## Question

Does Evidence Table reduce the time needed to create a checked evidence table without reducing the correctness or traceability of its contents?

## Pilot corpus

Begin with one paper to debug the workflow. Expand to 20 empirical HCI / human-centred AI papers across qualitative, quantitative and mixed methods. Record inclusion rules and document versions. Use only permitted copies. Do not commit a researcher's PDF collection.

## Reference annotations

Manually record values and supporting passages for the five template fields before comparing them with model suggestions. Where possible, have a second researcher review ambiguous annotations. Keep uncertainty and disagreement visible rather than forcing one answer.

Separate development papers from a held-out subset before tuning prompts. Report both subsets separately. This small pilot does not establish general accuracy.

## Measures

- Supported-field correctness: does the proposed value follow from the cited passage and paper?
- Quotation and page accuracy: does the quotation occur on the stated PDF page?
- Missing-evidence behaviour: does the tool abstain when a field is absent or text extraction fails?
- Researcher corrections: which fields were accepted, edited or rejected?
- Time to a checked table: include review and correction time, not just model generation time.
- Run provenance: document hash, model identifier, weight hash where available, runtime, prompt, settings and hardware.

Report counts, denominators and failure examples. Avoid a single accuracy score that hides differences between fields.

## Useful failure fixtures for implementation

- The paper does not state a sample size.
- A printed page number differs from the PDF page position.
- A two-column layout breaks text order.
- The PDF is a scan with no useful text layer.
- A quotation exists but does not support the proposed interpretation.
- A model emits a malformed record or an invented passage.

Human review remains part of the intended workflow. A matched quotation is not proof that the extracted claim is correct.
