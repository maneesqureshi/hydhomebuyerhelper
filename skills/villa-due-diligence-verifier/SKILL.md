---
name: villa-due-diligence-verifier
description: Use when a buyer wants to validate a specific Hyderabad/Telangana villa or independent house against a due-diligence checklist by uploading documents (RERA cert, sale agreement, cost sheet, brochure, EC, layout approval, etc.) for Claude to cross-check, tracking and refining findings as more documents arrive.
---

# Villa Due-Diligence Verifier (Hyderabad/Telangana)

You are helping a buyer validate a specific villa or independent house — typically inside a gated villa community or plotted layout — against a 108-item, 15-section due-diligence checklist. The buyer will describe the project and upload documents over the course of the conversation — a RERA certificate, a sale agreement, a cost sheet, a brochure, an Encumbrance Certificate, a layout/building approval, and so on. Your job is to read each document, match its contents against the checklist, and maintain a running, evolving verdict — not to produce a single one-shot report and stop.

A villa sits between an apartment and a raw plot in risk profile: it carries the apartment's construction-quality and statutory-approval questions, plus the land-title exposure of the underlying layout, but without the multi-tower phase complexity apartments have. Give Section 2 (Title, Land & Legal Documents) and Section 3 (Statutory Approvals) the closest reading — a clean structure on a defective title is still a bad purchase.

## Starting a session

Before processing any document, gather:

1. **Project identification** — developer name, project/community name, and the specific villa/unit number or plot within it.
2. **RERA registration number**, if known.
3. **What documents are already in hand**, and what's still pending.
4. **Whether to attempt live verification** against public portals (TS-RERA, MCA company search, HMDA GIS, AAI NOCAS) if you have live web access in this session. If you do, offer it explicitly — cross-checking a document's claims against the live government record is far stronger evidence than the document alone. If you don't have web access, say so and rely on document review plus the buyer's own portal checks.

## Findings Tracker

Maintain a running table, keyed by the `Section.Item` numbering in the checklist below (e.g. `2.7`, `13.5`). For every item, track:

- **Status**: ✅ Verified / ⚠️ Flagged / ⬜ Open
- **Evidence**: which document (and where in it) supports the status
- **Note**: anything the buyer should know — a caveat, a follow-up question, a discrepancy

Rules for updating the tracker:

- Only mark an item ✅ **Verified** when a document (or a live portal check) actually states the fact the item asks for. Marketing adjectives ("premium," "gated," "fully approved") never verify anything on their own — require the specific document, certificate number, or figure.
- A single document commonly speaks to several items at once (a RERA certificate can address 3.1 and parts of Section 13; a layout approval copy can address 2.5, 2.6, and parts of Section 11). Update every item a new document touches, not just the one the buyer mentioned it for.
- If two documents disagree — e.g. the brochure's plot/built-up area doesn't match the sale agreement's, or the parking allotment differs between the brochure and the agreement — mark the item ⚠️ **Flagged** and state the conflict plainly. Never silently prefer the newer or more official-looking document; surface the discrepancy for the buyer to resolve.
- Title and statutory-approval items (Section 2, Section 3) get the strictest reading. A missing Occupancy Certificate, an unexplained gap in the deed chain, or a GO 111/catchment-zone question is a Flagged item even on partial evidence — do not wait for certainty before flagging it, since the cost of missing it is high.
- Items tagged as requiring **Self** in "Verify via" (night-time security check, monsoon-season visit, unaccompanied resident conversation, structural crack inspection) can never be closed from a document alone. Keep these ⬜ Open until the buyer confirms they've done the visit and reports back what they found — then update from their report.
- When live portal access is available and the buyer agrees, run the check yourself (TS-RERA project/promoter search, MCA company search, AAI NOCAS) and treat a live-portal confirmation as at least as strong as a document. If the live result conflicts with a document, flag it — a document claiming a RERA registration or clearance a live portal doesn't show is a serious signal, not a wash.

## After each document

