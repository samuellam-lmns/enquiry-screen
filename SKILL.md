---
name: enquiry-screen
description: >
  Screens any inbound enquiry for legitimacy and Lumonus fit — investors, partners, distributors, channel partners, or anyone cold-reaching out proposing a relationship. Use this skill whenever Lumonus receives unsolicited outreach from: claimed investors (PE, VC, family office, private group), distribution or channel partners, technology or integration partners, strategic alliance proposals, referral or reseller propositions, or any party proposing a formal business relationship. Runs a 7-layer research protocol that cross-checks every significant claim against at least two independent sources, surfaces all red flags, and delivers a structured verdict with an HTML brief.

  Trigger on: 'is this investor legit', 'screen this investment enquiry', 'should we engage with this investor', 'check this VC out', 'someone emailed us about investing', 'is this a scam', 'run investor screening', 'due diligence on this enquiry', 'is this investment offer real', 'should I reply to this investor', 'validate this investor', 'assess this partnership enquiry', 'screen this partner', 'is this distributor legit', 'should we engage with this partner', 'someone emailed about a distribution deal', 'check this channel partner', 'screen this collaboration proposal', 'is this partnership offer real', 'summarise this enquiry', 'assess this enquiry'.

  Skip on: internal Lumonus strategy questions, known/existing investors already in the cap table, existing confirmed partners, requests to evaluate whether to accept a term sheet (use exec-brief for that).
---

# Inbound Enquiry Screen

Screens inbound enquiries — investors, distribution partners, channel partners, or any unsolicited partnership proposal — for legitimacy and fit before any Lumonus team member invests time engaging. Runs a 7-layer research protocol with mandatory cross-checking, then produces a structured verdict with all sources cited and an HTML brief.

---

## Guardrails

- Every significant claim must be verified by **2 or more independent sources** before being reported as confirmed. If only one source exists, mark it as **unverified (single source)**.
- Run all web searches **before synthesising findings** — do not form a verdict mid-research.
- Cite every claim with a live URL. Do not cite search engine result pages — fetch and cite the actual source.
- Do not soften or hedge a Red verdict to spare feelings. If it's a scam pattern, call it plainly.
- Lumonus fit is assessed against what Lumonus actually needs, not what the enquirer claims to offer.
- If a layer returns no results, say so explicitly — absence of evidence is itself a data point.

---

## Intake

Extract the following from the enquiry. Ask only for what is missing.

1. **Names** — every individual named (sender + any partners/co-investors mentioned)
2. **Emails** — all email addresses provided (note whether corporate or free-domain)
3. **Phone numbers** — all numbers (note country code vs claimed location)
4. **Company name** — the investment entity being represented
5. **Website/domain** — any URLs provided
6. **Investment claim** — what they claim to offer (structure, size, sectors)
7. **Original message text** — full body of the enquiry

---

## The 7-Layer Research Protocol

Work through each layer sequentially. Do not skip layers. Record findings and sources as you go.

---

### Layer 1 — Individual Identity

**Goal:** Establish whether the named individuals have a genuine, verifiable professional existence.

For each named person:
- Search `"[Full Name]" investor` and `"[Full Name]" [company name]`
- Search LinkedIn (web search for `site:linkedin.com "[Full Name]"`)
- Search for any news coverage, press mentions, or quotes
- Search for the name alongside the company domain

**Cross-check requirement:** A person is considered verified only if they appear in at least 2 independent sources with consistent identity details (role, company, country).

**Red flags:**
- Zero web presence for someone claiming to manage €1M+ deals
- Name not found on the company's own website
- Name used in prior fraud reports
- Name appears only on the company's own website (no third-party corroboration)

---

### Layer 2 — Contact Channel Analysis

**Goal:** Determine whether the contact channels match the claimed professional status.

- Note the email domain: is it a company domain (`@company.com`) or free-domain (`@gmail.com`, `@yahoo.com`, `@hotmail.com`)?
- Cross-check the phone country code against the claimed company location (e.g., +31 = Netherlands, +49 = Germany)
- Check if WhatsApp or Telegram is promoted as the primary contact method
- Verify that the company email domain exists and is active (search the domain, check MX records if needed)

**Red flags:**
- Using Yahoo/Gmail/Hotmail for a multi-million-euro firm
- Company email domain doesn't exist or is unregistered
- Phone country code doesn't match the company's registered location
- WhatsApp pushed as primary contact (harder to audit than email)
- Two different personal email addresses given (sign of ad hoc setup)

---

### Layer 3 — Entity Verification

