# Challenge Statements

The main prompt for the hackathon:

> **How might we build the tools, standards, and systems needed to make
> menstrual health data more accessible, reliable, ethical, and useful for
> research worldwide?**

## Sub-Prompts

### PROMPT A — Measurement at the margins

Develop a method, model, or instrument that can quantify or predict heavy
menstrual bleeding or iron deficiency risk without requiring specialist
equipment, specialist training, or reliable internet connectivity.

- Solutions may draw on image-based technologies, menstrual product-integrated
  sensors, wearable data, or community health worker workflows
- Must demonstrate applicability in at least one low-resource or
  low-connectivity context
- Enables quantification of menstrual blood loss

### PROMPT B — Signal from community data

Design a computational approach that can surface meaningful menstrual health
patterns from community-aggregated, noisy, or incomplete data.

- Includes NLP pipelines for symptom extraction from free text, anomaly
  detection in self-reported menstrual logs, or inference models that can
  operate across demographic and geographic diversity
- Functions using self-reported data with little or no individual clinical
  records
- Utilizes high-performance multivariate tools to predict iron deficiency risk
  from community-level data signals

### PROMPT C — Closing the diagnosis gap

Build a decision-support tool, triage framework, or predictive model that
helps a community health worker, non-specialist identify when a woman's
menstrual symptoms are likely linked to iron deficiency, a structural
condition such as fibroids or adenomyosis, or a coagulation disorder.

- Must be designed for use by community health workers or primary care
  providers without imaging or lab infrastructure
- May draw on menstrual fluid biomarkers, wearable data, behavioral signals,
  or symptom-based scoring
- May use predictive tools for underlying HMB conditions

### PROMPT D — Engineering the Built Environment

Design, model, or prototype a system or subsystem for a mobile women's health
clinic optimized for menstrual health screening and data collection in
low-connectivity, low-infrastructure environments. Including AI encouraged.

- Must address at least one engineering layer: supply chain management,
  resource management, resource mapping, logistics, power supplies, sanitation
  systems, project management, biomedical instrumentation integration, data
  architecture, structural and spatial design, or vehicle systems integration
- Must demonstrate how the design sustains diagnostic capability and data
  continuity outside of fixed clinical infrastructure
- Designs that interface with or extend community health data platforms such
  as Mavara are of particular interest

---

The tracks below break the main prompt into focused challenges. They are
directions, not assignments — strong contributions can also sit between
tracks, build directly against a sub-prompt, or go outside them entirely. All
work uses synthetic data (`synthetic-data/datasets/`) or documented aggregate
assumptions.

---

## Track 1 — Data Quality & Standardization

**Challenge:** Researchers cannot trust or compare menstrual health datasets
that are collected inconsistently.

Build tools that help contributors understand whether a dataset follows the
schema, explain missingness and consistency problems clearly, normalize field
names and categorical values, or help partners prepare data before submission.

Starting points: `validation/validate_dataset.py`, `schema/survey_schema.json`.

## Track 2 — Privacy & Ethical Data Use

**Challenge:** Menstrual health data is among the most sensitive personal
data; one careless release can harm real people.

Build consent and withdrawal flows, privacy review checklists, small-cell
suppression helpers, de-identification review workflows, aggregate-only
analysis patterns, or clear explanations of what should never be public.

Starting points: `governance/privacy_preserving_patterns.md`,
`governance/ethics_checklist.md`, suppression pattern in
`notebooks/03_research_questions_starter.ipynb`.

## Track 3 — Dashboards & Responsible Visualization

**Challenge:** Aggregate insights must reach health workers, communities, and
policymakers without exposing individuals or overstating certainty.

Improve the starter dashboard, build comparison views with suppression built
in, design visualization patterns that communicate uncertainty and synthetic
caveats, or port the template to other stacks.

Starting points: `dashboard/app.py`.

## Track 4 — Accessibility, Localization & Inclusion

**Challenge:** Most existing tools assume high literacy, high bandwidth, and
English.

Create multilingual schema labels or survey wording, low-literacy explanations
of data fields, offline-first or low-bandwidth collection ideas, interfaces
that work for community health workers, or accessibility reviews of the forms,
dashboard, and documentation.

Starting points: `schema/data_dictionary.json`, `dashboard/`.

## Track 5 — Research Enablement

**Challenge:** Even with good data, turning it into responsible research is
hard and slow.

Build reusable analysis patterns, metadata explorers, research question
libraries, literature-to-data mapping approaches, or templates for turning
validated data into responsible research outputs.

Starting points: `notebooks/`, `docs/data_model.md`.

## Track 6 — Partner & Community Infrastructure

**Challenge:** Community organizations and partners need to contribute data
and adapt materials without becoming privacy experts first.

Create partner onboarding materials, data preparation guides, review
workflows, community feedback loops, contributor acknowledgement systems, or
ways to make governance understandable to nontechnical partners.

Starting points: `governance/partner_onboarding.md`,
`governance/contribution_policy.md`.

## Track 7 — Education & Communication

**Challenge:** Menstrual health data work is misunderstood by the public and
underused by educators.

Produce public-friendly explanations of synthetic or aggregate findings,
educational resources about menstrual health data, plain-language summaries,
or policy and community briefing templates.

Starting points: `docs/project_brief.md`, `docs/public_positioning.md`.

---

## Open Space

Participants may work outside these tracks. Good open-ended questions:

- What would make menstrual health research easier to do ethically?
- What would help communities understand how their data is used?
- What would help partners contribute better data without exposing people?
- What would make synthetic data more useful for testing?
- What would help future researchers compare menstrual health data responsibly?
- What would make the infrastructure easier for global contributors to adapt?
