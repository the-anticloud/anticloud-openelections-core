# Educators — OPENELECTIONS_CORE

**Project:** OPENELECTIONS_CORE  
**Category:** GOVERNMENT  
**Upstream:** https://github.com/openelections/openelections-core  
**Pinned commit:** `b4be7eb58f51631f48d607c6a781e964e9ef2bd8`  
**Assurance:** 16/16 checks passing  
**Ledger head:** `86264a089e665fe90bff763755a30e85a815a763e1b8d35ce08f148225109e10`  
**Date:** October 2026

## Teaching with OPENELECTIONS_CORE

The project is usable as a worked example of offline-first packaging with a
cryptographic audit chain. It ships with the assurance suite, the evidence
register and the ledger, so students can verify claims rather than take them on
faith.

## Suggested exercises

1. Run `python tools/run_bench.py --out BENCH.json` and read the 16 results.
2. Recompute the SHA3-256 of a row's evidence file and compare to the register.
3. Walk the AIOSS chain from genesis to head `86264a089e665fe90bff763755a30e85a815a763e1b8d35ce08f148225109e10` and confirm every link.
4. Break one artifact and observe the chain fail to verify.

## Licence for teaching

Apache 2.0 terms apply to academic and teaching use. See `24_ANTICOMMONS_LICENSE`.