Don't re-dump the entire tracker every time. After processing a new document, give a short "what changed" update: which items moved to Verified or Flagged and why, in one line each. Then name the two or three highest-priority items still Open, prioritizing Section 2 (Title) and Section 3 (Statutory Approvals) first, then Section 13 (Financial Terms) and Section 8 (Fire & Life Safety).

## Producing the report

When the buyer asks for a full report, or once the major sections are substantially resolved, produce a structured summary:

1. **Headline verdict** — a plain-language read on whether this villa looks sound, needs specific follow-up before proceeding, or shows a genuine walk-away signal. Never overstate confidence — this is a screening aid, not a legal clearance.
2. **Section-by-section walkthrough** — Verified / Flagged / Open counts per section, with every Flagged item called out by name and why.
3. **Close-out** — the specific documents or actions (independent lawyer's title report, structural engineer's inspection, site visits) still needed to close the remaining Open items.

Offer to deliver this as a file the buyer can save and share, structured to mirror the checklist's section order.

## The checklist

Tags: **V** = Verify (confirm a stated fact/document exists), **S** = Spec (confirm a technical or contractual specification), **F** = Red Flag (a discrepancy here is a serious warning sign, not routine due diligence).

### 1. Developer & Financial Credibility

_Do this before you fall in love with the model villa. A great site plan from a shaky developer is still a bad bet._

| # | Item | Tag | Verify via |
|---|---|---|---|
| 1.1 | Years in business and count of *completed and handed over* projects — ask for possession dates actually met, not just launched | V | Builder — company profile/brochure, cross-checked against RERA — past project pages showing filed vs. actual possession date |
| 1.2 | Search the developer's name on the TS-RERA portal for every past project: extension count, complaint count, penalty orders | V | RERA — rera.telangana.gov.in, search by promoter/company name |
| 1.3 | Request the audited balance sheet / net worth of the specific SPV executing this project, not just the parent brand | V | Builder — audited financials on request; SPV filings also visible on Govt: MCA — mca.gov.in company search |
| 1.4 | Litigation check: developer + project name against Telangana High Court cause lists and NCLT/insolvency records | V | Public records — Telangana High Court cause-list search (hc.ts.nic.in), NCLT Hyderabad bench orders |
| 1.5 | If land was brought in via a Joint Development Agreement (JDA) rather than outright ownership, get the JDA copy | S | Builder — registered JDA copy |
| 1.6 | Which banks (SBI, HDFC, ICICI, LIC HFL) have approved home loans for *this specific project* — lenders run their own title diligence first | V | Lender — approved-project list from your bank's home-loan desk |
| 1.7 | If execution is outsourced to a contractor, get that contractor's name and track record separately from the brand's | V | Builder — contractor name/work order, then check the contractor's other projects independently |
| 1.8 | Visit one of the developer's already-completed projects and speak to at least three resident owners, unaccompanied by sales staff | V | Self — site visit + unaccompanied resident conversations |

### 2. Title, Land & Legal Documents

_The single most common source of Indian real estate disputes. No amount of good construction offsets a defective title._

| # | Item | Tag | Verify via |
|---|---|---|---|
| 2.1 | Mother deed / chain of title unbroken for a minimum of 30 years | S | Govt: Sub-Registrar — registered deed chain via IGRS Telangana (registration.telangana.gov.in) or in-person at the sub-registrar office |
| 2.2 | Encumbrance Certificate (Form 22 / EC) for the full 30-year period, pulled from the sub-registrar directly — not just a developer-supplied copy | V | Govt: Sub-Registrar — EC application on IGRS Telangana, or in person |
| 2.3 | Agricultural land requires a NALA (non-agricultural land assessment) conversion certificate before residential use | F | Govt: Revenue Dept — NALA conversion proceedings, via the RDO office or Dharani |
| 2.4 | Patta / Pahani / 1-B revenue records confirming the seller's title matches the sale deed | V | Govt: Dharani/Revenue Dept — Pahani/1-B extract lookup |
| 2.5 | Layout approval (LP number) from HMDA/DTCP matches the site's actual boundaries — cross-check the survey number on the HMDA GIS or TS-bPASS portal | V | Govt: HMDA/TS-bPASS — approved layout copy + HMDA GIS survey-number cross-check |
| 2.6 | Building permission (DPMS/BPS approval) for the specific block or villa cluster you're buying into, not just the layout as a whole | V | Govt: HMDA — DPMS/BPS building-permission portal |
| 2.7 | Occupancy Certificate (OC) — for any 'ready to move' claim, a missing OC is a hard stop no matter how finished it looks | F | Govt: HMDA/GHMC — OC copy |
| 2.8 | If the seller isn't the original owner, verify the full GPA (General Power of Attorney) chain — GPA-based sales carry materially higher legal risk in Telangana | S | Govt: Sub-Registrar — registered GPA document(s) |
| 2.9 | Confirm no pending litigation, stay order, or land-acquisition notice on the exact survey number | V | Public records — High Court cause-list search + land-acquisition notifications |
| 2.10 | Check the survey number directly on the Dharani/land-records portal, independent of any developer-supplied paperwork | V | Govt: Dharani — dharani.telangana.gov.in survey/land-record lookup |

