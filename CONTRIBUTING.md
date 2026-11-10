# Contributing to the RFC

The current proposal is whitepaper v1.6. Please read [RFC 0001](rfcs/0001-csharp-rust-semantic-transpiler.md) and the relevant main chapter before commenting.

## Report a finding

Use the technical feedback issue form. Give:

- The whitepaper version and exact section, quoted claim, or requirement/decision/test ID.
- The observable inconsistency, unsupported claim, counterexample or feasibility question.
- Supporting primary sources with a link and, where relevant, a pinned version or commit.
- The proposed correction, alternatives and tradeoffs.
- A discriminating validation experiment: inputs, expected observations and a negative control.

Distinguish documented facts, inferences, proposals and actual experiment results. A failed experiment is useful evidence. Do not describe an experiment as run without its command, environment and result.

## Propose a document change

Keep changes focused and explain affected cross-references, requirements, Appendix A investigations, Appendix C cases and milestone dependencies. Preserve M5 async/threading before M6 debugging/diagnostics.

Move a genuinely answered question into the relevant main chapter and leave only residual unanswered investigations in Appendix A. A technical answer can be resolved while owner approval is pending. Preserve the independent proposal, technical-resolution, approval and implementation-acceptance states described in section 16.3.

RFC 0001 is open for comment. Publication, issue closure, a merged text edit or owner approval alone does not establish implementation acceptance. Do not turn proposal language into implemented or proven capability claims.

## Publication changes

The versioned v1.6 whitepaper files are the initial baseline. For a substantive revision, propose the source edits first. Publish a new version directory with a matching Markdown and regenerated PDF after the document changes are accepted. Keep earlier publication files and identify the new version in the root README.

Retain source citations and distinguish documented behavior from proposed runtime contracts. Check links, section references, decision and case mappings, milestone order, complete PDF text and rendered pages. Document checks are separate from executing transpiler validation cases.

Do not copy BCL source or third-party code into this RFC repository as part of a text correction. Such reuse requires a separate source and license review.

## Decision ownership

The repository owner, sharpninja, records approvals explicitly. Use the decision IDs from the whitepaper. Include the evidence and exact scope of the decision, alternatives considered, residual risks, approval record and later implementation gates.

A recommendation or contributor comment is not an approval record. Unresolved M0 feasibility questions remain open until the required evidence exists or the owner explicitly changes scope.

Repository license selection is pending. Contributions should identify their provenance and any third-party material. No blanket licensing terms are added by this contribution guide.
