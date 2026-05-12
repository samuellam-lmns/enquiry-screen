# enquiry-screen

Screens any inbound cold enquiry — investors, distribution partners, channel partners, technology partners, or anyone proposing a formal relationship — for legitimacy and fit before any team member invests time engaging.

## What it does

Takes a raw inbound enquiry (name, company, email, phone, message) and runs a **7-layer research protocol** that cross-checks every significant claim against at least two independent sources. Outputs a structured verdict with all sources cited and an HTML brief.

## When to use it

Any time you receive unsolicited outreach proposing a business relationship. Especially useful for:

- **Investors** — VC, private equity, family office, angel, or anyone offering capital
- **Distribution partners** — claiming to sell into your target market or customer base
- **Channel partners** — resellers, referral partners, or intermediaries proposing a commercial arrangement
- **Technology partners** — platforms or vendors proposing an integration or co-sell
- **Strategic alliances** — anyone proposing a formal partnership, joint venture, or collaboration

Common sources: website contact forms, cold LinkedIn messages, cold emails, intermediary referrals.

## The 7 layers

| Layer | What it checks |
|---|---|
| 1. Individual identity | Are the named people findable, consistent, real? |
| 2. Contact channels | Do the email/phone match a legitimate firm? |
| 3. Entity verification | Is the company properly registered? |
| 4. Registered address | Physical presence or mail-drop? |
| 5. Track record | Any disclosed deals, clients, or partnership history? |
| 6. Fraud/regulatory check | BaFin, FCA, SEC, ASIC, scam databases |
| 7. Lumonus fit | Right sector, stage, model, and geography? |

## Verdict

```
VERDICT:      🔴 RED / 🟡 AMBER / 🟢 GREEN
LUMONUS FIT:  POOR / POSSIBLE / STRONG
```

RED = do not engage. AMBER = proceed with caution, require verification. GREEN = legitimate.

## How to invoke

```
/enquiry-screen
```

Then paste the full enquiry text. The skill will extract the key details and run the protocol.

## Cross-check guarantee

Every significant claim is verified by 2+ independent sources. Findings are reported per layer with live links — no aggregated verdicts that hide mixed findings.

## Lumonus and the radiation oncology ecosystem

Lumonus is an agent-native radiation oncology intelligence platform. Understanding the ecosystem helps interpret Layer 7 fit assessments.

**What Lumonus does:** Orchestrates the full patient journey — referral intake, consult prep, treatment planning, revenue cycle, and follow-up — for radiation oncology departments inside hospitals and cancer centres. Primary market is US Integrated Delivery Networks (IDNs) and community hospital systems, with growing operations in Australia.

**The ecosystem — relevant companies and categories:**

| Category | Examples | Relevance to Lumonus |
|---|---|---|
| Oncology Information Systems (OIS) | Varian ARIA, Elekta Mosaiq | Core workflow systems Lumonus integrates with |
| Treatment Planning Systems (TPS) | RaySearch RayStation, Varian Eclipse, Elekta Monaco | Downstream recipients of Lumonus plan directives |
| Linac manufacturers | Varian (Siemens Healthineers), Elekta, Accuray, ViewRay | Hardware vendors in the care pathway |
| EHR / hospital systems | Epic, Oracle Health (Cerner) | Upstream referral and patient record sources |
| Revenue cycle / billing | R1 RCM, Omega Healthcare, nThrive | Adjacent to Lumonus's RCM automation capabilities |
| Imaging / radiology | Philips, GE HealthCare, Siemens Healthineers | PACS/imaging systems in the diagnostic pathway |
| AI oncology platforms | Various health tech startups | Potential partners, competitors, or acquirers |
| Health system operators | IDNs, community hospitals, cancer centre networks | Lumonus's buyers — channel partners often have relationships here |

**Relevant investors** are typically health tech VCs, MedTech growth funds, or AI-focused funds with demonstrated healthcare portfolios. Lumonus raises equity, not debt. Geographic focus: US and Australia.

**Red flags for fit:** investors or partners with no health tech history, no oncology or clinical software exposure, wrong geography, or proposing structures (loans, licensing fees, exclusivity) incompatible with a venture-backed SaaS model.

---

## Why this exists

Most due diligence tools (Keye, CENTRL, ToltIQ, Vantager) solve buyside DD — screening opportunities you're actively pursuing. None address the reverse: a company screening unsolicited inbound outreach for legitimacy before committing team time to a call. Cold enquiries from unverified parties — whether investors, distributors, or partners — carry real risk: wasted time, data exposure, and reputational harm from engaging bad actors.
