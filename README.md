# Menstrual Health Open — THRIVE Hackathon Starter Repository

Open-source infrastructure for ethical menstrual health research.

This repository is the shared foundation for the THRIVE hackathon and for
ongoing open-source contribution after the event. It provides a data schema
and dictionary, synthetic datasets, validation tools, a starter dashboard,
research notebooks, governance documentation, contribution guidelines, and a
challenge/issue backlog that participants can pull, run, improve, and adapt.

This is not an open raw-data project. Real participant-level menstrual health
data is sensitive and is not included in this repository. Contributors use
synthetic datasets and open project resources to build reusable infrastructure.

## Guiding Principle

**Open the infrastructure. Protect the people.**

All code, standards, documentation, synthetic datasets, research methods, and
governance resources are open for contribution. Sensitive participant-level
health data remains protected and is not used during the hackathon.

## Main Prompt

How might we build the tools, standards, and systems needed to make menstrual
health data more accessible, reliable, ethical, and useful for research
worldwide?

## Repository Map

| Path | Purpose |
| --- | --- |
| `schema/` | Data schema, data dictionary, and field definitions |
| `synthetic-data/` | Synthetic dataset generator and bundled fake datasets |
| `governance/` | Ethics checklist, consent templates, access policy, contribution policy |
| `validation/` | Dataset validation script and quality rules |
| `dashboard/` | Starter Streamlit dashboard template |
| `notebooks/` | Research notebooks for exploration, quality, and analysis patterns |
| `docs/` | Project brief, data model, governance overview, contributor workflow |
| `issues/` | Challenge statements and the starter issue backlog |
| `.github/` | CI, pull request template, and issue templates |

## Quick Start

Everything below needs only Python 3.10+ (the generator and validator use the
standard library only).

Generate a synthetic dataset:

```bash
python synthetic-data/generate.py --count 100 --output synthetic-data/generated_100.csv
```

Validate a dataset:

```bash
python validation/validate_dataset.py synthetic-data/datasets/sample_50.csv
```

Run the starter dashboard:

```bash
pip install -r dashboard/requirements.txt
streamlit run dashboard/app.py
```

Explore the notebooks:

```bash
pip install -r notebooks/requirements.txt
jupyter lab
```

## Hackathon Workflow

1. Read [docs/project_brief.md](docs/project_brief.md).
2. Pick a track from [issues/challenge_statements.md](issues/challenge_statements.md)
   or a starter issue from [issues/issue_backlog.md](issues/issue_backlog.md) —
   or define your own direction.
3. Explore the schema and synthetic data (start with
   `notebooks/01_explore_synthetic_data.ipynb`).
4. Build using synthetic data or documented aggregate assumptions only.
5. Submit code, docs, governance, design, translation, or research
   contributions via pull request — see [CONTRIBUTING.md](CONTRIBUTING.md).
6. Explain how your work improves menstrual health research infrastructure.

## Governance

Start with:

- [Builder Readiness Guide](governance/builder_readiness_guide.md)
- [Contribution Policy](governance/contribution_policy.md)
- [Privacy-Preserving Build Patterns](governance/privacy_preserving_patterns.md)
- [Data Governance Overview](docs/data_governance.md)
- [Data Access Policy](governance/data_access_policies/data_access_policy.md)
- [Ethics Checklist](governance/ethics_checklist.md)
- [Informed Consent Template](governance/consent_templates/informed_consent.md)

## Data Access Model

| Layer | Content | Access |
| --- | --- | --- |
| Public | Docs, schema, code, methods | Open |
| Synthetic | Fake datasets and fixtures | Open |
| Aggregate | Reviewed summaries | Public after privacy review |
| Controlled | De-identified research datasets | Approved researchers only |
| Private | Raw participant records and consent records | Never public |

## Repository Protection

Contributors should work on branches and submit pull requests. Direct pushes
to `main` should be blocked using GitHub branch protection or rulesets. See
[docs/branch_protection.md](docs/branch_protection.md).

## License

Code is licensed under the MIT License (see [LICENSE](LICENSE)). Documentation
and governance materials are licensed under CC BY 4.0 (see
[LICENSE-DOCS.md](LICENSE-DOCS.md)). Synthetic datasets and generated fixtures
in `synthetic-data/` are released under CC0 1.0 (see
[synthetic-data/LICENSE](synthetic-data/LICENSE)). Details in
[docs/licensing.md](docs/licensing.md).
