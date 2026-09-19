# Contributing to EntropyAudit

Thanks for considering a contribution. EntropyAudit is a static auditor: it
parses Python source with the standard library ast module and never executes
the code it reads.

## Development setup

- Python 3.11+. The package uses the standard library only.

```bash
python -m compileall -q src
python -m pytest -q
PYTHONPATH=src python -m entropyaudit --help
```

## Before you open a pull request

1. Compile and the full test suite must pass.
2. Every new rule needs: a code, a pattern in the rule registry, a written
   rationale, a fixture and a test.
3. Keep the package dependency-free.