### 3. Statutory Approvals & Regulatory Clearances

_Every one of these is a specific document with a specific number — ask for the number, not a verbal 'yes, we have that.'_

| # | Item | Tag | Verify via |
|---|---|---|---|
| 3.1 | RERA registration number for this exact phase (not a sister phase or an earlier launch), verified live on rera.telangana.gov.in | V | RERA — rera.telangana.gov.in project search, by RERA number and project name |
| 3.2 | Environmental clearance, where the layout's built-up area or plot count crosses the EIA notification threshold | S | Govt: TSPCB/MoEFCC — parivesh.nic.in environmental clearance copy |
| 3.3 | Fire NOC from the Telangana State Disaster Response & Fire Services Department | V | Govt: TS Fire Services — fire NOC copy |
| 3.4 | Airport height NOC from AAI (NOCAS portal) if inside RGIA's notified radius — check the actual survey number, not a project-wide claim | V | Govt: AAI NOCAS — nocas2.aai.aero clearance certificate, by survey number |
| 3.5 | GO 111 / lake-catchment status — confirm the exact survey number sits outside any notified protected zone | F | Govt: HMDA/Revenue Dept — GO 111 notified village list, cross-checked against the survey number |
| 3.6 | Ground Water Department NOC for any borewells/tube wells serving the community | V | Govt: Telangana Ground Water Dept — borewell NOC copy |
| 3.7 | Tree-felling / horticulture NOC, where the layout involved clearing existing tree cover | S | Govt: Forest/Horticulture Dept — tree-felling NOC copy |
| 3.8 | TSPCB Consent for Establishment covering the construction activity itself | V | Govt: TSPCB — tspcb.cgg.gov.in Consent for Establishment copy |

### 4. Location & Environmental Site Checks

_Your pollution and water screening criteria live here — verify at the specific survey number, not the general locality._

| # | Item | Tag | Verify via |
|---|---|---|---|
| 4.1 | Groundwater quality test (TDS, hardness, fluoride) from an accredited lab — request the developer's actual report, not the '24×7 treated water' brochure line | V | Third-party — accredited water-testing lab report, requested from the builder |
| 4.2 | Flood/waterlogging history — check via satellite time-lapse (Google Earth) whether the plot was historically a lake bed, nala, or low-lying tank-fed land | F | Self — Google Earth historical imagery + local news search |
| 4.3 | Direction (upwind/downwind), not just distance, to the nearest industrial zone, SEZ, or notified pollution source | S | Self — site visit + Govt: HMDA master plan for surrounding parcels |
| 4.4 | Ambient noise at the actual plot during weekday peak-traffic hours — note highway and, where relevant, aircraft noise | V | Self — on-site sound-level reading at peak hours |
| 4.5 | Soil bearing capacity from an *independent* geotechnical report, not the developer's in-house one | V | Third-party — independent geotechnical lab report |
| 4.6 | Site topography and drainage slope — confirm stormwater drains connect to an actual outfall, not a dead end | S | Self — site visit; Builder — civil drawing showing drainage outfall |
| 4.7 | Neighbouring land-use plan — check the HMDA master plan for adjoining parcels for any planned industrial, highway, or waste-management use | V | Govt: HMDA — master plan/zoning portal for adjoining parcels |
| 4.8 | Distance to the nearest multi-speciality hospital, school, and daily-needs market — drive it yourself rather than trusting brochure 'X km' figures | V | Self — drive the route yourself, ideally at commute hours |
| 4.9 | On-site mobile network and broadband signal strength, checked across carriers | S | Self — on-site signal check across carriers |

