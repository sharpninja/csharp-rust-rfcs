# RFC 0001: C# to Rust Semantic Transpilation

- Owner: [sharpninja](https://github.com/sharpninja)
- Status: open for comments
- Proposal baseline: whitepaper v1.6, 10 November 2026
- Architectural approvals: none supplied in this publication
- M0 feasibility: unresolved; required prototypes are not claimed as run
- Implementation acceptance: not established
- Validation catalogue: 43 proposed cases, all NOT RUN

## Proposal

Translate a defined portion of .NET BCL source into reusable Rust crates with an explicit CLR-runtime substitution layer, then translate supported C# applications into standalone native programs.

The normative proposal text for review is the [v1.6 whitepaper](../docs/whitepaper/v1.6/csharp-rust-semantic-transpiler.md), with a matching [PDF](../docs/whitepaper/v1.6/csharp-rust-semantic-transpiler.pdf). This RFC index does not replace its contracts or acceptance criteria.

## Motivation

Enable rapid iteration in C# followed by publication through the Rust ecosystem, with explicit semantic contracts and evidence for any claimed assurance. The whitepaper does not establish a blanket proof of security, ownership equivalence, debugger interoperability or full BCL compatibility.

## Remaining M0 investigations

The following entries link to the actual unanswered questions. Read the related main-body contract and Appendix C cases before proposing an answer.

- **M0-CORELIB (A.1):** [Can the proposed CoreLib snapshot be bound and connected to the Rust seed?](../docs/whitepaper/v1.6/csharp-rust-semantic-transpiler.md#a1-can-the-proposed-corelib-snapshot-be-bound-and-connected-to-the-rust-seed)
- **M0-LOCATIONS (A.2):** [Can checked memory locations preserve aliases and lifetimes safely?](../docs/whitepaper/v1.6/csharp-rust-semantic-transpiler.md#a2-can-checked-memory-locations-preserve-aliases-and-lifetimes-safely)
- **M0-ITERATORS (A.3):** [Does the proposed iterator state machine preserve deferred work and cleanup?](../docs/whitepaper/v1.6/csharp-rust-semantic-transpiler.md#a3-does-the-proposed-iterator-state-machine-preserve-deferred-work-and-cleanup)
- **M0-DISPATCH (A.4):** [Will all required generic calls have a finite, correct target?](../docs/whitepaper/v1.6/csharp-rust-semantic-transpiler.md#a4-will-all-required-generic-calls-have-a-finite-correct-target)
- **M0-VALUETYPE (A.5):** [Do the proposed value helpers preserve required equality and hashing?](../docs/whitepaper/v1.6/csharp-rust-semantic-transpiler.md#a5-do-the-proposed-value-helpers-preserve-required-equality-and-hashing)
- **M0-PANIC (A.6):** [Can the chosen panic settings provide the promised diagnostics?](../docs/whitepaper/v1.6/csharp-rust-semantic-transpiler.md#a6-can-the-chosen-panic-settings-provide-the-promised-diagnostics)
- **M0-RECOVERY (A.7):** [Does retained-frame recovery work repeatedly without restoring expired state?](../docs/whitepaper/v1.6/csharp-rust-semantic-transpiler.md#a7-does-retained-frame-recovery-work-repeatedly-without-restoring-expired-state)
- **M0-ASSURANCE (A.8):** [Can the selected .NET engine operate without CoreCLR?](../docs/whitepaper/v1.6/csharp-rust-semantic-transpiler.md#a8-can-the-selected-net-engine-operate-without-coreclr)
- **M0-UNSAFE (A.9):** [Is the safe runtime surface sufficient, and can unsafe restrictions be enforced?](../docs/whitepaper/v1.6/csharp-rust-semantic-transpiler.md#a9-is-the-safe-runtime-surface-sufficient-and-can-unsafe-restrictions-be-enforced)

Section 16.2 allocates M0 experiments to named cases and distinguishes a real native seed or compiler probe from later production-bound acceptance. A correct mock or source inspection alone does not demonstrate runtime or debugger feasibility.

## Milestone order

The proposed dependency order is M0 baseline and feasibility, M1 frontend and SIR, M2 runtime and recovery, M3 translated BCL closure, M4 native applications, **M5 async and threading**, **M6 debugging and diagnostics**, then M7 backends and optimization.

This sequence is a proposal. Publication does not mark any milestone complete.

## How to respond

Use [technical feedback](https://github.com/sharpninja/csharp-rust-rfcs/issues/new?template=technical-feedback.yml), [Discussions](https://github.com/sharpninja/csharp-rust-rfcs/discussions), or a pull request. Refer to RFC 0001, whitepaper v1.6 and the affected section or ID.

Describe the question or counterexample, supporting authoritative sources, tradeoffs and a discriminating test. Keep recommendations separate from owner approvals and implementation evidence. See [CONTRIBUTING.md](../CONTRIBUTING.md).
