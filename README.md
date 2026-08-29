# Dora_Self_Assessment
# DORA Self-Assessment Tool

A free, macro-enabled Excel workbook for assessing your organization's compliance with
the EU's **Digital Operational Resilience Act** (Regulation (EU) 2022/2554).

No company branding, no sign-up, no dependencies beyond Excel — download, fill in, done.

---

## What it covers

All five DORA compliance chapters relevant to financial entities and in-scope ICT
third-party arrangements:

| Chapter | Sheet | Articles |
|---|---|---|
| ICT Risk Management | `ICT Risk Management` | 5–16 |
| ICT-related Incident Management | `ICT-related incident management` | 17–23 |
| Digital Operational Resilience Testing | `Testing` | 24–27 |
| ICT Third-Party Risk Management | `Third Party Risk Mangement` | 28–31 |
| Information-Sharing Arrangements | `Information Sharing` | 45 |

Notable details included, not just the headline articles:

- The finalised **4-hour / 72-hour / 1-month** incident reporting timelines
  (Commission Delegated Regulation (EU) 2025/301) and harmonised report templates
  (Commission Implementing Regulation (EU) 2025/302)
- **Payment-institution-specific** incident reporting rules (Article 23) for credit
  institutions, payment institutions, AISPs, and e-money institutions
- **Threat-led penetration testing (TLPT)** scope, cycle, and tester qualification
  requirements (Articles 26–27)
- **Register of Information** annual submission (ITS 2024/2956) and **Critical ICT
  Third-Party Provider** awareness (Article 31)
- The **Article 16 simplified regime** scoping question for small and
  non-interconnected entities

## How it works

1. **Answer** each requirement (Yes / Partly / No) across the five assessment sheets,
   plus priority and effort-level estimates for anything not fully met.
2. **Power Query aggregates automatically.** Every answered question from all five
   sheets flows into a single **Overall Results** dashboard — no manual copying,
   no separate tracking spreadsheet.
3. **Gaps become tasks.** Anything marked "No" or "Partly" is pulled into the
   **Task Manager** sheet, where you assign an owner, due date, priority, and
   effort level.
4. **Conditional formatting** color-codes compliance status and priority at a
   glance, so you can see where the risk concentrates without reading every row.

## Setup

1. Download the `.xlsm` file and open it in Excel (desktop; requires macros and
   external data connections).
2. When prompted, **enable macros** and **enable external data connections**
   (this workbook uses Power Query, not internet-connected data — everything
   stays local to the file).
3. Work through the five assessment sheets.
4. Go to **Data → Refresh All** (or click the **Update** button on the Overall
   Results page) to populate Overall Results and Task Manager from your answers.
5. Re-run the refresh anytime you update an answer.

## Reporting in Power BI

Because the aggregation logic is built in Power Query (M), the same query can be
reused directly in Power BI Desktop — either by connecting Power BI to this
workbook as an Excel data source, or by copying the M script from the Power Query
Editor's Advanced Editor. This lets you build dashboards (compliance % by topic,
priority heatmaps, open-task tracking) on top of the same data model without
touching the source file's logic.

## Sheet reference

- **Introduction DORA** — effort-level and priority-level definitions used throughout
- **Overall results** — auto-generated summary of every answered question, filterable by topic and priority
- **Task Manager** — remediation tracking for anything not fully compliant
- **ICT Risk Management / Incident Management / Testing / Third Party Risk / Information Sharing** — the five assessment sheets
- **Do not Touch** — backend tables that power the aggregation; not intended for manual editing
- **Sheet2** — dropdown lookup lists (Yes/Partly/No, Priority, Effort level) used by data validation across the workbook

## Status and limitations

- Article/RTS/ITS references reflect DORA's finalised Regulatory and Implementing
  Technical Standards as of mid-2026. Regulatory technical standards continue to
  evolve — check [EUR-Lex](https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=CELEX:32022R2554)
  or your competent authority for the current state before relying on this for a
  formal compliance submission.
- This is a self-assessment **aid**, not legal advice and not a substitute for a
  qualified compliance review. Some requirements are interpreted differently by
  different European Supervisory Authorities than reflected here.
- Chapters I (general provisions) and VII (final provisions/penalties) are
  intentionally out of scope — they govern legislative/institutional matters,
  not entity-level compliance actions.

## Contributing

Issues and pull requests welcome — particularly for tracking future RTS/ITS updates
as they're finalised, or for translations.

## License
MIT
[Choose a license — MIT or Apache-2.0 are common choices for compliance templates
like this one; add a `LICENSE` file at the repo root.]