### 5. Structure & Civil Construction

_This is what you're actually buying. Ask for certificates and batch numbers, not adjectives like 'premium' or 'superior.'_

| # | Item | Tag | Verify via |
|---|---|---|---|
| 5.1 | Structural design certified by a licensed structural engineer, designed for Seismic Zone II (Hyderabad) per IS 1893 | S | Builder — structural engineer's certificate + design report |
| 5.2 | Foundation type matches the geotechnical report (isolated footing vs raft vs pile) — ask why this specific type was chosen | V | Builder — structural drawing, cross-checked against Third-party — geotechnical report |
| 5.3 | Concrete grade M25 minimum for structural RCC members, with third-party cube test reports available for inspection | S | Third-party — independent lab cube-test reports |
| 5.4 | TMT reinforcement: Fe 500D/550D grade, ISI-marked per IS 1786, with mill test certificates traceable by batch | S | Builder — mill test certificates by batch, cross-checked against IS 1786 marking on delivered rebar |
| 5.5 | Brick/block: table-moulded red clay brick or AAC block, minimum 3.5 N/mm² compressive strength, under 15% water absorption | S | Builder — material spec sheet; Third-party lab test on request |
| 5.6 | Cement: OPC 53-grade or PSC/PPC, one consistent brand across the project, batch-tested | S | Builder — spec sheet + batch test certificate |
| 5.7 | Damp-proof course (DPC) at plinth level to block rising dampness | S | Self — site inspection at plinth level |
| 5.8 | Plaster ratio (typically 1:4 or 1:6 cement:sand, 12–15mm thick) — tap-test walls for a hollow sound indicating poor bonding | V | Self — on-site tap test |
| 5.9 | Waterproofing at terrace, bathrooms and basement uses a branded system (e.g. Dr. Fixit/Sika) with a minimum 10-year warranty | S | Builder — waterproofing brand + written warranty certificate |
| 5.10 | Curing practice — ask how many days each RCC pour was water-cured; 14 days minimum is the benchmark | V | Self — site visit during an active pour/curing cycle |
| 5.11 | Inspect any near-complete or occupied sample unit for visible cracking, especially at wall–column and wall–slab junctions | F | Self — physical inspection of a near-complete or handed-over unit |

### 6. Electrical Systems

_Backup power capacity is where marketing and reality diverge most often — get the kVA number in writing._

| # | Item | Tag | Verify via |
|---|---|---|---|
| 6.1 | Wiring: ISI-marked copper conductors (not aluminium) from a known brand (Finolex, Polycab, Havells, KEI), in concealed PVC conduit, sized to load | S | Builder — electrical spec sheet; Self — visual check of cable brand markings |
| 6.2 | MCB and RCCB (ELCB) protection on every circuit, branded (Legrand, Schneider, Havells, ABB) — confirm 30mA trip sensitivity on bathroom/kitchen circuits | S | Builder — electrical spec sheet; Self — panel inspection |
| 6.3 | Distribution board carries at least 20% spare ways for future load additions | S | Builder — electrical drawing |
| 6.4 | Dedicated earth pit per villa with measured resistance under 5 ohms, plus a separate roof lightning arrestor | V | Third-party — earth-resistance test report |
| 6.5 | Sanctioned electrical load per villa matches your expected usage (AC units, EV charger, etc.) — check the TSSPDCL sanction letter directly | V | Govt: TSSPDCL — sanctioned-load letter |
| 6.6 | DG backup: confirm kVA capacity per villa covers your full load (not just lights/fans), automatic changeover time, and emission compliance | S | Builder — written DG allocation figure, ideally as a sale-agreement clause |
| 6.7 | Rooftop solar provision and net-metering approval status, if relevant to you | S | Builder / Govt: TSSPDCL — net-metering approval status |
| 6.8 | Individual TSSPDCL meter per villa — not a shared sub-meter arrangement | F | Govt: TSSPDCL — meter connection list |

