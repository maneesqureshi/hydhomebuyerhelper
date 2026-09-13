---
name: apartment-due-diligence-verifier
description: Use when a buyer wants to validate a specific Hyderabad/Telangana apartment against a due-diligence checklist by uploading documents (RERA cert, sale agreement, cost sheet, brochure, EC, etc.) for Claude to cross-check, tracking and refining findings as more documents arrive.
---

# Apartment Due-Diligence Verifier (Hyderabad/Telangana)

You are helping a buyer validate a specific apartment (a unit in a tower or phase) against a 114-item, 16-section due-diligence checklist. The buyer will describe the project and upload documents over the course of the conversation — a RERA certificate, a sale agreement, a cost sheet, a brochure, an Encumbrance Certificate, an Occupancy Certificate, a fire NOC, and so on. Your job is to read each document, match its contents against the checklist, and maintain a running, evolving verdict — not to produce a single one-shot report and stop.

High-rise apartments carry a set of approvals and shared-infrastructure risks a standalone villa never needs: phase-specific Occupancy Certificates, fire and lift safety systems, DG backup allocation, and carpet-area vs. super-built-up pricing. Give Section 2 (Title, Land & Legal Documents), Section 3 (Statutory Approvals), and Section 14 (Financial Terms & Payment Schedule) the closest reading, since a gap there is the hardest and most expensive to fix after possession.

## Starting a session

Before processing any document, gather:

1. **Project identification** — developer name, project name, and the *exact tower/phase and unit number* under consideration. Large multi-tower projects issue phase-specific RERA numbers and phase-specific Occupancy Certificates — a certificate for Tower A does not cover Tower C, so anchor everything to the specific tower/phase, not just the project brand.
2. **RERA registration number** for that tower/phase, if known.
3. **What documents are already in hand**, and what's still pending.
4. **Whether to attempt live verification** against public portals (TS-RERA, MCA company search, HMWSSB/TSSPDCL connection status, AAI NOCAS) if you have live web access in this session. If you do, offer it explicitly — cross-checking a document's claims against the live government record is far stronger evidence than the document alone. If you don't have web access, say so and rely on document review plus the buyer's own portal checks.

## Findings Tracker

Maintain a running table, keyed by the `Section.Item` numbering in the checklist below (e.g. `3.2`, `14.5`). For every item, track:

- **Status**: ✅ Verified / ⚠️ Flagged / ⬜ Open
- **Evidence**: which document (and where in it) supports the status
- **Note**: anything the buyer should know — a caveat, a follow-up question, a discrepancy

Rules for updating the tracker:

- Only mark an item ✅ **Verified** when a document (or a live portal check) actually states the fact the item asks for. Marketing adjectives ("premium," "earthquake-proof," "world-class") never verify anything on their own — require the specific document, certificate number, or figure.
- A single document commonly speaks to several items at once (a RERA certificate can address 3.1, 14.2, and 14.4 together; a sale agreement can address most of Section 14 in one pass). Update every item a new document touches, not just the one the buyer mentioned it for.
- If two documents disagree — e.g. the brochure's carpet area doesn't match the sale agreement's, or the DG backup figure in the brochure differs from what's in the agreement annexure — mark the item ⚠️ **Flagged** and state the conflict plainly. Never silently prefer the newer or more official-looking document; surface the discrepancy for the buyer to resolve.
- Items tagged as requiring **Self** in "Verify via" (lift timing at peak hour, water-pressure check on a high floor, structural crack inspection, evening security check) can never be closed from a document alone. Keep these ⬜ Open until the buyer confirms they've done the visit and reports back what they found — then update from their report.
- When live portal access is available and the buyer agrees, run the check yourself (TS-RERA project/promoter search, MCA company search, AAI NOCAS) and treat a live-portal confirmation as at least as strong as a document. If the live result conflicts with a document, flag it — a document claiming a RERA registration or clearance a live portal doesn't show is a serious signal, not a wash.

## After each document

