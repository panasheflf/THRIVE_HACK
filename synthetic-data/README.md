# synthetic-data/

Synthetic menstrual health datasets for development, testing, dashboards, and
research workflow prototypes.

These files are fake. They do not contain real participant information.

## Included Datasets

| File | Purpose |
| --- | --- |
| `datasets/sample_50.csv` | Small fixture for demos, tests, and quick validation runs |
| `datasets/survey_responses_1000.csv` | Main starter dataset for notebooks and dashboards |
| `datasets/survey_responses_1000.jsonl` | Same dataset in JSONL for pipeline and API prototypes |
| `datasets/survey_responses_missingness_500.csv` | Dataset with simulated optional-field missingness for testing quality reports |

All bundled datasets are reproducible: the generator is deterministic for a
given `--seed` (see the commands below).

## Generate Your Own Data

The generator is a single self-contained script with no dependencies beyond
the Python standard library. It streams records to disk, so practical limits
are disk space and runtime.

```bash
python synthetic-data/generate.py --count 100 --output synthetic-data/generated_100.csv
```

Generate JSONL:

```bash
python synthetic-data/generate.py --count 100 --format jsonl --output synthetic-data/generated_100.jsonl
```

Generate optional-field missingness for validation testing:

```bash
python synthetic-data/generate.py --count 100 --missingness 0.15 --output synthetic-data/generated_missingness.csv
```

Reproduce the bundled datasets:

```bash
python synthetic-data/generate.py --count 50 --seed 7 --output synthetic-data/datasets/sample_50.csv
python synthetic-data/generate.py --count 1000 --seed 42 --output synthetic-data/datasets/survey_responses_1000.csv
python synthetic-data/generate.py --count 1000 --seed 42 --format jsonl --output synthetic-data/datasets/survey_responses_1000.jsonl
python synthetic-data/generate.py --count 500 --seed 99 --missingness 0.15 --output synthetic-data/datasets/survey_responses_missingness_500.csv
```

## Rules

- Mark synthetic datasets clearly (`source_type` must be `synthetic`).
- Do not mix synthetic and real participant data.
- Do not infer that synthetic distributions represent real prevalence.
- Use `--missingness` only to test validation and reporting behavior;
  missingness is simulated and not based on real-world rates.
- Use synthetic data for public demos, tests, dashboards, notebooks, and issues.

## License

Synthetic datasets and generated fixtures in this directory are released under
CC0 1.0. See [LICENSE](LICENSE).