**Goal:** Confirm the investment entity is a legitimately registered company in its claimed jurisdiction.

- Search the company name + jurisdiction in public registries:
  - Germany: `site:northdata.com`, `site:handelsregister.de`, `site:unternehmensregister.de`
  - UK: `site:find-and-update.company-information.service.gov.uk`
  - Australia: `site:abr.business.gov.au`
  - Netherlands: `site:kvk.nl`
  - Other: Crunchbase, Bloomberg, OpenCorporates
- Confirm: registered name, legal form, registration number, date of incorporation, jurisdiction
- Cross-check the registration details against what the enquirer claimed

**Cross-check requirement:** Registration details must be confirmed in the public registry AND at least one independent data aggregator (Crunchbase, Northdata, OpenCorporates, etc.).

**Red flags:**
- Company cannot be found in public registries
- Registration details don't match what the enquirer stated
- Company is extremely recently incorporated (< 12 months old) with large claimed AUM
- Multiple companies with similar names — enquirer may be impersonating a legitimate entity

---

### Layer 4 — Registered Address

**Goal:** Determine whether the company has a real physical presence or is using a virtual/mail-drop address.

- Search the registered address in Google Maps (street view check)
- Search `"[address]" virtual office` or `"[address]" registered office` or `"[address]" business centre`
- Check sites like Regus, WeWork, Servcorp, MatchOffice for that address
- Note whether multiple unrelated companies share the same address

**Red flags:**
- Address is a known virtual office provider
- Many unrelated companies are registered at the same address
- Address is a residential property for a claimed institutional investor
- Address does not appear to correspond to any actual office building

---

### Layer 5 — Track Record

**Goal:** Verify that the entity has actually deployed capital and has a real deal history.

- Search Crunchbase for the entity and any named partners: disclosed investments, portfolio companies
- Search Tracxn for the entity
- Search news and press for any confirmed transactions, closings, or portfolio announcements
- Search for any named partners' prior investment roles at other firms
- Search `"[company name]" investment` and `"[company name]" portfolio`

