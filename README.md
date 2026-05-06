# Startup Cap Table Manager

> Part of the [worlds-biggest-software-project](https://github.com/worlds-biggest-software-project) initiative.
>
> An AI-native, open-source equity management platform covering cap tables, option grants, 409A valuations, and investor updates.

Startup Cap Table Manager is a candidate project for a self-hostable cap table and equity administration system aimed at founders, CFOs, and finance teams from pre-seed through late stage. It targets the gap left by expensive incumbents and the trust deficit created by Carta's 2024 secondary-data controversy, combining transparent OSS tooling with AI-powered valuation and scenario modelling.

---

## Why Startup Cap Table Manager?

- **Carta pricing scales aggressively**: third-party benchmarks place Carta at $40K–$77K+/yr for Series B+ companies and up to $11,988/month, pricing that pushes mid-stage companies to look for alternatives.
- **Trust deficit at the incumbent**: in January 2024 Carta was accused of using client confidential secondary transaction data to solicit trades through its own marketplace, creating an opening for a transparent, OSS-licensed alternative with documented data-use policies.
- **409A is the largest recurring cost for early-stage companies**: traditional firms charge $1,200–$8,000+ per valuation, while AI-assisted platforms now deliver compliant valuations from $499 — a wedge for an OSS platform with a built-in AI valuation engine.
- **The only existing OSS option (Captable.io) is immature**: it lacks 409A integration, ASC 718 calculation, hosted SaaS, and AI features, leaving room for a well-funded OSS project to take the category.
- **Mid-stage companies ($5M–$50M raised) are underserved**: Carta is expensive and controversial, while Pulley and Eqvista are lightweight on multi-class waterfalls, ASC 718, and complex scenario modelling.

---

## Key Features

### Cap Table & Equity Administration

- Manage common stock, preferred stock, SAFEs, convertible notes, warrants, and ISO/NSO stock options plus RSUs.
- Vesting schedule management with cliff, graded, and custom patterns and automated vest-date calculations.
- Share issuance, transfer, cancellation, and repurchase workflows with board-approval gating.
- Option exercise workflow with ISO/NSO tax type selection and documentation generation.
- Board consent and approval workflows for equity actions with e-signature execution.

### Fundraising, Modelling & Reporting

- Fundraising round modelling with pro-forma dilution preview and investor allocation tables.
- Waterfall analysis showing exit proceeds distribution by security class at multiple valuation scenarios.
- ASC 718 stock-based compensation expense calculation for GAAP financial reporting.
- Investor portal with limited-access shareholder views, holdings, documents, and vesting status.
- Employee equity portal with grant acceptance, vesting visualisation, and exercise estimator.

### Valuation & Compliance

- Integrated 409A valuation, either via an embedded engine or third-party API.
- Post-409A audit trail documenting FMV methodology for IRS examination readiness.
- Compliance monitoring against IRS Section 409A, SEC Rule 701, IRC §422 (ISO/NSO), and ASC 718.
- Optional support for UK EMI, French BSPCE, and other EU jurisdiction-specific instruments.

### Migration & Interoperability

- Carta migration importer with high-fidelity cap table reconstruction targeting customers leaving the incumbent.
- REST API and SSO from launch for programmatic access and enterprise identity.
- Accounting integrations (QuickBooks, Xero) for ASC 718 / IFRS 2 journal entries.
- HRIS integrations (Gusto, Rippling, BambooHR, Personio) for employee record sync.
- E-signature integrations (DocuSign, Dropbox Sign) for grant execution.

---

## AI-Native Advantage

Conversational scenario modelling lets founders ask questions like "what happens to my ownership if we raise $8M at $40M pre-money with a 10% option pool top-up?" in plain English, removing the primary friction point in cap-table software. An AI-powered 409A engine selects comparables, runs DCF modelling, and produces defensible methodology documentation at a fraction of traditional valuation cost. Proactive compliance monitoring surfaces alerts when Rule 701 thresholds are approaching, options are nearing expiration, or 83(b) election windows are open, and AI-drafted investor updates compress a multi-hour monthly task to minutes.

---

## Tech Stack & Deployment

The project is positioned as MIT-compatible open source with a self-hostable core and an optional hosted SaaS tier offering AI-assisted 409A and scenario modelling. Captable.io (MIT) is identified as a possible reference base. Expected interfaces include a REST API, SSO, HRIS and accounting integrations, and e-signature providers. Compliance scope covers IRS Section 409A, ASC 718, SEC Rule 701, IRC §422 (ISO/NSO), UK EMI, and GDPR / CCPA for shareholder PII.

---

## Market Context

The cap table management software market is estimated at roughly USD $6.3B in 2026 and projected to reach USD $15B by 2033 at ~12% CAGR (Data Insights Market), with the broader equity management software market on a similar trajectory through 2034 (Zion Market Research). Incumbent pricing ranges from free tiers up to $40K–$77K+/yr at Carta Scale and ~$50K+/yr at Diligent Equity. Primary buyers are first-time and seed-stage founders, Series A–B CFOs, and late-stage / pre-IPO finance teams, with budgets ranging from under $1K/yr to $100K+/yr.

---

## Project Status

> This project is in the **research and specification phase**.  
> Contributions, feedback, and domain expertise are welcome.

---

## Contributing

We welcome contributions from developers, domain experts, and potential users.
See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

**Important:** All contributions must be your own original work or clearly attributed
open-source material with a compatible licence. Copyright infringement and licence
violations will not be tolerated and will result in immediate removal of the offending
contribution. If you are unsure whether a piece of code, text, or other material is
safe to contribute, open an issue and ask before submitting.

---

## Licence

Licence to be determined. See [discussion](#) for context.