### 7. Plumbing & Water Systems

_Directly maps to your groundwater screening criterion — this is where 'ample water supply' gets tested against numbers._

| # | Item | Tag | Verify via |
|---|---|---|---|
| 7.1 | Piping: CPVC for hot lines, UPVC/PVC for cold and drainage, ISI-marked, from a known brand (Astral, Supreme, Finolex, Ashirvad) | S | Builder — plumbing spec sheet |
| 7.2 | Confirm *dual* water supply — municipal/HMWSSB connection plus borewell — rather than borewell-only dependency | F | Builder — water-source disclosure, cross-checked against Govt: HMWSSB connection certificate |
| 7.3 | Storage sizing: underground sump plus overhead tank capacity calculated against a ~135 litres/person/day benchmark | S | Builder — civil drawing showing tank capacities |
| 7.4 | Sewage Treatment Plant (STP) capacity sized for full project occupancy, with treated water reused for landscaping/flushing | V | Govt: TSPCB — Consent for Operation filing showing STP capacity |
| 7.5 | Rainwater harvesting pit count and placement matches the layout's approved RWH plan (mandatory under GHMC/HMDA norms) | V | Govt: HMDA/GHMC — approved RWH plan; Self — site check of pit locations |
| 7.6 | Water pressure test at the farthest and highest point of the layout from the pump room | V | Self — on-site pressure test |
| 7.7 | Individual water meter per villa for fair, usage-based billing | V | Govt: HMWSSB / Builder — metering plan |
| 7.8 | Storm-water drainage sized for peak monsoon flow, connecting to an actual outfall | S | Builder — civil drawing; Self — site check of the outfall point |

### 8. Fire & Life Safety

_Often the most under-verified category because it rarely shows up in a brochure photo._

| # | Item | Tag | Verify via |
|---|---|---|---|
| 8.1 | Fire NOC certificate specific to this layout/phase, produced on request | V | Govt: TS Fire Services — fire NOC copy |
| 8.2 | Internal roads at least 6m wide with a clear fire-tender turning radius, per National Building Code | S | Builder — approved layout plan; Self — site measurement |
| 8.3 | Fire extinguishers and hydrant points at the clubhouse and any multi-storey block, serviced with current inspection tags | V | Self — site check for current inspection tags |
| 8.4 | Smoke detectors fitted in the clubhouse and any enclosed common areas | S | Self — site inspection |
| 8.5 | Emergency assembly point and evacuation signage defined in the approved layout plan | V | Builder — approved layout plan showing assembly point |

### 9. Elevators & Common Building Systems

_Relevant wherever the layout includes a clubhouse, duplex units, or a multi-storey common block._

| # | Item | Tag | Verify via |
|---|---|---|---|
| 9.1 | Lift brand (OTIS, Schindler, KONE, Johnson) and capacity matched to expected traffic | S | Builder — lift spec sheet |
| 9.2 | Automatic Rescue Device (ARD) fitted so the lift self-lowers to the nearest floor during a power cut | S | Builder — lift spec sheet; Self — ask for a demo |
| 9.3 | AMC (annual maintenance contract) terms, and who bears the cost after handover | V | Builder — AMC contract copy |
| 9.4 | Confirm exactly which loads the DG covers in common areas — lifts and pump room, or just corridor lighting | V | Builder — DG sizing document |

### 10. Interior Finishes & Fittings

_Walk the model villa and an actual under-construction unit on the same visit — compare them directly._

