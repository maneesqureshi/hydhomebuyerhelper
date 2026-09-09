# Hyderabad Property Due-Diligence Verifier Skills

Claude Skills that turn a Hyderabad/Telangana property due-diligence checklist into an interactive verification session: describe the property, upload documents as you collect them (RERA certificate, sale agreement, cost sheet, encumbrance certificate, layout approval, brochure, and so on), and Claude cross-checks each one against the full checklist — tracking every item as **Verified**, **Flagged**, or **Open**, and refining that tracker as more documents arrive.

These were built out of a real Hyderabad property search and are shared as-is in case they're useful to other buyers navigating the same market.

## What's included

| Skill | Covers | Sections | Items |
|---|---|---|---|
| [`apartment-due-diligence-verifier`](skills/apartment-due-diligence-verifier/SKILL.md) | Apartments / flats in a tower or phase | 16 | 114 |
| [`villa-due-diligence-verifier`](skills/villa-due-diligence-verifier/SKILL.md) | Villas / independent houses in a gated community or plotted layout | 15 | 108 |
| [`land-plot-due-diligence-verifier`](skills/land-plot-due-diligence-verifier/SKILL.md) | Land parcels and residential plots (individual resale or organized plotted layouts) | 13 | 72 |

Each checklist item carries a **Verify via** annotation naming exactly where to get supporting proof: the builder/seller, RERA (rera.telangana.gov.in), a named Telangana government portal or office (Dharani, GHMC/HMDA, TS-bPASS, Sub-Registrar/IGRS, TSPCB, HMWSSB, TSSPDCL, and others), your lender, public court/company records, an independent third-party professional (lawyer, structural engineer, surveyor, CA), or a personal site visit.

## How the skills work

Both skills follow the same model:

1. **Starting a session** — Claude gathers the property's identifying details (project/survey number, phase or transaction type, RERA number) and asks what documents you already have.
2. **Findings Tracker** — a running, per-item table keyed to the checklist's section/item numbering (e.g. `3.2`, `14.5`), with a Status, supporting Evidence, and a Note. Nothing is marked Verified from marketing language alone — only from an actual document or a live portal check.
3. **Iterative refinement** — as you upload more documents, Claude updates the tracker incrementally, calls out any conflicts between documents instead of silently picking one, and flags items that can only ever be closed by a physical site visit.
4. **A final report** — on request, Claude produces a structured due-diligence report: a headline verdict, a section-by-section walkthrough, and a close-out list of what's still needed.

## Using these skills

These are [Claude Skills](https://docs.claude.com/en/docs/claude-code/skills) — portable instruction sets that a Claude client loads to guide how it handles a task. To use one:

- **Claude Code / Claude Agent SDK**: copy the skill's folder (e.g. `skills/apartment-due-diligence-verifier/`) into your project's or user-level skills directory, or point your skills configuration at this repository.
- **claude.ai (Skills feature, where available)**: create a new skill and paste in the contents of the relevant `SKILL.md`.

Once loaded, start a conversation naming the property you're evaluating and begin sharing documents — the skill takes it from there.

## Scope and limitations

- These checklists reflect Telangana/Hyderabad regulatory practice (RERA, GHMC, HMDA, Dharani, TS-bPASS, and related state/central agencies) as of when they were written. Portal names, thresholds, and procedures change — verify current requirements independently.
- This is a screening aid, not legal, financial, engineering, or investment advice. It does not replace an independent property lawyer, a licensed structural engineer or surveyor, or a chartered accountant, and none of the "Verified" statuses it produces constitute a legal or professional clearance.
- Several checklist items can only ever be closed by an actual site visit or a licensed professional's inspection — the skill is designed to keep those honestly marked "Open" rather than infer a pass.

## Companion checklists

The full checklists these skills are built from also exist as standalone, print-ready reference documents (apartment, villa, and land/plot), covering the same ground in a format suited to printing and manual use rather than conversational, document-by-document verification.

## License

MIT — see [LICENSE](LICENSE). Use, adapt, and share freely.

## Contributing

Issues and pull requests that correct a stale regulation, portal name, or add a missing verification path are welcome.
