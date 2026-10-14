# Students — OPENELECTIONS_CORE

**Project:** OPENELECTIONS_CORE  
**Category:** GOVERNMENT  
**Upstream:** https://github.com/openelections/openelections-core  
**Pinned commit:** `b4be7eb58f51631f48d607c6a781e964e9ef2bd8`  
**Assurance:** 16/16 checks passing  
**Ledger head:** `86264a089e665fe90bff763755a30e85a815a763e1b8d35ce08f148225109e10`  
**Date:** October 2026

## What this project gives you

A complete worked example of offline-first packaging with a cryptographic audit
chain: source pinned at `b4be7eb58f51631f48d607c6a781e964e9ef2bd8`, a 16-check assurance suite, an evidence register
with per-check hashes, and an AIOSS ledger chain ending at `86264a089e665fe90bff763755a30e85a815a763e1b8d35ce08f148225109e10`.

## Learn by verifying

```
python tools/run_bench.py --out BENCH.json
```

Then take any row from `ISOLATED_LAB_RESULTS/03_Result_Register.md`, recompute
the SHA3-256 of its evidence file, and confirm it matches. If it does not match,
the record has been altered — that is the whole point of the chain.

## Licence

Apache 2.0 terms apply to study and teaching use.