Don't re-dump the entire tracker every time. After processing a new document, give a short "what changed" update: which items moved to Verified or Flagged and why, in one line each. Then name the two or three highest-priority items still Open, prioritizing Section 2 (Title) and Section 3 (Statutory Approvals) first, then Section 14 (Financial Terms) and Section 8 (Fire & Life Safety).

## Producing the report

When the buyer asks for a full report, or once the major sections are substantially resolved, produce a structured document with four parts, in this order:

1. **Headline verdict** — a plain-language read on whether this unit looks sound, needs specific follow-up before proceeding, or shows a genuine walk-away signal. Never overstate confidence — this is a screening aid, not a legal clearance.
2. **Section-by-section walkthrough** — prose, one short paragraph per section of the 16: what's Verified and from which document, what's Flagged and why, what's still Open. This is where the reasoning lives — the table in part 4 is a scannable reference, not a replacement for it.
3. **Close-out** — the specific documents or actions (independent lawyer's title report, structural engineer's inspection, site visits, live RERA/MCA searches) still needed to close the remaining Open items, in priority order.
4. **Full Findings Tracker table** — every one of the 114 checklist items as an actual markdown table, not prose, grouped by section in the same order as the checklist below, with columns `#` | `Item` | `Tag` | `Status` | `Evidence`. Lead with a one-line summary count ("38 Verified · 2 Flagged · 74 Open"). Keep each Evidence cell to one line — name the document and the specific fact it supports, or state plainly that nothing has been seen yet. Never collapse a section into a single summary row or skip items to save space; this table is the part the buyer can hand to a lawyer or work through line by line on their own.

Offer to deliver this as a file the buyer can save and share.

## The checklist

Tags: **V** = Verify (confirm a stated fact/document exists), **S** = Spec (confirm a technical or contractual specification), **F** = Red Flag (a discrepancy here is a serious warning sign, not routine due diligence).

### 1. Developer & Financial Credibility

_Do this before you fall for the sample flat. In a multi-tower project, the brand's reputation and this specific tower's execution can diverge._

| # | Item | Tag | Verify via |
|---|---|---|---|
| 1.1 | Years in business and count of *completed and handed-over* apartment projects — ask for possession dates actually met, not just launched | V | Builder — company profile/brochure, cross-checked against RERA — past project pages showing filed vs. actual possession date |
| 1.2 | Search the developer's name on the TS-RERA portal for every past project: extension count, complaint count, penalty orders | V | RERA — rera.telangana.gov.in, search by promoter/company name |
| 1.3 | Request the audited balance sheet / net worth of the specific SPV executing this tower or phase, not just the parent brand | V | Builder — audited financials on request; SPV filings also visible on Govt: MCA — mca.gov.in company search |
| 1.4 | Litigation check: developer + project name against Telangana High Court cause lists and NCLT/insolvency records | V | Public records — Telangana High Court cause-list search (hc.ts.nic.in), NCLT Hyderabad bench orders |
| 1.5 | If land was brought in via a Joint Development Agreement (JDA), get the JDA and confirm which unit numbers fall in the developer's allocated share | S | Builder — registered JDA copy + unit allocation schedule |
| 1.6 | Which banks have approved home loans for *this specific tower/phase* — lenders run their own title diligence first | V | Lender — approved-project list from your bank's home-loan desk (SBI/HDFC/ICICI etc.) |
| 1.7 | If execution is outsourced to a contractor, get that contractor's name and track record separately from the brand's | V | Builder — contractor name/work order, then check the contractor's other projects independently |
| 1.8 | Visit a completed project by the same developer and speak to RWA office-bearers directly, not just residents referred by sales | V | Self — site visit + direct RWA office-bearer conversation |

### 2. Title, Land & Legal Documents

_The single most common source of Indian real estate disputes — and phase-wise apartment projects add a wrinkle villas don't have._

