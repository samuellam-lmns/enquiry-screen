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

## Why this exists

Most due diligence tools (Keye, CENTRL, ToltIQ, Vantager) solve buyside DD — screening opportunities you're actively pursuing. None address the reverse: a company screening unsolicited inbound outreach for legitimacy before committing team time to a call. Cold enquiries from unverified parties — whether investors, distributors, or partners — carry real risk: wasted time, data exposure, and reputational harm from engaging bad actors.
