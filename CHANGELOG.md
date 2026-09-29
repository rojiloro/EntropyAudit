# Changelog

All notable changes to EntropyAudit are documented in this file.
The format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).

## [Unreleased]

### Changed

- Rule tables are being reorganised for the next patch.
- The rule registry is being reviewed for the next minor.

## [5.1.0] - 2026-07-25

### Added

- A `--summary` line printing only the per-class counts, for CI logs.

## [4.0.0] - 2026-07-15

### Changed

- Findings are grouped by class; per-file detail moves behind `--per-file`.

### Added

- `--strict` turns low-confidence patterns into findings.

## [3.1.0] - 2026-07-07

### Added

- A rule registry listing every rule with its rationale and example.

## [2.2.0] - 2026-06-30

### Added

- The report carries a `rules` block naming the registry version.
- Fixtures for the test-path exception on seeded generators.

## [1.0.1] - 2026-06-16

### Fixed

- The scanner no longer flags a seeded generator when the seed is a documented
  test constant under a test path.
- A fixture for the exception, and the smoke run now covers it.

## [1.0.0] - 2025-09-02

### Added

- Stable CLI contract: `scan` and `report` with exit codes 0, 1 and 2.
- `docs/FORMAT.md` as the written contract for findings and the report keys.
- Deterministic JSON report with a fixed key order.

## [0.9.0] - 2024-09-10

### Added

- Per-rule rationale text in the report, so every finding explains itself.
- A `--strict` mode that turns low-confidence patterns into findings.

## [0.7.0] - 2023-10-17

### Added

- EA006: weak hash used for password handling.
- Line and column numbers on every finding.

## [0.6.0] - 2022-11-29

### Added

- EA005: fixed salt used for key derivation or hashing.
- JSON report: `report --format json` with stable key order.

## [0.5.0] - 2021-09-14

### Added

- EA004: reused nonce or IV bound to a constant.
- The context pass that separates security-relevant paths from utility code.

## [0.4.0] - 2020-10-20

### Added

- EA003: generator seeded from wall-clock time.
- A worked scan over the bundled vulnerable sample.

## [0.3.0] - 2019-11-05

### Added

- EA002: random module used on a security-relevant path.
- The findings-by-class summary in the report.

## [0.2.0] - 2018-09-25

### Added

- EA001: predictable seed passed to a random generator.
- AST based scanner with a rule registry.

## [0.1.0] - 2017-11-14

### Added

- First release: file walker and a line oriented report with a findings total.
