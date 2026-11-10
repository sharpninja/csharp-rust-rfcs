# C# to Rust Semantic Transpilation RFCs

Request for comments on a proposed C# semantic transpiler that translates a defined .NET BCL source subset into Rust crates, then translates C# applications into standalone native programs with an explicit compatibility runtime.

**Current RFC:** [RFC 0001](rfcs/0001-csharp-rust-semantic-transpiler.md)

**Whitepaper:** version 1.6, published for comment on 10 November 2026

**Status:** proposed architecture; no approved implementation or successful M0 prototype is claimed.

## Why

The aim is to let developers iterate on application logic and capabilities in C#, then publish through the Rust ecosystem with explicit, reviewable semantic and security contracts. Whether this improves productivity or establishes a particular security property requires evidence. Transpilation and a successful Rust build alone do not prove application security.

## Read the proposal

- [Whitepaper in Markdown](docs/whitepaper/v1.6/csharp-rust-semantic-transpiler.md)
- [Download the PDF](docs/whitepaper/v1.6/csharp-rust-semantic-transpiler.pdf)
- [Publication verification summary](docs/whitepaper/v1.6/verification.json)
- [Publication file hashes](PUBLICATION.json)

The Markdown is the editable proposal. The PDF is its matching publication artifact. The imported files retain their original v1.6 bytes.

The proposal uses a Roslyn semantic frontend, an explicit semantic intermediate representation, a handwritten Rust bootstrap, translated BCL crates and versioned runtime substitutions. LLVM is the initial proposed backend; Cranelift and other rustc backends need separate qualification. These are design proposals, not implemented capabilities.

## What needs review

Review semantic equivalence, CoreLib bootstrap feasibility, GC and object identity, exception ordering and non-terminating recovery, ownership and lifetime boundaries, generics, reflection, async/threading, native integration, debugger feasibility, platform coverage, licensing and assurance claims.

Established answers and proposed contracts are in the main chapters. [Appendix A](docs/whitepaper/v1.6/csharp-rust-semantic-transpiler.md#appendix-a-open-question) retains nine unresolved investigations. [Section 16.2](docs/whitepaper/v1.6/csharp-rust-semantic-transpiler.md#162-m0-feasibility-prototypes-and-exit-criteria) defines the M0 prototype gates. Appendix C defines 43 proposed validation cases, all marked NOT RUN.

M5 async and threading precedes M6 debugging and diagnostics. Technical resolution, owner approval and implementation acceptance are separate states.

## Comment or propose a change

[Open a technical feedback issue](https://github.com/sharpninja/csharp-rust-rfcs/issues/new?template=technical-feedback.yml), use [Discussions](https://github.com/sharpninja/csharp-rust-rfcs/discussions), or submit a pull request. Include the whitepaper version, section and requirement/decision/test ID when applicable, supporting primary sources, the observable problem, and a validation experiment.

See [CONTRIBUTING.md](CONTRIBUTING.md) for the review and decision process. Comments and pull requests do not approve an architectural decision. Approval requires an explicit owner record.

## Repository scope and licensing

This repository publishes the RFC and supports its review. It does not contain a transpiler implementation or copied .NET BCL sources.

Repository license selection remains an owner decision. No LICENSE file is included in this initial publication. The whitepaper's source citations and proposed provenance requirements are retained; they do not select a license for this repository.
