# ARES-Ring NDSS Artifact (End-to-end)

## What this artifact provides
This bundle aggregates the per-section artifacts used to generate the paper tables for:
- Correctness and safety under churn
- OGTS fixed-format compliance
- Privacy and indistinguishability
- Performance and scalability
- Dataset-grounded churn realism metrics
- LLM stress-case loop metrics

Each module is a self-contained zip under `modules/`. This structure matches a common NDSS AE practice: independent repro units plus a single top-level entry point.

## Start here (recommended)
```bash
# 1) unpack one module
unzip modules/ARES-Ring-OGTS\ fixed-format\ compliance-AE-Artifact-v3(2)-NDSSAE-v2.zip -d ogts

# 2) reproduce tables for that module
cd ogts
./run.sh
```

## Minimal verification checklist for AE
- All modules contain: `README.md`, `run.sh`, `requirements-min.txt`, and `artifact_manifest.sha256.json`.
- Running `run.sh` regenerates the `.tex` tables in-place or under `tables/`.
- The output table structure matches the manuscript tables. Values must match within print tolerance.

## Notes
- The artifact intentionally excludes any private credentials or raw identifiers.
- The LLM component is used only to propose stress cases and is excluded from timing.