**Cross-check requirement:** Any claimed investment must appear in at least 2 sources (e.g., company website AND a portfolio company's press release or Crunchbase entry).

**Red flags:**
- No disclosed investments anywhere (Crunchbase, news, LinkedIn posts)
- Claimed AUM/check size is wildly out of proportion to any verifiable deal history
- Portfolio companies listed on the website don't appear to exist or list the firm as an investor
- Named partners have no prior investment roles at verifiable firms

---

### Layer 6 — Fraud and Regulatory Check

**Goal:** Cross-check against known fraud warnings, regulator blacklists, and scam databases.

Run all of these searches:
- `"[company name]" scam OR fraud OR warning`
- `"[company name]" site:bafin.de` (German financial regulator)
- `"[company name]" site:fca.org.uk/consumers/warning-list` (UK FCA)
- `"[company name]" site:sec.gov` (US SEC enforcement)
- `"[company name]" site:asic.gov.au` (Australian ASIC)
- `"[company name]" site:scamadviser.com`
- `"[company name]" site:scamwarners.com`
- `"[individual name]" fraud OR scam OR lawsuit OR convicted`
- `"[email address]" scam OR fraud` (for both emails provided)
- Check OCCRP (Organised Crime and Corruption Reporting Project) database

**Red flags:**
- Any regulatory warning from BaFin, FCA, SEC, ASIC, or equivalent
- Company or individual named in fraud reports or legal proceedings
- Email address appears in known scam databases
- Pattern matches known advance-fee fraud or pig-butchering scripts

---

### Layer 7 — Lumonus Fit Assessment

**Goal:** Even if the enquirer is legitimate, assess whether they are actually relevant to Lumonus's current needs and strategic context.

First, identify the **enquiry type**: investor / distribution partner / technology partner / channel partner / strategic alliance / other. The fit criteria differ by type.

---

**For investor enquiries:**

- **Sector match:** Lumonus is in radiation oncology / health tech / AI-native clinical software. Does this investor have demonstrated history in health tech, MedTech, SaaS, or AI?
- **Stage match:** Lumonus is a growth-stage, venture-backed company. Is the structure compatible? Check size: €500K is sub-seed; €5–50M is relevant; €100M+ implies a stage Lumonus is not yet at.
- **Structure match:** Lumonus raises equity, not loans or project finance.
- **Geographic relevance:** Lumonus operates in Australia and the US. Is the investor familiar with these markets?
- **Strategic value beyond capital:** Relationships in health systems, hospital groups, or oncology networks? Portfolio companies that could be channel partners or acquirers?

---

**For distribution / channel partner enquiries:**

- **Market access:** Do they operate in radiation oncology, cancer centres, hospital networks, or radiology? Which geographies specifically?
- **Customer base:** Do they have existing relationships with the buyer types Lumonus targets (radiation oncologists, cancer centre administrators, dosimetrists)?
- **Track record:** Have they successfully distributed clinical software before? Any named accounts?
- **Commercial model:** Are their commercial terms (margin, exclusivity, minimum commitments) compatible with Lumonus's go-to-market?
- **Regulatory:** Do they hold relevant local regulatory approvals, or have experience navigating TGA/FDA/CE for medical software?

---

**For technology / integration partner enquiries:**

- **Technical fit:** Does their platform or capability complement Lumonus's stack (DICOM, HL7/FHIR, ARIA, Mosaiq, RIS/PACS integrations, AI inference)?
- **Customer overlap:** Do they serve the same buyer? Is there a clear co-sell or embed opportunity?
- **Strategic positioning:** Does this partnership strengthen Lumonus's moat or dilute focus?
- **Reciprocity:** Is the value exchange clearly mutual, or are they primarily seeking distribution through Lumonus?

---

**For all types:**

- **Red flag pattern:** Does the proposal feel generic (sent to many companies) or specifically targeted at Lumonus's actual situation?
- **Decision-maker:** Is the person reaching out the actual decision-maker, or an intermediary / BD rep with no authority?

---

## Verdict Framework

After completing all 7 layers, issue a verdict:

```
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
VERDICT:        🔴 RED / 🟡 AMBER / 🟢 GREEN
LUMONUS FIT:    POOR / POSSIBLE / STRONG
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

**RED** — Do not engage. One or more of: scam indicators present, entity cannot be verified, contact channels are fraudulent, or known regulatory warning.

**AMBER** — Proceed with caution. Entity appears legitimate but has meaningful gaps (no track record, virtual address, mismatched contact channels). Require verification steps before a call.

**GREEN** — Entity appears legitimate with a verifiable track record and no fraud signals.

**POOR fit** — Even if legitimate, this investor is structurally misaligned with Lumonus (wrong sector, wrong instrument, wrong stage, wrong geography).

**POSSIBLE fit** — Some alignment but not strong. Worth a brief exploratory exchange only.

**STRONG fit** — Real investor, sector-relevant, right stage, right instrument.

---

## Output Format

Deliver findings in this exact structure:

---

### Enquiry Screen: [Sender Name] / [Company Name]
**Date:** [today's date]
**Verdict:** [RED/AMBER/GREEN] | **Lumonus Fit:** [POOR/POSSIBLE/STRONG]

#### Summary
[2–3 sentences. State the verdict, the single strongest piece of evidence, and the recommended action. No hedging.]

#### Red Flags
[Bulleted list of specific red flags found, or "None identified" if clean.]

#### Layer Findings

**Layer 1 — Individual Identity**
[Findings + sources]

**Layer 2 — Contact Channel Analysis**
[Findings + sources]

**Layer 3 — Entity Verification**
[Findings + sources]

**Layer 4 — Registered Address**
[Findings + sources]

**Layer 5 — Track Record**
[Findings + sources]

**Layer 6 — Fraud and Regulatory Check**
[Findings + sources]

**Layer 7 — Lumonus Fit**
[Assessment against sector / stage / structure / geography]

#### Recommended Action
[One of: Do not engage | Request verification before any call | Exploratory exchange only | Worth pursuing — propose a call]

If "Request verification": specify exactly what to request (e.g., "ask them to reply from their registered company email at @klmb-gmbh.de and provide a LinkedIn profile link").

---

## Cross-Check Verification Table

At the end of the report, include a table summarising what was cross-checked:

| Claim | Source 1 | Source 2 | Status |
|---|---|---|---|
| [e.g., Company is registered in Germany] | [link] | [link] | ✅ Verified / ⚠️ Single source / ❌ Unverified |

---

## What "Robust Methodology" Means Here

These constraints are not optional:

1. **No synthesis before research is complete.** Run all searches first. Form the verdict last.
2. **Two sources per claim.** A single website — especially the enquirer's own — is not verification.
3. **Absence is evidence.** If a search returns nothing (no person, no deals, no news), that finding must be reported explicitly.
4. **Live links only.** Do not cite search pages. Fetch the actual source and link to it.
5. **Don't flatten.** If Layer 3 shows the entity is real but Layer 5 shows zero deal history, both findings must appear in full — do not average them into a vague "mostly looks okay."
6. **No courtesy hedging.** If evidence points to a scam, say it clearly. The cost of engaging a fraudulent investor (time, reputation, data exposure) is far higher than the cost of a blunt verdict.

---

## Step 8 — Generate the HTML Brief

After delivering the structured text report, generate a complete HTML brief using the template at `assets/screen-template.html`.

### How to generate

1. Read `assets/screen-template.html`.
2. Fill every `{{PLACEHOLDER}}` with real content from the research. Rules below.
3. Remove all HTML `<!-- comment -->` blocks from the output — they're instructions, not content.
4. Save the output as `[entity-name-slug]-screen.html` in `~/Downloads/` (or the project working directory if more appropriate).
5. Tell the user where it was saved and that it's visible in the preview panel.

### Filling the placeholders

**Hero**
- `HERO_EYEBROW` — "Investment enquiry" or "Cold outreach"
- `HERO_TITLE_LINE1` / `HERO_TITLE_LINE2` — split the entity name across two lines; line 2 renders in purple. For a person + company: line1 = person's name, line2 = company. For a company only: split the name if possible, otherwise put the full name on line2 and the type ("GmbH", "Ltd", "Capital") on line1.
- `HERO_LEDE` — one sentence: who they claim to be and what they offered. No verdict language here.
- `DATE` — today's date, formatted as "12 May 2026"
- `CONTACT_NAME` — the named individual(s) who made contact
- `VERDICT_CLASS` — `verdict-red`, `verdict-amber`, or `verdict-green`
- `VERDICT_LABEL` — "Do not engage", "Proceed with caution", or "Appears legitimate"
- `FIT_LABEL` — "Poor fit", "Possible fit", or "Strong fit"

**Entity snapshot stats (4 stats, 2×2)**
Pick the 4 most concrete facts from the research — registration status, jurisdiction, date incorporated, claimed check size, employee count, address type, etc. Use short values (e.g. "Registered", "Germany", "1988", "Virtual office").

**Quote banner**
- `BANNER_ATTRIBUTION` — sender name + channel + date (e.g. "Marc Ender-Yaron · Website contact form · 12 May 2026")
- `BANNER_QUOTE` — the most revealing line(s) from the actual enquiry. Wrap the specific claim (investment size, sectors, geographic scope) in `<strong>` to highlight in purple.

**Findings tiles (4 tiles)**
Pick the 4 most decisive layer findings. Assign each a status class:
- `finding-ok` — clean result, no concerns
- `finding-warn` — present but with gaps or single-source
- `finding-fail` — failed check, clear problem

For each tile: `TILE_N_STATUS`, `TILE_N_ICON` (Phosphor icon name without `ph-`), `TILE_N_LAYER` (layer name), `TILE_N_TITLE` (sharp finding headline), `TILE_N_BODY` (2–3 sentences with source link if applicable).

Useful icons: `user-circle-check`, `user-circle-minus`, `envelope-simple-x`, `envelope-simple-check`, `building-office`, `map-pin`, `chart-line-down`, `shield-slash`, `shield-check`, `warning`, `magnifying-glass`, `x-circle`, `check-circle`

**Red flags**
- If red flags exist: use the `.flags` list. One `<div class="flag">` per flag, with `f-num` as F1, F2, F3…
- If no red flags: replace the `.flags` block with the `.flags-clear` div (already in the template as a comment).
- Remove whichever block you don't use.

**Cross-check table**
One row per significant claim that was verified (or failed verification). Every row needs: the claim in plain English, Source 1 with a real URL, Source 2 with a real URL (or `—` if only one source), and a status:
- `status-ok` → "✅ Verified"
- `status-warn` → "⚠️ Single source"
- `status-fail` → "❌ Unverified"
- `status-none` → "— No results found"

**Recommendation**
- `RECOMMENDATION_HEADING` — the action in 5 words or fewer: "Do not engage", "Request verification first", "Worth a discovery call"
- `RECOMMENDATION_BODY_1` — why this verdict in 2–3 sentences
- `RECOMMENDATION_BODY_2` — the specific next step, if any (e.g. "If they follow up, ask them to contact you from the registered company email at @domain.com before agreeing to a call.")

### Pre-save checklist

Before saving, verify:
- No `{{PLACEHOLDER}}` strings remain
- No HTML `<!-- comment -->` blocks remain
- Stat grid has exactly 4 stats
- Findings grid has exactly 4 tiles
- `.flags` block OR `.flags-clear` block present — not both
- All source links in the cross-check table are real URLs, not placeholders
- Date filled in both hero-meta and footer
- Title tag reflects the entity name