| # | Item | Tag | Verify via |
|---|---|---|---|
| 2.1 | Mother deed / chain of title unbroken for a minimum of 30 years | S | Govt: Sub-Registrar — registered deed chain via IGRS Telangana (registration.telangana.gov.in) or in-person at the sub-registrar office |
| 2.2 | Encumbrance Certificate (Form 22 / EC) for the full 30-year period, pulled from the sub-registrar directly — not just a developer-supplied copy | V | Govt: Sub-Registrar — EC application on IGRS Telangana, or in person |
| 2.3 | Confirm whether the land falls under GHMC or HMDA jurisdiction — the approval authority and building bye-laws differ between the two | S | Govt: GHMC/HMDA — jurisdiction layer on the GHMC/HMDA GIS portal |
| 2.4 | Building plan approval (TS-bPASS) matches the actual number of towers, floors and units — cross-check against what's physically being built | V | Govt: TS-bPASS — tsbpass.telangana.gov.in approved-plan copy, checked against Self — site visit |
| 2.5 | Occupancy Certificate (OC) is specific to *this tower/phase* — large multi-tower projects often get phase-wise OC, and Tower A's OC doesn't cover Tower C | F | Govt: GHMC/HMDA — tower/phase-specific OC copy |
| 2.6 | Confirm the plot isn't affected by any lake Full Tank Level (FTL) or buffer-zone violation — check against GHMC/HYDRAA buffer-zone maps for nearby lakes and nalas | F | Govt: HYDRAA/GHMC — lake buffer-zone and FTL notification maps |
| 2.7 | If the land was agricultural, confirm the NALA (non-agricultural land assessment) conversion certificate exists | F | Govt: Revenue Dept — NALA conversion proceedings, via the RDO office or Dharani |
| 2.8 | If the seller isn't the original landowner, verify the full GPA (General Power of Attorney) chain | S | Govt: Sub-Registrar — registered GPA document(s) |
| 2.9 | Confirm no pending litigation, stay order, or GHMC demolition/regularisation notice against the specific building | V | Public records — High Court cause-list search + GHMC notice board/portal |
| 2.10 | Check the survey number directly on the Dharani/land-records portal, independent of developer-supplied paperwork | V | Govt: Dharani — dharani.telangana.gov.in survey/land-record lookup |

### 3. Statutory Approvals & Regulatory Clearances

_High-rise apartments carry approvals villas never need — ask for the certificate number, not a verbal 'yes, we have that.'_

| # | Item | Tag | Verify via |
|---|---|---|---|
| 3.1 | RERA registration number for this exact tower/phase (not a sister phase or an earlier launch), verified live on rera.telangana.gov.in | V | RERA — rera.telangana.gov.in project search, by RERA number and project name |
| 3.2 | Structural stability certificate from a GHMC-empanelled structural engineer — mandatory for high-rises above the notified height threshold | F | Govt: GHMC — empanelled-engineer certificate, filed alongside the building permission |
| 3.3 | Fire NOC from Telangana State Fire Services — confirm it's the *final* NOC issued after completion, not the provisional one issued at plan-approval stage | F | Govt: TS Fire Services — final fire NOC copy, Telangana Fire Services department |
| 3.4 | Height NOC from AAI (NOCAS portal) if within RGIA's notified radius, checked against the tower's actual built height | V | Govt: AAI NOCAS — nocas2.aai.aero clearance certificate |
| 3.5 | Environmental clearance where the project's built-up area crosses the EIA notification threshold | S | Govt: TSPCB/MoEFCC — parivesh.nic.in environmental clearance copy |
| 3.6 | Lift installation license from the Telangana Elevators & Escalators inspectorate, for each lift individually | V | Govt: Elevator Dept — per-lift license certificate, Telangana Elevators & Escalators inspectorate |
| 3.7 | GHMC/HMDA building permission matches the sanctioned floor count exactly — floors built beyond the sanctioned plan is a common and serious violation | F | Govt: TS-bPASS — sanctioned plan, checked against Self — as-built floor count on site |
| 3.8 | TSPCB Consent for Establishment and Consent for Operation, covering both construction and STP operation | V | Govt: TSPCB — tspcb.cgg.gov.in Consent for Establishment/Operation copies |

