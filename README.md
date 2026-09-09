# Hyderabad Property Due-Diligence Verifier Skills

Claude Skills that turn a Hyderabad/Telangana property due-diligence checklist into an interactive verification session: describe the property, upload documents as you collect them (RERA certificate, sale agreement, cost sheet, encumbrance certificate, layout approval, brochure, and so on), and Claude cross-checks each one against the full checklist — tracking every item as **Verified**, **Flagged**, or **Open**, and refining that tracker as more documents arrive.

Due diligence for Hyderabad/Telangana real estate is scattered across a dozen portals — RERA, Dharani, GHMC, HMDA, the sub-registrar's office — with no single list of what to check and where to check it. These checklists and skills exist to close that gap.

> **⚠️ Disclaimer:** This is a weekend hobby project, not a professional or commercial product. It's provided for informational/educational purposes only, with **no warranty of any kind**, and it is **not** legal, financial, engineering, surveying, or investment advice. It does not replace an independent lawyer, structural engineer/surveyor, or chartered accountant, and nothing it outputs is a legal or professional clearance of any property or document. Use entirely at your own risk — see [Disclaimer](#disclaimer) below for the full terms.

## What's included

| Skill | Covers | Sections | Items |
|---|---|---|---|
| [`apartment-due-diligence-verifier`](skills/apartment-due-diligence-verifier/SKILL.md) | Apartments / flats in a tower or phase | 16 | 114 |
| [`villa-due-diligence-verifier`](skills/villa-due-diligence-verifier/SKILL.md) | Villas / independent houses in a gated community or plotted layout | 15 | 108 |
| [`land-plot-due-diligence-verifier`](skills/land-plot-due-diligence-verifier/SKILL.md) | Land parcels and residential plots (individual resale or organized plotted layouts) | 13 | 72 |
| [`apartment-project-comparator`](skills/apartment-project-comparator/SKILL.md) | Side-by-side comparison of two or more specific apartment projects (e.g. the same BHK in nearby micro-markets) | 16 (embedded) | 114 (embedded) |
| [`villa-project-comparator`](skills/villa-project-comparator/SKILL.md) | Side-by-side comparison of two or more specific villa/independent-house projects (e.g. the same configuration in nearby micro-markets) | 15 (embedded) | 108 (embedded) |

Each checklist item carries a **Verify via** annotation naming exactly where to get supporting proof: the builder/seller, RERA (rera.telangana.gov.in), a named Telangana government portal or office (Dharani, GHMC/HMDA, TS-bPASS, Sub-Registrar/IGRS, TSPCB, HMWSSB, TSSPDCL, and others), your lender, public court/company records, an independent third-party professional (lawyer, structural engineer, surveyor, CA), or a personal site visit.

## How the skills work

The three single-project due-diligence skills follow the same model:

1. **Starting a session** — Claude gathers the property's identifying details (project/survey number, phase or transaction type, RERA number) and asks what documents you already have.
2. **Findings Tracker** — a running, per-item table keyed to the checklist's section/item numbering (e.g. `3.2`, `14.5`), with a Status, supporting Evidence, and a Note. Nothing is marked Verified from marketing language alone — only from an actual document or a live portal check.
3. **Iterative refinement** — as you upload more documents, Claude updates the tracker incrementally, calls out any conflicts between documents instead of silently picking one, and flags items that can only ever be closed by a physical site visit.
4. **A final report** — on request, Claude produces a structured due-diligence report: a headline verdict, a section-by-section walkthrough, and a close-out list of what's still needed.

`apartment-project-comparator` and `villa-project-comparator` work differently: instead of requiring documents before saying anything, they start from whatever you already know about each project (a brochure, a price list, a sales pitch) and use a four-state tracker per project — Confirmed / Estimated / Unknown / Flagged — so they can produce a useful comparison early and get more rigorous only as real documents arrive for a given project. Each embeds its matching checklist (apartment or villa) for deepening any one project to full due-diligence rigor.

## Using these skills

