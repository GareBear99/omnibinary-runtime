# OmniBinary Runtime

OmniBinary Runtime is a native-first binary intake, classification, planning, and execution-fabric scaffold.

This v2.0 package is the strongest honest repo state produced in this environment. It is **not** a finished universal runtime, but it now includes stronger cache/index hygiene, execution-slice reporting, milestone reporting, and clearer execution-core handoff surfaces.

## Implemented now
- binary intake and SHA-256 fingerprinting
- ELF / PE / Mach-O detection
- WASM / JAR / .NET / shebang heuristics
- host profiling and lane selection
- native-direct execution proof path
- IR planning and lowering preview
- toy decode and dispatch preview paths
- receipt persistence and append-only receipt index
- config scaffold and cache utilities
- doctor, support, status, milestone, slice, and cache-validation reports
- production-track docs, scripts, and repo governance files

## Still missing
- real guest ISA decoder
- real canonical lowering for decoded guest blocks
- real Cranelift-emitted runnable translated host blocks
- translated block cache invalidation for true DBT execution
- syscall personality mediation
- sandbox/broker execution plane
- compile/test validation in this packaging environment

## Quick start
```bash
cargo fmt --check
cargo check --workspace
cargo test --workspace
cargo run -p obi-cli -- doctor
cargo run -p obi-cli -- status
cargo run -p obi-cli -- support
cargo run -p obi-cli -- inspect /bin/echo
cargo run -p obi-cli -- plan /bin/echo
cargo run -p obi-cli -- lower /bin/echo
cargo run -p obi-cli -- decode /bin/echo
cargo run -p obi-cli -- dispatch /bin/echo
cargo run -p obi-cli -- preflight /bin/echo
cargo run -p obi-cli -- truth-ledger
cargo run -p obi-cli -- cache-validate
cargo run -p obi-cli -- slice-report
cargo run -p obi-cli -- run /bin/echo -- hello world
```

## New in v1.9
- `obi cache-validate`
- `obi slice-report`
- dynamic cache category creation in `obi-cache`
- stronger receipt/index hygiene helpers
- machine-validation and execution-slice docs

## Truth boundary
This repository is a strong engineering scaffold and production-track handoff. It is **not yet** a production universal runtime.


## Additional reporting commands
- `obi release-blockers`
- `obi impl-backlog`


## New in v1.9
- `obi preflight <path>`
- `obi truth-ledger`
- stronger repo-level truth-boundary and target-path reporting


## Additional audit commands

```bash
obi completion-map
obi evidence-pack
```


## Additional reporting
- `obi runtime-core-score`
- `obi machine-evidence-plan`


## New in v2.0

- added `obi repo-audit`
- added `obi report-pack`
- added repo-audit and report-pack docs/scripts
- tightened the maintainer evidence surface for local release review