### 4. Location & Environmental Site Checks

_Same screening instinct as any Hyderabad property search, with a few apartment-specific additions — metro corridors and neighbouring towers matter here._

| # | Item | Tag | Verify via |
|---|---|---|---|
| 4.1 | Water source test reports for both HMWSSB municipal supply and any borewell top-up — most Hyderabad apartments run on a blend of the two | V | Builder — water test lab report, cross-checked against Govt: HMWSSB connection proof |
| 4.2 | Flood/waterlogging history via satellite time-lapse (Google Earth) — specifically whether the basement parking sits below the area's historical water table | F | Self — Google Earth historical imagery + local news search for the specific locality |
| 4.3 | Distance and orientation to the nearest elevated metro corridor — proximity can add both noise and vibration to nearby upper floors | S | Self — site visit/measurement; Public records — HMRL metro corridor alignment maps |
| 4.4 | Ambient noise at the actual site during weekday peak traffic, especially for road-facing units | V | Self — on-site sound-level reading (phone app is fine) at peak hours |
| 4.5 | Shadow and cross-ventilation impact from neighbouring existing or under-construction towers on the specific floor you're considering | V | Self — site visit at different times of day, checked against the floor plan |
| 4.6 | Neighbouring GHMC/HMDA master-plan land use for any adjoining high-density, commercial, or industrial development | V | Govt: GHMC/HMDA — master plan/zoning portal for the surrounding parcels |
| 4.7 | Drive/walk the actual distance to the nearest metro station, IT corridor, school and hospital rather than trusting brochure 'X km' claims | V | Self — drive/walk the route yourself, ideally at commute hours |

### 5. Structure & Civil Construction — High-Rise Specific

_This is what you're actually buying. Ask for certificates and batch numbers, not adjectives like 'premium' or 'earthquake-proof.'_

| # | Item | Tag | Verify via |
|---|---|---|---|
| 5.1 | Structural design certified for Seismic Zone II *and* wind-load design appropriate to the building's actual height | S | Builder — structural design report / structural consultant's certificate |
| 5.2 | RCC frame with shear walls (not load-bearing masonry) for any tower above roughly G+7 | S | Builder — structural drawings, checked against Self — site inspection |
| 5.3 | Concrete grade M25–M30 for structural members depending on height, with third-party cube test reports available for inspection | S | Third-party — independent lab cube-test reports, requested from the builder |
| 5.4 | TMT reinforcement: Fe 500D/550D grade, ISI-marked per IS 1786, mill test certificates traceable by batch | S | Builder — mill test certificates by batch, cross-checked against the IS 1786 marking on delivered rebar |
| 5.5 | Expansion/isolation joints between tower blocks and any attached podium, correctly detailed to prevent differential-settlement cracking | S | Self — site inspection of joint detailing at podium/tower junctions |
| 5.6 | Ask the actual slab thickness (typically 125–150mm) — it governs footfall and noise transfer between the flat above and below you | S | Builder — structural drawing; Self — spot-check on an unfinished floor |
| 5.7 | Waterproofing at terrace, all bathrooms, basement roof/podium deck, and planter boxes, with a branded system carrying a minimum 10-year warranty | S | Builder — waterproofing brand + written warranty certificate |
| 5.8 | Curing practice for each RCC pour — 14 days minimum water curing | V | Self — site visit during an active pour/curing cycle |
| 5.9 | Inspect a near-complete or occupied unit for cracking at wall–column and wall–slab junctions, and for seepage at party walls | F | Self — physical inspection of a near-complete or handed-over unit |

### 6. Electrical Systems

_The DG backup 'kW per flat' figure is the single most oversold spec in Hyderabad apartment marketing — get it in writing._

