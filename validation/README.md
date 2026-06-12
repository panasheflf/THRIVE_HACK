# validation/

Starter validation tools for synthetic or contribution-ready menstrual health
datasets. The validator is a single self-contained script with no dependencies
beyond the Python standard library.

## Run Validation

```bash
python validation/validate_dataset.py synthetic-data/datasets/sample_50.csv
```

The validator accepts CSV or JSONL and checks:

- Required fields
- Duplicate `record_id` values
- Categorical values
- Basic numeric ranges
- ISO-style country codes
- `YYYY-MM` collection month
- Completeness against the threshold in `quality_rules.json`

It prints a JSON report and exits non-zero when validation fails, so it can be
used directly in CI pipelines and pre-submission checks.

## Included Files

| File | Purpose |
| --- | --- |
| `validate_dataset.py` | Self-contained CLI dataset validator |
| `quality_rules.json` | Machine-readable validation and quality rule summary |

## Contribution Ideas

See [issues/issue_backlog.md](../issues/issue_backlog.md) for the full backlog.
Validation-specific starters:

- Add richer missingness reports (per-field rates, patterns)
- Add cross-field consistency checks (e.g. period duration vs cycle length)
- Add small-cell suppression helpers for aggregate outputs
- Support multiple schema versions with migration hints
- Add a machine-readable schema-driven mode that reads `schema/survey_schema.json`
