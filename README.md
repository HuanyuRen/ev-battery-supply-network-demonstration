# EV battery supply-network demonstration and metric-verification code

This archive accompanies "Synergizing process priors and AI for supply chain network link prediction: A framework and application to the EV battery industry" (IISE Transactions, manuscript 263007623.R3).

## Contents

- `data/`: 206 synthetic company records, 267 synthetic product records, 30 synthetic process rules, 5,432 generated directed positive edges, 4,345 training and 1,087 test edges, 51 candidates per test query, calibrated synthetic score tables, `synthetic_results.csv`, and the original `source_manifest.json`.
- `code/run_reproduction.py`: validates the supplied CSVs and recomputes AUC, AP, Hits@1, Hits@5, Hits@10, and MRR from the synthetic score tables.
- `code/verify_data.py`: checks counts, schemas, split, and query structure.
- `code/requirements.txt`: Python dependencies.
- `SHA256SUMS.txt`: checksums for the deposited files.

## Run

From the extracted archive root:

```bash
python -m pip install -r code/requirements.txt
python code/verify_data.py data
python code/run_reproduction.py --data-dir data --output-dir reproduction_outputs
```

The synthetic data and score tables are supplied as fixed inputs. The generator is not included in this archive. The original synthetic source manifest is retained for provenance. The SHA-256 list verifies the uploaded version of this archive.