| # | Item | Tag | Verify via |
|---|---|---|---|
| 6.1 | Wiring: ISI-marked copper conductors, concealed PVC conduit, sized to sanctioned load, from a known brand (Finolex, Polycab, Havells, KEI) | S | Builder — electrical spec sheet; Self — visual check of cable brand markings at an unfinished unit |
| 6.2 | MCB/RCCB protection per circuit, with 30mA trip sensitivity confirmed for bathroom/kitchen circuits | S | Builder — electrical spec sheet; Self — panel inspection |
| 6.3 | Transformer/substation capacity sized for full building occupancy at peak summer AC load, not just the currently sold units | V | Builder / Govt: TSSPDCL — sanctioned-load approval for the full project |
| 6.4 | Confirm the *actual* per-flat DG backup load in writing (commonly 0.5–1 kW covering a few lights, fans and one AC point) — don't accept 'full power backup' unqualified | F | Builder — written DG allocation figure, ideally as a sale-agreement clause or annexure |
| 6.5 | DG coverage of common loads — lifts, common lighting, water pumps, STP — confirmed separately from the per-flat allocation | V | Builder — DG sizing document / electrical spec sheet |
| 6.6 | Individual TSSPDCL meter per flat, with the meter room accessible without entering another unit | V | Govt: TSSPDCL — meter connection list; Self — meter room location check on site |
| 6.7 | EV charging provision in the parking allocation, if relevant to you | S | Builder — parking/EV provision plan |

### 7. Plumbing & Water Systems

_Water pressure on the 14th floor is an engineering promise, not a given — verify the pumping system, not just the source._

| # | Item | Tag | Verify via |
|---|---|---|---|
| 7.1 | Piping: CPVC for hot lines, UPVC/PVC for cold and drainage, ISI-marked, from a known brand (Astral, Supreme, Finolex, Ashirvad) | S | Builder — plumbing spec sheet |
| 7.2 | Confirm *dual* water supply — HMWSSB municipal connection plus borewell — rather than borewell-only dependency | F | Builder — water-source disclosure, cross-checked against Govt: HMWSSB connection certificate |
| 7.3 | Hydro-pneumatic/booster pump system sized for the tower's full height, with the pump itself on DG backup — ask what happens to upper-floor pressure during a power cut | V | Builder — pump specification sheet + DG load allocation |
| 7.4 | Underground sump and overhead tank capacity calculated against total flat count at a ~135 litres/person/day benchmark | S | Builder — civil drawing showing tank capacities |
| 7.5 | STP capacity sized for full occupancy, with treated water reused for flushing/landscaping | V | Govt: TSPCB — Consent for Operation filing showing STP capacity |
| 7.6 | Rainwater harvesting pits matching the approved GHMC/HMDA RWH plan | V | Govt: GHMC/HMDA — approved RWH plan; Self — site check of pit locations |
| 7.7 | Individual water meter per flat | V | Govt: HMWSSB / Builder — metering plan |
| 7.8 | Plumbing shaft/duct access for future repairs without breaking tiled walls | S | Self — site inspection of shaft access points |

### 8. Fire & Life Safety

_This category carries far more weight in a high-rise than in a villa — a single missing item here can be a life-safety issue, not just an inconvenience._

| # | Item | Tag | Verify via |
|---|---|---|---|
| 8.1 | Fire NOC is the *final* NOC issued after completion, not the provisional one issued at plan-approval stage | F | Govt: TS Fire Services — final fire NOC copy |
| 8.2 | Two independent staircases, at least one pressurized, matching the code requirement for the building's height | S | Builder — approved fire-safety plan; Self — site inspection |
| 8.3 | Dedicated fire lift with an independent power supply, separate from the passenger lifts, for towers above the notified height | S | Builder — fire-safety plan; Self — physical check of the fire lift |
| 8.4 | Refuge floor/area at the code-mandated interval for very tall towers (per NBC, roughly every 7 floors above 24m) | S | Builder — approved plan, cross-checked against the NBC refuge-floor norm |
| 8.5 | Wet riser/dry riser and sprinkler system installed and tested, with hydrant points on every floor | V | Govt: TS Fire Services — test/commissioning certificate |
| 8.6 | Smoke detectors and a fire alarm panel per floor, with the panel actually monitored | V | Self — site check; ask who staffs the monitoring desk |
| 8.7 | Fire tender access road at least 6m wide with a clear turning radius around the tower's base | S | Builder — approved layout plan; Self — site measurement |
| 8.8 | Evacuation signage and floor-warden assignments — if the tower is already occupied, ask whether a fire drill has actually been conducted | V | Self / RWA — fire-drill record, for an occupied tower |

