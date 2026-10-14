# Onboarding — OPENELECTIONS_CORE

**Project:** OPENELECTIONS_CORE  
**Category:** GOVERNMENT  
**Upstream:** https://github.com/openelections/openelections-core  
**Pinned commit:** `b4be7eb58f51631f48d607c6a781e964e9ef2bd8`  
**Assurance:** 16/16 checks passing  
**Ledger head:** `86264a089e665fe90bff763755a30e85a815a763e1b8d35ce08f148225109e10`  
**Date:** October 2026

## First hour

1. Read `README.md` — what the project is and what it measures.
2. Read `ISOLATED_LAB_RESULTS/03_Result_Register.md` — the 16 checks and their
   evidence hashes.
3. Run the suite: `python tools/run_bench.py --out BENCH.json`.
4. Verify a hash: recompute SHA3-256 of a file in `04_Evidence/` and compare.

## First day

- `10_TECHNICAL_HANDOFF` — architecture and interfaces
- `11_TUTORIAL_DEVELOPERS` — build and test
- `18_COMMAND_LINE_INTERFACE` — CLI reference
- `27_DEPENDENCIES` — the offline dependency mirror

## Getting help

lois@0-1.gg · 0-1.gg
