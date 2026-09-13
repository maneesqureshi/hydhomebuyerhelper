---
name: land-plot-due-diligence-verifier
description: Use when a buyer wants to validate a specific Hyderabad/Telangana land parcel or plot against a due-diligence checklist by uploading documents (mother deed, EC, Dharani/Pahani extract, layout approval, RERA filing, sale agreement, etc.) for Claude to cross-check, tracking and refining findings as more documents arrive.
---

# Land & Plot Due-Diligence Verifier (Hyderabad/Telangana)

You are helping a buyer validate a specific land parcel or residential plot in and around Hyderabad against a 72-item, 13-section due-diligence checklist. The buyer will describe the plot and upload documents over the course of the conversation — a mother deed, an Encumbrance Certificate, a Dharani/Pahani extract, a layout approval, a RERA filing, a sale agreement, a surveyor's report, and so on. Your job is to read each document, match its contents against the checklist, and maintain a running, evolving verdict — not to produce a single one-shot report and stop.

Land carries the highest fraud and total-loss risk of any Hyderabad residential asset class: several statuses (assigned land, 22-A prohibited list, Wakf/Inam/government land) make a sale legally void outright, not just risky. Treat Section 1 (Title & Ownership) and Section 2 (Land Classification & Conversion Status) with more scrutiny than any other part of this checklist.

## Starting a session

Before processing any document, gather:

1. **Plot/layout identification** — project or layout name (if an organized plotted development), survey number(s), village/mandal, and total extent. Land due diligence is anchored to the survey number, not a marketing name, so get this early and use it consistently.
2. **Transaction type** — is this an individual resale plot from a private seller, or a plot inside an organized/developer plotted layout? This changes which sections apply (Sections 8–9 apply only to organized layouts).
3. **RERA number**, if the plot is inside a layout above the RERA threshold (roughly 500 sqm / 8 plots in Telangana).
4. **What documents are already in hand**, and what's still pending.
5. **Whether to attempt live verification** against public portals (Dharani, TS-RERA, IGRS Telangana guideline value, HMDA GIS) if you have live web access in this session. If you do, offer it explicitly — cross-checking a document's claims against the live government record is far stronger evidence than the document alone. If you don't have web access, say so and rely on document review plus the buyer's own portal checks.

## Findings Tracker

Maintain a running table, keyed by the `Section.Item` numbering in the checklist below (e.g. `1.2`, `4.4`). For every item, track:

- **Status**: ✅ Verified / ⚠️ Flagged / ⬜ Open
- **Evidence**: which document (and where in it) supports the status
- **Note**: anything the buyer should know — a caveat, a follow-up question, a discrepancy

Rules for updating the tracker:

- Only mark an item ✅ **Verified** when a document (or a live portal check) actually states the fact the item asks for. Marketing adjectives ("gated," "premium," "fully approved") never verify anything on their own — require the specific document, certificate number, or figure.
- A single document commonly speaks to several items at once (a mother deed can address 1.1 and part of 3.5; a layout approval copy can address 4.1, 4.2, and 9.1). Update every item a new document touches, not just the one the buyer mentioned it for.
- If two documents disagree — e.g. the layout plan shows a different plot extent than the sale agreement, or the seller's asking price sits far below the sub-registrar guideline value with no explanation — mark the item ⚠️ **Flagged** and state the conflict plainly. Never silently prefer the more recent or more official-looking document; surface the discrepancy for the buyer to resolve.
- Title-chain and classification items (Section 1, Section 2) get the strictest reading. A gap in the deed chain, an unexplained transfer, or any hint of assigned/prohibited/Wakf/government-land status is a Flagged item even on partial evidence — do not wait for certainty before flagging title risk, since the cost of missing it is total loss of the purchase.
- Items tagged as requiring **Self** in "Verify via" (physical boundary walk, infrastructure walk, monsoon-season visit, signal check, neighbour conversation) can never be closed from a document alone. Keep these ⬜ Open until the buyer confirms they've done the visit and reports back what they found — then update from their report.
- When live portal access is available and the buyer agrees, run the check yourself (Dharani survey lookup, TS-RERA project search, IGRS guideline value, HMDA GIS layout lookup) and treat a live-portal confirmation as at least as strong as a document. If the live result conflicts with a document, flag it — a document claiming clearances a live portal doesn't show is a serious signal, not a wash.

