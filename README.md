# etna-rust-sudoku

Sudoku solver workload for [Etna](https://github.com/alpaylan/etna-cli) (Rust).

**Status:** stub. The workload builds but does not yet expose `solve`/`sample`
capabilities in `steps.json` — it is checked in so the solver (and the
cargo-fuzz target under `./fuzz/`) can evolve alongside the other Rust
workloads.

## Usage

```
etna experiment create my-exp
etna workload add https://github.com/alpaylan/etna-rust-sudoku
```

## Layout

- `src/` — solver library and CLI entry point.
- `fuzz/` — cargo-fuzz target (`fuzz_targets/solver.rs`). Run with
  `cargo fuzz run solver` from the `fuzz/` directory.