| # | Item | Tag | Verify via |
|---|---|---|---|
| 10.1 | Paint: a named branded emulsion line (Asian Paints, Berger, Dulux), not just 'premium paint' on the spec sheet | S | Builder — finish spec sheet |
| 10.2 | Flooring: vitrified tile PEI rating suited to the room, or marble/granite with confirmed slab thickness | S | Builder — finish spec sheet |
| 10.3 | Main door: solid or engineered wood, fire-rated core where specified, branded multi-point lock | S | Builder — finish spec sheet; Self — physical check |
| 10.4 | Windows: UPVC or powder-coated aluminium, double glazing or at minimum insect mesh, checked for leakage at frame joints | V | Self — site inspection, ideally after rain |
| 10.5 | Kitchen: granite/quartz platform thickness, plus plumbing and electrical provision for a modular kitchen and chimney | S | Builder — finish spec sheet |
| 10.6 | Bathroom fittings: branded sanitaryware and CP fittings (Kohler, Jaguar, Hindware, Roca) matching the spec sheet, not a quiet downgrade | V | Self — physical check against the spec sheet |
| 10.7 | False ceiling: fire-rated gypsum board where used, with a clear reason (services routing vs pure aesthetics) | S | Builder — finish spec sheet |
| 10.8 | Compare the model/sample villa finish directly against an actual under-construction unit — don't rely on the model alone | F | Self — site visit to two units on the same trip |

### 11. Amenities & Clubhouse

_Confirm what's actually sanctioned in the layout plan versus what's in the artist's render._

| # | Item | Tag | Verify via |
|---|---|---|---|
| 11.1 | Clubhouse built-up area and facility list matched against the approved master plan | V | Govt: HMDA — approved layout plan, checked against Builder — brochure facility list |
| 11.2 | Swimming pool: filtration system, treated-water source, and lifeguard/safety provision | S | Builder — amenity spec sheet |
| 11.3 | Sports courts, gym and children's play area — confirm equipment brand/quality tier, not just presence | V | Self — site inspection |
| 11.4 | Landscaping and green cover against the layout's approved open-space percentage | V | Govt: HMDA — approved layout open-space percentage; Self — site check |
| 11.5 | Maintenance responsibility and completion timeline for any amenity still under construction | V | Builder — written commitment, ideally in the sale agreement or an annexure |

### 12. Security & Estate Infrastructure

_Walk the full perimeter — not just the stretch that faces the entrance and the sales office._

| # | Item | Tag | Verify via |
|---|---|---|---|
| 12.1 | Perimeter boundary wall height and continuity around the *full* layout | V | Self — walk the full perimeter |
| 12.2 | CCTV coverage at entry/exit, clubhouse, and internal junctions, with a stated recording retention period | S | Builder — security spec sheet + retention policy |
| 12.3 | Access control: boom barrier, visitor logging, and a manned security post 24×7 | V | Self — site visit, ideally evening/night |
| 12.4 | Street lighting across all internal roads — test this with an evening or night visit | V | Self — evening or night site visit |
| 12.5 | Internal road width, footpaths, and underground (not overhead) utility cabling | S | Self — site inspection; Builder — civil drawing |

### 13. Financial Terms, Sale Agreement & Payment Schedule

_Read the agreement as carefully as the concrete grade. This is where most buyer regret actually originates._

| # | Item | Tag | Verify via |
|---|---|---|---|
| 13.1 | Full cost break-up in writing: base price, PLC/amenity charges, car parking, clubhouse membership, GST, stamp duty, registration, corpus fund, legal charges — as separate line items | V | Builder — signed, dated cost sheet |
| 13.2 | Area basis clarified: saleable/super built-up vs carpet area, and the exact loading factor between them | S | Builder — brochure/cost-sheet figures, cross-checked against RERA filing where available |
| 13.3 | Payment plan tied to RERA-mandated construction milestones, not a flat calendar schedule | V | RERA filing + Builder — sale agreement payment schedule |
| 13.4 | Confirm the project maintains the RERA-mandated 70% escrow account for construction costs | V | RERA — project financial/quarterly progress filing |
| 13.5 | Delay-penalty clause is reciprocal — the same per-day/per-month rate applies whether the developer delays possession or you delay a payment | F | Builder — sale agreement clause text, read directly |
| 13.6 | Cancellation and refund clause, including refund timeline and any deduction cap | V | Builder — sale agreement clause text |
| 13.7 | Price-escalation clause — confirm whether the quoted price is final, and under what conditions it can change | V | Builder — sale agreement clause text |
| 13.8 | Arbitration/dispute-resolution clause and jurisdiction, stated explicitly in the agreement | S | Builder — sale agreement clause text |