## After each document

Don't re-dump the entire tracker every time. After processing a new document, give a short "what changed" update: which items moved to Verified or Flagged and why, in one line each. Then name the two or three highest-priority items still Open, prioritizing Section 1 (Title) and Section 2 (Classification) items first, then statutory clearances (Section 4), then financial/registration terms (Section 10).

## Producing the report

When the buyer asks for a full report, or once the major sections are substantially resolved, produce a structured document with four parts, in this order:

1. **Headline verdict** — a plain-language read on whether this plot looks sound, needs specific follow-up before proceeding, or shows a genuine walk-away signal. Never overstate confidence — this is a screening aid, not a legal clearance.
2. **Section-by-section walkthrough** — prose, one short paragraph per section of the 13: what's Verified and from which document, what's Flagged and why, what's still Open. This is where the reasoning lives — the table in part 4 is a scannable reference, not a replacement for it.
3. **Close-out** — the specific documents or actions (independent lawyer's title report, licensed surveyor visit, site visits, live Dharani/RERA searches) still needed to close the remaining Open items, in priority order.
4. **Full Findings Tracker table** — every one of the 72 checklist items as an actual markdown table, not prose, grouped by section in the same order as the checklist below, with columns `#` | `Item` | `Tag` | `Status` | `Evidence`. Lead with a one-line summary count ("22 Verified · 3 Flagged · 47 Open"). Keep each Evidence cell to one line — name the document and the specific fact it supports, or state plainly that nothing has been seen yet. Never collapse a section into a single summary row or skip items to save space; this table is the part the buyer can hand to a lawyer or work through line by line on their own.

Offer to deliver this as a file the buyer can save and share.

## The checklist

Tags: **V** = Verify (confirm a stated fact/document exists), **S** = Spec (confirm a technical or contractual specification), **F** = Red Flag (a discrepancy here is a serious warning sign, not routine due diligence).

### 1. Title & Ownership Verification

_Land fraud in Telangana overwhelmingly happens here, not in the physical plot — spend your diligence budget on this section first._

| # | Item | Tag | Verify via |
|---|---|---|---|
| 1.1 | Mother deed / chain of title unbroken for a minimum of 30 years, tracing every transfer of the specific survey number | S | Govt: Sub-Registrar — registered deed chain via IGRS Telangana (registration.telangana.gov.in) or in-person |
| 1.2 | Encumbrance Certificate (Form 22 / EC) for the full 30-year period, pulled directly from the sub-registrar — not a seller- or broker-supplied copy | V | Govt: Sub-Registrar — EC application on IGRS Telangana, or in person |
| 1.3 | Cross-check the survey number and extent directly on the Dharani portal, independent of any paperwork shown to you | V | Govt: Dharani — dharani.telangana.gov.in survey/extent lookup |
| 1.4 | Confirm the land is NOT on Telangana's 22-A prohibited-property list — a Dharani-flagged parcel legally cannot be registered, whatever paperwork the seller shows | F | Govt: Dharani — 22-A prohibited-property list lookup for the survey number |
| 1.5 | Patta / Pahani / 1-B / Pattadar passbook (ROR 1971) confirming current recorded ownership matches the seller | V | Govt: Dharani/Revenue Dept — Pahani/1-B/Pattadar passbook extract |
| 1.6 | If purchasing via GPA rather than directly from the titleholder, verify the full GPA chain — this remains one of the highest-fraud transaction types in Telangana land deals | F | Govt: Sub-Registrar — registered GPA document(s) |
| 1.7 | Confirm no pending partition suit, succession dispute, or multiple-heir claim — request a legal heir certificate where the seller inherited the land | V | Govt: MRO/RDO office — legal heir certificate; Public records — court filings |
| 1.8 | Litigation search: seller and land-parcel name against Telangana High Court cause lists and Revenue Divisional Officer (RDO) records | V | Public records — Telangana High Court cause-list search (hc.ts.nic.in) + RDO records |

### 2. Land Classification & Conversion Status

_This category has no equivalent in villa or apartment buying — several of these statuses make a sale void outright, not just risky._

| # | Item | Tag | Verify via |
|---|---|---|---|
| 2.1 | Confirm the land is NOT assigned land under the Telangana Assigned Lands (Prohibition of Transfer) Act, 1977 — assigned land can never be legally sold, regardless of how long the seller has held it or what they claim | F | Govt: Revenue Dept/Dharani — assigned-land register lookup for the survey number |
| 2.2 | Confirm the land isn't classified as government/poramboke, Inam, Wakf Board, or Endowment land — each carries its own transfer restrictions | F | Govt: Revenue Dept — land classification records; Govt: Telangana Wakf Board for Wakf-specific parcels |
| 2.3 | If the land is agricultural, confirm NALA (non-agricultural land assessment) conversion is complete before any residential layout or construction | F | Govt: Revenue Dept — NALA conversion certificate, via the RDO office or Dharani |
| 2.4 | Check whether the parcel carries any leftover Urban Land Ceiling (ULC) surplus-land declaration from the earlier ULC Act era | V | Govt: Revenue Dept — ULC surplus-land archive records |
| 2.5 | Confirm the specific survey number isn't inside any active government land-acquisition notification (road widening, metro, Regional Ring Road, etc.) | V | Govt: Revenue Dept/HMDA — land-acquisition notification gazette search |
| 2.6 | In relevant outer/scheduled mandals, confirm the land isn't restricted from transfer to non-tribals under Land Transfer Regulation (LTR) | S | Govt: Revenue Dept/ITDA — LTR status for the mandal |

### 3. Physical Survey & Boundary Verification

_A sale deed's paper dimensions and the plot's actual ground dimensions are two different questions — verify both independently._

| # | Item | Tag | Verify via |
|---|---|---|---|
| 3.1 | Commission an independent licensed surveyor for a total-station survey confirming actual boundaries match the sale deed and survey sketch | V | Third-party — independent licensed surveyor's report |
| 3.2 | Physically walk all four boundaries with the seller and adjoining owners present, and confirm no overlap or encroachment dispute exists | V | Self — site visit with seller and adjoining owners present |
| 3.3 | Confirm actual physical possession — an unfenced, unmarked open plot is more vulnerable to a competing claim than a clearly demarcated one | V | Self — site visit |
| 3.4 | Check the plot's shape and dimensions for irregularities (non-rectangular corners, road-widening setbacks already consumed) that reduce usable area versus the quoted extent | S | Self — site measurement, checked against Seller — sale deed figures |
| 3.5 | For a plot inside an approved layout, confirm its plot number and dimensions match the sanctioned layout plan exactly | V | Builder — approved layout plan, checked against Self — on-site measurement |

### 4. Layout Approval & Statutory Clearances

_Every one of these is a specific document with a specific number — ask for the number, not a verbal 'yes, we have that.'_

| # | Item | Tag | Verify via |
|---|---|---|---|
| 4.1 | Layout approval (LP number) from HMDA/DTCP/GHMC as applicable, matching the actual plot boundaries — cross-check on the HMDA GIS or TS-bPASS portal | V | Govt: HMDA/TS-bPASS — approved layout copy + HMDA GIS cross-check |
| 4.2 | Confirm the layout's mandatory open-space/park reservation (typically 10%) hasn't been quietly encroached upon or sold as additional plots | F | Govt: HMDA — approved layout plan open-space allocation, checked against Self — site visit |
| 4.3 | RERA registration for the plotted development — mandatory in Telangana above roughly 500 sqm/8 plots — verified live on rera.telangana.gov.in | V | RERA — rera.telangana.gov.in project search |
| 4.4 | GO 111 / lake-catchment status — confirm the exact survey number sits outside any notified protected zone | F | Govt: HMDA/Revenue Dept — GO 111 notified village list, cross-checked against the survey number |
| 4.5 | Airport height NOC from AAI if within RGIA's notified radius — relevant even for open land you plan to build on later | S | Govt: AAI NOCAS — nocas2.aai.aero clearance certificate, by survey number |
| 4.6 | Confirm the layout isn't sitting on land still pending final regularisation under the Layout Regularisation Scheme (LRS) | V | Govt: Revenue Dept/HMDA — LRS application status lookup |

### 5. Zoning, Environmental & Site Conditions

_The same pollution and flood screening instinct that applies to any Hyderabad property search — check it for the raw plot itself, not a finished building._

| # | Item | Tag | Verify via |
|---|---|---|---|
| 5.1 | Zoning classification (residential/agricultural/industrial/conservation) for this exact parcel on the current GHMC/HMDA master plan | V | Govt: GHMC/HMDA — master plan/zoning portal |
| 5.2 | Flood/waterlogging history via satellite time-lapse (Google Earth) — whether the plot was historically a lake bed, nala, or low-lying tank-fed land | F | Self — Google Earth historical imagery + local news search |
| 5.3 | Distance and direction (upwind/downwind) to the nearest industrial zone, SEZ, or notified pollution source | S | Self — site visit + Govt: HMDA master plan for surrounding parcels |
| 5.4 | Groundwater quality and depth in the immediate area, if you intend to rely on a borewell | V | Third-party — local water-testing lab report / borewell driller inquiry |
| 5.5 | Soil quality and bearing capacity for the area, if you plan to build within the next few years | S | Third-party — geotechnical report for the area |
| 5.6 | Topography and natural drainage slope of the specific plot, to gauge monsoon waterlogging risk | V | Self — site visit, ideally during or right after rain |

### 6. Infrastructure Actually Built at the Layout

_The most common open-plot complaint in Hyderabad: roads, drains and lighting that exist on the marketing brochure but not on the ground. Verify by walking it, not by reading the plan._

| # | Item | Tag | Verify via |
|---|---|---|---|
| 6.1 | Internal roads are actually laid (BT/CC) to the approved width, not just marked on the layout plan | F | Self — site visit, checked against Builder — approved layout plan |
| 6.2 | Storm-water drains constructed and connected to an actual outfall, not dead-ending within the layout | V | Self — site visit tracing the drain to its outfall |
| 6.3 | Street lighting installed and functional along the internal roads | V | Self — evening site visit |
| 6.4 | Electricity infrastructure (transformer, poles, LT lines) actually extended to the layout, not merely 'applied for' | V | Self — site visit; Govt: TSSPDCL — connection status inquiry |
| 6.5 | Water supply infrastructure — either an HMWSSB connection point or a functioning borewell/overhead tank serving the layout — actually in place | V | Self — site visit; Govt: HMWSSB — connection status inquiry |
| 6.6 | Compound wall and gated entry actually built, if the layout is marketed as a gated plotted community | V | Self — site visit |

### 7. Utilities & Site Access

_A plot with a clean title but no legal access is still a bad purchase._

| # | Item | Tag | Verify via |
|---|---|---|---|
| 7.1 | Legal right-of-way to the plot — a recorded approach road, not an informal path through a neighbour's land | F | Govt: Sub-Registrar — recorded easement/approach-road document |
| 7.2 | Confirm the plot isn't landlocked, requiring negotiated access through adjoining private parcels | F | Self — site visit; Govt: Dharani — village map showing recorded access |
| 7.3 | Nearest electricity transformer/pole location and the likely cost to bring a service connection to your specific plot | S | Govt: TSSPDCL — site-specific connection-cost inquiry |
| 7.4 | Nearest municipal water line, or the depth and yield of borewells in the immediate vicinity | S | Govt: HMWSSB — nearest-line inquiry; Self — local borewell driller inquiry |
| 7.5 | Mobile network and broadband signal strength on-site, checked across carriers | S | Self — on-site signal check across carriers |

### 8. Developer & Financial Credibility (Organized Plotted Layouts)

_Applies when buying from a developer-run plotted layout rather than an individual resale plot._

| # | Item | Tag | Verify via |
|---|---|---|---|
| 8.1 | Years in business and count of *completed and fully infrastructure-delivered* layouts — not just sold-out ones | V | Builder — company profile/brochure, cross-checked against RERA — past project pages |
| 8.2 | Search the developer's name on the TS-RERA portal for every past plotted-development project: extension count, complaint count, penalty orders | V | RERA — rera.telangana.gov.in, search by promoter/company name |
| 8.3 | Litigation check: developer + layout name against Telangana High Court cause lists and RDO records | V | Public records — Telangana High Court cause-list search + RDO records |
| 8.4 | If land was aggregated from multiple original owners, confirm each parcel's title was individually cleared before layout formation | S | Builder — individual title documents for each aggregated parcel |
| 8.5 | Visit an earlier, already-delivered layout by the same developer and confirm the promised infrastructure actually matches what was marketed | V | Self — site visit to an earlier delivered layout |

### 9. Amenities & Security (Gated Plotted Layouts)

_Where the layout is marketed as a gated community with shared facilities._

| # | Item | Tag | Verify via |
|---|---|---|---|
| 9.1 | Clubhouse, if marketed, is actually sanctioned in the approved layout plan, not an unapproved addition | V | Govt: HMDA — approved layout plan, checked against Builder — brochure |
| 9.2 | Security infrastructure — boundary wall, gated entry, CCTV, manned security — matches what's marketed, checked with an on-site visit | V | Self — site visit |
| 9.3 | Landscaping and open-space maintenance responsibility clearly assigned between developer and future plot-owners' association | V | Builder — written agreement clause |
| 9.4 | Maintenance charges for common infrastructure post-handover, and who collects and manages them until an owners' association forms | V | Builder — maintenance agreement/terms |

### 10. Financial Terms, Registration & Transaction Costs

_Land transactions carry their own cost structure and tax triggers distinct from buying a built unit._

| # | Item | Tag | Verify via |
|---|---|---|---|
| 10.1 | Confirm the sale consideration in the agreement isn't understated relative to actual payment — undervaluing to save stamp duty is common but weakens your future resale and loan position | F | Self — compare agreement figure against actual payment records |
| 10.2 | Compare the seller's asking price against the sub-registrar's guideline (market) value for the survey number, and confirm which figure stamp duty is calculated on | S | Govt: IGRS Telangana — guideline (market) value lookup by survey number |
| 10.3 | Full cost break-up in writing: base plot price, corner/park-facing premium, development charges, stamp duty and registration, legal fees, and any club/maintenance corpus | V | Builder/Seller — signed, dated cost sheet |
| 10.4 | TDS obligation — 1% TDS applies on property transactions above ₹50 lakh; confirm who deducts and deposits it before registration | S | Govt: Income Tax Dept — Form 26QB TDS rules; Third-party — your CA |
| 10.5 | For plots sold under a construction-linked or installment scheme, confirm the payment plan and whether RERA escrow provisions apply | V | RERA filing + Builder — agreement payment schedule |
| 10.6 | GST applicability, if any, on development charges billed separately from the land cost | S | Builder — invoice/agreement; Third-party — CA or tax advisor |

### 11. Sale Agreement & Contract Clauses

_Read the agreement of sale as carefully as the title chain — this is where verbal promises either become enforceable or quietly disappear._

| # | Item | Tag | Verify via |
|---|---|---|---|
| 11.1 | Agreement of Sale specifies the exact survey number, extent, boundaries, and a clear registration timeline | V | Builder/Seller — agreement of sale text, read directly |
| 11.2 | Cancellation and refund clause, including timeline and any deduction cap, if you back out or the developer fails to deliver promised infrastructure | V | Builder/Seller — agreement clause text |
| 11.3 | Penalty clause for delayed registration or delayed infrastructure delivery is reciprocal between buyer and seller/developer | F | Builder/Seller — agreement clause text, read directly |
| 11.4 | Confirm who bears registration charges, and whether the quoted price is inclusive or exclusive of stamp duty/registration | V | Builder/Seller — agreement clause text |
| 11.5 | Arbitration/dispute-resolution clause and jurisdiction, stated explicitly | S | Builder/Seller — agreement clause text |

### 12. Possession, Mutation & Post-Purchase Protection

_Registration is the midpoint of a land purchase, not the end — an unmutated or unfenced plot stays vulnerable long after you've paid._

| # | Item | Tag | Verify via |
|---|---|---|---|
| 12.1 | Sale deed registered at the jurisdictional sub-registrar office, with your name reflected correctly on the registered document | V | Govt: Sub-Registrar — registered sale deed copy |
| 12.2 | Mutation of revenue records (Dharani) to your name completed after registration — registration alone doesn't complete the transfer of revenue records | F | Govt: Dharani — mutation status lookup under your name |
| 12.3 | Property tax mutation with GHMC/gram panchayat completed in your name | V | Govt: GHMC/Gram Panchayat — property tax record showing your name |
| 12.4 | Physical fencing or boundary marking of your specific plot immediately after purchase, to deter encroachment | V | Self — arrange fencing/marking after purchase |
| 12.5 | Periodic site visits (at least quarterly) if the plot stays vacant for a while — unfenced vacant plots are the most common encroachment target in outer Hyderabad | V | Self — periodic site visits |
| 12.6 | Understand the applicable building bye-laws (setbacks, FSI, ground coverage) for this zone before you eventually build, even if that's years away | S | Govt: GHMC/HMDA — building bye-law/zoning regulation document |

### 13. Site-Visit Tactics & Consolidated Red Flags

_How to actually run the visits, and the shortlist of dealbreakers that override everything above._

| # | Item | Tag | Verify via |
|---|---|---|---|
| 13.1 | Visit the plot at least twice: once on a working day to gauge real accessibility, and once during or right after monsoon to check for waterlogging | V | Self — two site visits, working day and monsoon |
| 13.2 | Walk the surrounding area, not just the marketed layout, to independently assess future development trajectory and adjoining land-use risk | V | Self — site visit beyond the layout boundary |
| 13.3 | Cross-check the developer's or seller's claims against neighbours or long-term local residents, who often know the parcel's actual dispute history | V | Self — unaccompanied conversation with neighbours/local residents |
| 13.4 | Use a local, independent revenue-side lawyer for the title search — not the developer's or seller's empanelled lawyer | V | Third-party — independent lawyer's title-search report |

## Walk-away triggers

Any one of these, on its own, is a strong signal to pause the transaction until independently resolved — even if every other item checks out:

- Land is on Telangana's 22-A prohibited list, or is assigned/government/Inam/Wakf land
- Seller pressures for unusually fast registration or discourages an independent title search
- Price significantly below the area's sub-registrar guideline value with no clear explanation
- Layout exceeds the RERA threshold but carries no RERA registration
- Promised roads, drainage, or electricity infrastructure exist only on the layout plan, not on the ground
- Any request to pay a large cash component outside the registered sale consideration
- Plot is landlocked with no recorded legal right-of-way
- Seller cannot produce an unbroken 30-year EC or explain a gap in the title chain

## Guardrails

- This skill is a screening aid, not a substitute for an independent revenue-side lawyer, a licensed surveyor, or a chartered accountant. Say so plainly in any report, and recommend professional review before registration regardless of how clean the tracker looks.
- Land title risk in Telangana is disproportionately about chain-of-title gaps and land classification, not physical condition — resist the temptation to spend equal effort across all 13 sections. Weight your attention toward Sections 1, 2, and 4.
- No document uploaded for an item means it stays ⬜ Open. Never infer a pass from silence, from the absence of a red flag, or from the buyer's confidence.
- If a live portal check conflicts with a document the buyer trusts, report both findings plainly and let the buyer see the conflict — don't resolve it on their behalf.
- Site-visit-only items (physical boundary walk, infrastructure walk, monsoon check) stay Open until the buyer reports back from an actual visit.
- Standards cited (30-year EC, RERA plotted-development threshold, 1% TDS above ₹50 lakh) are general benchmarks current as of the checklist's creation — note to the buyer that exact figures and thresholds should be confirmed against current regulations, since tax and RERA rules can change.