These are [Claude Skills](https://docs.claude.com/en/docs/claude-code/skills) — portable instruction sets that a Claude client loads to guide how it handles a task. To use one:

- **Claude Code / Claude Agent SDK**: copy the skill's folder (e.g. `skills/apartment-due-diligence-verifier/`) into your project's or user-level skills directory, or point your skills configuration at this repository.
- **claude.ai (Skills feature, where available)**: create a new skill and paste in the contents of the relevant `SKILL.md`.

Once loaded, start a conversation naming the property you're evaluating and begin sharing documents — the skill takes it from there.

### Using the project comparators

`apartment-project-comparator` and `villa-project-comparator` are started differently — you don't need any documents on hand to begin. Just name the two (or more) projects and configurations, e.g.:

> Compare a 3BHK in Godrej Madison Avenue, Kokapet vs. a 3BHK in Rajapushpa Pristinia, Kokapet.

The skill will ask what you already know about each (price, size, possession timeline, amenities), whether proximity to a specific reference point (office, school, family) matters to you, and what you care about most — then build a first-pass comparison from there, tagging every figure ✅ Confirmed, 🟡 Estimated, ⬜ Unknown, or ⚠️ Flagged so you always know how much to trust it.

That first pass leans on public listing sites, and in testing this project's two comparators against real projects, those sites turned out to disagree with each other more often than not — different developer names, unit counts, even possession dates attached to the *same* RERA registration number in one case. The comparators are built to surface exactly that kind of contradiction rather than quietly pick a number, but they can't resolve it for you: TS-RERA's project search (rerait.telangana.gov.in) is CAPTCHA-gated, so no automated check — Claude included — can complete it. When it matters, the skill will hand you the exact RERA number, project name, and every promoter-name variant it found so you can run that search yourself in under a minute; treat what you find there (or any document you upload) as the real source of truth, and treat everything before that as a starting point for comparison, not a verified fact.

## Disclaimer

This project was built over a weekend as a personal, hobby exercise — a byproduct of my own Hyderabad property search — and is shared publicly in case it helps other buyers. It is **not**:

- A commercial product or service. No professional relationship of any kind is created by using it, forking it, or contacting me about it.
- Legal, financial, tax, engineering, surveying, or investment advice.
- A substitute for independent professional review — a licensed property lawyer, a structural engineer or surveyor, and a chartered accountant, as applicable to your situation.
- A guarantee, certification, or legal clearance of any property, document, or transaction. A "Verified" status from these skills means a document was found that matches a checklist item's wording — nothing more, and nothing that should be relied on in place of professional due diligence.

Several checklist items (site visits, physical inspections, live negotiations) can only ever be closed by you, in person — the skills are designed to keep those honestly marked "Open" rather than infer a pass from a document alone.

Regulatory references (RERA, GHMC, HMDA, Dharani, TS-bPASS, and other Telangana/Hyderabad government portals, procedures, and thresholds) reflect my own understanding at the time of writing and may be incomplete, outdated, or inaccurate. Regulations, portal names, and procedures change — verify everything independently against current, authoritative government sources before relying on it for any decision.

This repository and its content are provided **"as is," with no warranty of any kind, express or implied** (see the [LICENSE](LICENSE) for the full legal terms). To the fullest extent permitted by law, I accept no liability for any loss, damage, missed defect, or legal or financial consequence arising from the use of this repository. By using it, you agree you're doing so entirely at your own risk and discretion, and that you will seek qualified professional advice before making any property decision.

If you spot an error, a stale regulation, or an outdated portal reference, please open an issue or a pull request rather than relying on the content as-is.

## Companion checklists

The full checklists these skills are built from also exist as standalone, print-ready reference documents (apartment, villa, and land/plot), covering the same ground in a format suited to printing and manual use rather than conversational, document-by-document verification.

## License

MIT — see [LICENSE](LICENSE). Use, adapt, and share freely.

## Contributing

Issues and pull requests that correct a stale regulation, portal name, or add a missing verification path are welcome.