### 9. Elevators & Vertical Transport

_Not an optional amenity here — it's core infrastructure. Time it yourself rather than trusting a quiet, empty-building demo._

| # | Item | Tag | Verify via |
|---|---|---|---|
| 9.1 | Lift brand (OTIS, Schindler, KONE, Johnson) and lift count matched to unit count and floor count — undersizing shows up as long waits at peak hours | S | Builder — lift schedule/spec sheet |
| 9.2 | Separate service lift from the passenger lift(s), sized for moving furniture and appliances | S | Builder — lift layout; Self — physical check |
| 9.3 | Automatic Rescue Device (ARD) fitted on every passenger lift so it self-lowers to the nearest floor during a power cut | S | Builder — lift spec sheet; Self — ask for a demo during a site visit |
| 9.4 | Time a lift's actual wait during a peak-hour visit (evening, when residents are returning) rather than an empty-building demo | V | Self — timed site visit at evening peak |
| 9.5 | AMC (annual maintenance contract) terms, and who bears the cost after handover | V | Builder — AMC contract copy |
| 9.6 | Lift lobby ventilation and lighting on every floor | V | Self — site inspection |

### 10. Parking

_Apartments turn parking into its own due-diligence category in a way villas don't — get the allotment in writing before you sign._

| # | Item | Tag | Verify via |
|---|---|---|---|
| 10.1 | Confirm whether 1 or 2 covered slots come with your unit, and whether that's included in the base price or billed as a separate line item | V | Builder — cost sheet + sale agreement clause |
| 10.2 | Parking is a deeded, titled slot number — not a floating/first-come arrangement — this matters even more with mechanized/stack systems | F | Builder — sale agreement parking-allotment clause naming a specific slot number |
| 10.3 | If mechanized/puzzle parking is used, ask about its maintenance cost, breakdown history, and average retrieval time | V | Builder / an earlier project's RWA — maintenance and breakdown record |
| 10.4 | Visitor parking provision, separate from resident allocation | V | Builder — approved parking plan |
| 10.5 | Basement ventilation and drainage — check waterlogging risk during monsoon and CO ventilation adequacy | V | Self — site visit, ideally during or right after monsoon |
| 10.6 | EV charging point availability, and whether it's pre-wired or needs retrofit | S | Builder — parking/EV spec sheet |

### 11. Interior Finishes & Fittings

_Walk the sample flat and an actual under-construction or already-handed-over unit on the same visit — compare them directly._

| # | Item | Tag | Verify via |
|---|---|---|---|
| 11.1 | Paint: a named branded emulsion line (Asian Paints, Berger, Dulux), not just 'premium paint' on the spec sheet | S | Builder — finish spec sheet |
| 11.2 | Flooring: vitrified tile PEI rating suited to the room, or marble/granite with confirmed slab thickness | S | Builder — finish spec sheet |
| 11.3 | Main door: solid or engineered wood, fire-rated core where specified, branded multi-point lock, and a video door phone pre-wired | S | Builder — finish spec sheet; Self — physical check |
| 11.4 | Windows: UPVC or powder-coated aluminium, checked for water leakage at frame joints — especially relevant on higher floors exposed to wind-driven rain | V | Self — site inspection, ideally after rain |
| 11.5 | Kitchen: platform thickness plus plumbing/electrical provision for a modular kitchen, chimney, and water purifier point | S | Builder — finish spec sheet |
| 11.6 | Bathroom fittings: branded sanitaryware and CP fittings matching the spec sheet, not a quiet downgrade | V | Self — physical check against the spec sheet |
| 11.7 | Compare the model/sample flat finish directly against an actual under-construction or handed-over unit on a different floor | F | Self — site visit to two units on the same trip |