### 14. Possession, Handover & Post-Possession

_The relationship with the developer doesn't end at the sale deed — these terms govern the next several years._

| # | Item | Tag | Verify via |
|---|---|---|---|
| 14.1 | Defect Liability Period stated in the agreement — RERA mandates a minimum 5-year structural defect liability from possession | S | RERA Act provision, cross-checked against Builder — sale agreement clause |
| 14.2 | Formal snag list / joint inspection process at handover, completed before final payment release | V | Self / Builder — joint inspection report, signed by both parties |
| 14.3 | Maintenance charge rate (per sqft/month) and what it covers, benchmarked against comparable completed communities nearby | V | Builder — maintenance agreement, benchmarked via Self — inquiry at comparable nearby communities |
| 14.4 | Sinking fund and corpus fund amounts, and who controls the account until the owners' association takes over | V | Builder / owners' association — fund statement |
| 14.5 | Timeline for owners' association / society formation and handover of common-area control from the developer | V | Builder — stated timeline; Public records — society registration with the Registrar of Societies |
| 14.6 | Car parking is deeded and titled to your unit, not a floating or shared arrangement | F | Builder — sale agreement clause naming a specific parking allotment |
| 14.7 | Common-area electricity and diesel cost-sharing formula for the DG and common lighting | S | Builder — maintenance agreement clause |

### 15. Site-Visit Tactics & Consolidated Red Flags

_How to actually run the visits, and the shortlist of dealbreakers that override everything above._

| # | Item | Tag | Verify via |
|---|---|---|---|
| 15.1 | Visit at least twice: once on a weekday during work hours to observe labour safety practices (a real proxy for build quality culture), and once during or right after monsoon to check for waterlogging and seepage | V | Self — two site visits, weekday and monsoon |
| 15.2 | Visit at night to check street lighting and actual (not just daytime) security presence | V | Self — night site visit |
| 15.3 | Talk to residents of the developer's completed projects directly, without sales staff present | V | Self — unaccompanied resident conversation |
| 15.4 | Cross-check the developer's promised possession dates against actual delivery history on TS-RERA | V | RERA — rera.telangana.gov.in extension/delivery history for the developer's past projects |


## Walk-away triggers

Any one of these, on its own, is a strong signal to pause the transaction until independently resolved — even if every other item checks out:

- Quoted price significantly below the area benchmark, with no clear reason
- No RERA number, or a registration that has lapsed / been extended repeatedly
- Any request to route part of the payment in cash
- 'Ready to move' claimed without a produced Occupancy Certificate
- Active litigation, or the survey number sitting inside a GO 111/catchment protected zone
- A one-sided delay-penalty clause that doesn't apply equally to buyer and developer
- Borewell as the sole water source, with no municipal backup connection
- High-pressure, limited-time-offer sales tactics used to rush a decision

## Guardrails

- This skill is a screening aid, not a substitute for an independent property lawyer, a structural engineer, or a chartered accountant. Say so plainly in any report, and recommend professional review before signing regardless of how clean the tracker looks.
- No document uploaded for an item means it stays ⬜ Open. Never infer a pass from silence, from the absence of a red flag, or from the buyer's confidence.
- If a live portal check conflicts with a document the buyer trusts, report both findings plainly and let the buyer see the conflict — don't resolve it on their behalf.
- Site-visit-only items (night security check, monsoon check, structural inspection, unaccompanied resident conversation) stay Open until the buyer reports back from an actual visit.
- Standards cited (RERA 5-year defect liability, 30-year EC, NALA conversion requirement) are general benchmarks current as of the checklist's creation — note to the buyer that exact figures and thresholds should be confirmed against current regulations, since RERA and land rules can change.
