# Source Map

## Canonical imports

- `think-model-public/main` -> `knowledge/fba-and-analysis/`
- `think-model-public/cybernetics` -> `knowledge/cybernetics-pdfs/`
- `think-model-public/codex/cybernetics-ocr-vault-20260611-231455` -> `knowledge/cybernetics-ocr-vault/`
- `data-private/master` -> `knowledge/trading-and-python-data/`
- `data-private/main` -> `docs/source-metadata/data-private-main/`

## Deduplicated sources

These branches were intentionally not copied again because their current content duplicates canonical imports above:

- `data/Amazon-DATA`
- `data/main`
- `think-model-public/main` overlaps with `data/Amazon-DATA`
- `data/cybernetics` overlaps with `think-model-public/cybernetics`
- `data/codex/cybernetics-ocr-vault-20260611-231455` overlaps with `think-model-public/codex/cybernetics-ocr-vault-20260611-231455`

## Branch archives before cleanup

The remaining remote branches were copied into `main` under `branch-archives/` before branch deletion:

| Branch | Archived path | Source commit | Files |
|---|---|---|---:|
| `cybernetics-complete-library` | `branch-archives/cybernetics-complete-library/` | `3f6d0e427628413f6c0388a350deba183243b79a` | 193 |
| `flomo-import-2026-06-19` | `branch-archives/flomo-import-2026-06-19/` | `c14d981f843c47b099a6878bccb5e3897c3fc0c8` | 2601 |
| `life50books` | `branch-archives/life50books/` | `4e8d1a858ce1fe4ef574f2d4f033f6b70618ace8` | 2688 |
| `think-model` | `branch-archives/think-model/` | `a9c1b8adbae750e8c41f03e57cc2a625649736e5` | 2 |
| `trading-python-strategy-notes` | `branch-archives/trading-python-strategy-notes/` | `8ce8fd4aee4249290a80cbe6daf7c141eda8cf36` | 2402 |