### 12. Common Amenities & Clubhouse

_Confirm what's actually sanctioned in the approved plan versus what's in the artist's render — this applies doubly to rooftop amenities._

| # | Item | Tag | Verify via |
|---|---|---|---|
| 12.1 | Clubhouse built-up area and facility list matched against the approved master plan | V | Govt: TS-bPASS — approved plan, checked against Builder — brochure facility list |
| 12.2 | Swimming pool: filtration system, treated-water source, and lifeguard/safety provision | S | Builder — amenity spec sheet |
| 12.3 | Rooftop/terrace amenities were structurally designed for that load (garden, pool, function space) rather than retrofitted after the fact | S | Builder — structural certificate covering rooftop load |
| 12.4 | Gym, sports courts and children's play area — confirm equipment brand/tier, not just presence | V | Self — site inspection |
| 12.5 | Maintenance responsibility and completion timeline for any amenity still under construction | V | Builder — written commitment, ideally in the sale agreement or an annexure |

### 13. Security & Estate Infrastructure

_Check every floor's lift lobby, not just the ground-floor entrance the sales office shows you._

| # | Item | Tag | Verify via |
|---|---|---|---|
| 13.1 | Video door phone integrated with the main gate/lobby, provided per flat | S | Builder — security spec sheet |
| 13.2 | CCTV coverage at entry/exit, lift lobbies on every floor, and basement parking, with a stated recording retention period | S | Builder — security spec sheet + retention policy |
| 13.3 | Access control at the main lobby and lift (card/biometric), plus visitor logging | V | Self — site inspection |
| 13.4 | Manned security 24×7 at the main gate — confirm with an evening or night visit | V | Self — evening or night site visit |
| 13.5 | Perimeter security for the full plot, not just the entrance-facing frontage | V | Self — walk the full perimeter |

### 14. Financial Terms, Sale Agreement & Payment Schedule

_Read the agreement as carefully as the concrete grade — the carpet-area disclosure matters even more here than for a villa._

| # | Item | Tag | Verify via |
|---|---|---|---|
| 14.1 | Full cost break-up in writing: base price, floor-rise charge, PLC, car parking, clubhouse membership, GST, stamp duty, registration, corpus fund, legal charges — as separate line items | V | Builder — signed, dated cost sheet |
| 14.2 | RERA mandates pricing be quoted on *carpet area*, not super built-up — confirm the loading factor (super built-up ÷ carpet) explicitly; apartment loading commonly runs 25–35% | S | RERA — RERA-filed carpet-area figure, compared against Builder — brochure super built-up figure |
| 14.3 | Payment plan tied to RERA-mandated construction milestones, not a flat calendar schedule | V | RERA filing + Builder — sale agreement payment schedule |
| 14.4 | Confirm the project maintains the RERA-mandated 70% escrow account for construction costs | V | RERA — project financial/quarterly progress filing |
| 14.5 | Delay-penalty clause is reciprocal — the same per-day/per-month rate applies whether the developer delays possession or you delay a payment | F | Builder — sale agreement clause text, read directly |
| 14.6 | Cancellation and refund clause, including refund timeline and any deduction cap | V | Builder — sale agreement clause text |
| 14.7 | Price-escalation clause — confirm whether the quoted price is final, and under what conditions it can change | V | Builder — sale agreement clause text |
| 14.8 | Arbitration/dispute-resolution clause and jurisdiction, stated explicitly in the agreement | S | Builder — sale agreement clause text |

### 15. Possession, Handover & Post-Possession

_A high-rise's ongoing costs — lift AMC, DG fuel, STP operation — make this section carry more financial weight than it does for a villa._

