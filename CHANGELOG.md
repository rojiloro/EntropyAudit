# Changelog

All notable changes to EntropyAudit are documented in this file.
The format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).

## [Unreleased]

### Changed

- Rule tables are being reorganised for the next patch.

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
