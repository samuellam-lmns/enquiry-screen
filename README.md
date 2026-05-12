# enquiry-screen

Screens inbound investment enquiries for legitimacy and Lumonus fit before any team member invests time engaging.

## What it does

Takes a raw inbound enquiry (name, company, email, phone, message) and runs a **7-layer research protocol** that cross-checks every significant claim against at least two independent sources. Outputs a structured verdict with all sources cited.

## When to use it

Any time Lumonus receives a cold outreach from a claimed investor — VC, private equity, family office, angel, or anyone else offering capital. Especially useful for:

- Website contact form submissions from unknown parties
- Cold LinkedIn messages or emails claiming investment interest
- Referrals from intermediaries you haven't verified yet

## The 7 layers

| Layer | What it checks |
|---|---|
| 1. Individual identity | Are the named people findable, consistent, real? |
| 2. Contact channels | Do the email/phone match a legitimate firm? |
| 3. Entity verification | Is the company properly registered? |
| 4. Registered address | Physical presence or mail-drop? |
| 5. Track record | Any disclosed deals or portfolio history? |
| 6. Fraud/regulatory check | BaFin, FCA, SEC, ASIC, scam databases |
| 7. Lumonus fit | Right sector, stage, instrument, geography? |

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

Existing due diligence tools (Keye, CENTRL, ToltIQ, Vantager) all solve buyside DD — screening deals you want to invest in. None address the reverse: a startup screening inbound investor outreach for legitimacy before committing team time to a call.