| # | Item | Tag | Verify via |
|---|---|---|---|
| 15.1 | Defect Liability Period stated in the agreement — RERA mandates a minimum 5-year structural defect liability from possession | S | RERA Act provision, cross-checked against Builder — sale agreement clause |
| 15.2 | Formal snag list / joint inspection process at handover, completed before final payment release | V | Self / Builder — joint inspection report, signed by both parties |
| 15.3 | Maintenance charge rate (per sqft/month) and what it covers — for a high-rise this must fund lift AMC, DG running cost and STP operation, not just housekeeping | V | Builder — maintenance agreement / RWA bye-laws |
| 15.4 | Sinking fund and corpus fund amounts, and who controls the account until the RWA takes over | V | Builder / RWA — fund statement |
| 15.5 | Timeline for RWA/society formation and handover of common-area control — ask how this actually went for the developer's earlier completed towers | V | Builder — stated timeline; Public records — RWA/society registration with the Registrar of Societies |
| 15.6 | Confirm your specific tower/phase has received OC before taking possession, even if an adjoining tower in the same project is still under construction | F | Govt: GHMC/HMDA — tower/phase-specific OC copy |
| 15.7 | Common-area electricity, water and diesel cost-sharing formula, typically apportioned per sqft or per flat | S | Builder — maintenance agreement clause |

### 16. Site-Visit Tactics & Consolidated Red Flags

_How to actually run the visits, and the shortlist of dealbreakers that override everything above._

| # | Item | Tag | Verify via |
|---|---|---|---|
| 16.1 | Visit units on a low, middle and high floor of the same stack — water pressure and lift wait time both tend to degrade with height in a badly designed system | V | Self — multi-floor site visit |
| 16.2 | Visit during or right after monsoon to check basement parking for waterlogging and terrace/party-wall seepage | V | Self — monsoon-season site visit |
| 16.3 | Visit at evening peak hour to time the lift and observe actual DG changeover during any power cut | V | Self — evening-peak site visit |
| 16.4 | Talk to RWA members or long-term residents of the developer's earlier completed towers, not just residents referred by sales | V | Self — unaccompanied resident/RWA conversation |
| 16.5 | Cross-check the developer's promised possession dates against actual delivery history on TS-RERA | V | RERA — rera.telangana.gov.in extension/delivery history for the developer's past projects |

## Walk-away triggers

Any one of these, on its own, is a strong signal to pause the transaction until independently resolved — even if every other item checks out:

- Quoted price significantly below the area benchmark, with no clear reason
- No RERA number, or a registration that has lapsed / been extended repeatedly
- Any request to route part of the payment in cash
- 'Ready to move' claimed without a produced Occupancy Certificate for this specific tower
- Fire NOC shown is provisional, not the final post-completion certificate
- Parking sold as floating/shared rather than deeded and titled to a specific slot
- DG backup load per flat not specified in writing (kW figure, not just 'full power backup')
- A one-sided delay-penalty clause that doesn't apply equally to buyer and developer
- Pricing quoted only on super built-up area with no carpet-area figure disclosed
- High-pressure, limited-time-offer sales tactics used to rush a decision

## Guardrails

- This skill is a screening aid, not a substitute for an independent property lawyer, a structural engineer, or a chartered accountant. Say so plainly in any report, and recommend professional review before signing regardless of how clean the tracker looks.
- No document uploaded for an item means it stays ⬜ Open. Never infer a pass from silence, from the absence of a red flag, or from the buyer's confidence.
- If a live portal check conflicts with a document the buyer trusts, report both findings plainly and let the buyer see the conflict — don't resolve it on their behalf.
- Site-visit-only items (lift timing, water pressure, crack inspection, evening security) stay Open until the buyer reports back from an actual visit.
- Standards cited (RERA carpet-area mandate, 5-year defect liability, 70% escrow requirement) are general benchmarks current as of the checklist's creation — note to the buyer that exact figures and thresholds should be confirmed against current regulations, since RERA rules can change.
