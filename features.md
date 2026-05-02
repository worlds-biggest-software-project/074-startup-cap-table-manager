# Startup Cap Table Manager — Feature & Functionality Survey

> Candidate #74 · Researched: 2026-05-02

## Solutions Analysed

| Tool | Type | Licence / Model | URL |
|------|------|-----------------|-----|
| Carta | Commercial SaaS | Proprietary / tiered subscription | https://carta.com |
| Pulley | Commercial SaaS | Proprietary / subscription | https://pulley.com |
| Eqvista | Commercial SaaS | Proprietary / freemium + per-stakeholder | https://eqvista.com |
| Ledgy | Commercial SaaS | Proprietary / freemium + subscription | https://ledgy.com |
| Cake Equity | Commercial SaaS | Proprietary / freemium + subscription | https://cakeequity.com |
| Gust Equity Management | Commercial SaaS (freemium) | Proprietary / free + paid add-ons | https://gust.com/equity-management |
| Diligent Equity (Shareworks) | Commercial SaaS | Proprietary / enterprise | https://www.diligent.com |
| AngelList | Commercial SaaS | Proprietary / fee-on-funds | https://angel.co |
| Captable.io | Open Source | MIT licence | https://github.com/captable-inc/captable |
| LTSE Equity | Commercial SaaS | Proprietary / freemium | https://equity.ltse.com |

## Feature Analysis by Solution

### Carta

**Core features**
- Cap table management: all security types including common stock, preferred stock, SAFEs, convertible notes, warrants, and options
- Equity plan administration: ISO and NSO stock option grants with vesting schedule management, exercise workflow, and tax reporting
- RSU and restricted stock management with vesting and settlement workflows
- 409A independent valuation service with audit-ready reports
- Fundraising modelling: pro-forma cap table for new rounds with dilution preview
- Board approval workflow for equity grants and corporate actions
- Investor portal with ownership summary and document access
- ASC 718 stock compensation expense calculation for financial reporting
- Fund administration for VC funds alongside portfolio company cap tables
- Secondary transaction management and liquidity programmes

**Differentiating features**
- Network effects: 50,000+ companies and 2.5 million shareholders on the platform; investors and law firms use Carta as a default, reducing friction on every transaction
- Broadest feature set in the market: the only platform covering cap table, equity plan administration, 409A, fund administration, and secondary markets in a single product
- Carta Data: largest private company equity data set; used for 409A benchmarking, valuation comparables, and compensation benchmarking

**UX patterns**
- Dashboard showing total equity, outstanding options, and recent activity
- Grant workflow: draft → board approval → employee notification → acceptance → vesting schedule activation
- Scenario modeller with waterfall analysis showing proceeds to each security class at various exit valuations
- Investor portal: limited-access view for shareholders showing their position, documents, and vesting status

**Integration points**
- API integrations with Gusto, Rippling, and major HRIS for employee data sync
- QuickBooks and Xero integration for ASC 718 journal entries
- Docusign and Dropbox Sign integration for electronic execution of grants and exercise agreements
- Law firm integrations with major Silicon Valley law firms for cap table setup and maintenance

**Known gaps**
- Controversy in January 2024: Carta was accused of using client confidential secondary transaction data to solicit trades through its own Carta Liquidity marketplace without company consent; CEO investigated and Carta subsequently exited the secondary trading business — significant trust damage with the founder community
- Expensive at scale: pricing reaches $40K–$77K+/yr for Series B+ companies and $2,988–$11,988/month at the high end per third-party benchmarks
- Network lock-in: migrating off Carta requires converting complex data structures; customers report migration being deliberately difficult
- EU/UK equity compliance (EMI, growth shares) less deep than Ledgy for European companies

**Licence / IP notes**
- Fully proprietary (Carta Inc.; ~$7.4B valuation at last known round, 2021)
- 2024 data controversy raised questions about whether client equity data is used for Carta's own commercial purposes; scrutiny ongoing

---

### Pulley

**Core features**
- Cap table management for all common security types: common, preferred, SAFEs, convertible notes, options, warrants
- 409A independent valuation included in Growth and higher plans (3–5 day turnaround vs. Carta's 10)
- Fundraising modelling with round simulation and dilution analysis
- Option grant management with exercise workflow and tax planning tools
- Offer letter generation with equity component embedded
- Board consent and approval workflows for equity actions
- Investor portal for shareholder transparency

**Differentiating features**
- Faster 409A: 3–5 business day delivery vs. Carta's typical 10 days; bundled in Growth plan pricing
- Transparent, founder-friendly pricing: Growth plan at ~$3,500/yr includes 409A, option grants, and all features — positioned explicitly as the lower-cost Carta alternative
- Stripe backing (Series B led by Stripe, 2022) brings credibility and potential fintech integration depth
- Clean migration tools from Carta: specific tooling to ingest Carta data exports and reconstruct cap table fidelity

**UX patterns**
- Clean, minimal SaaS interface with cap table summary as the primary view
- Fundraising modelling wizard with step-by-step round parameter configuration
- Employee equity portal with vesting schedule visualisation and exercise estimator

**Integration points**
- HRIS integrations with Gusto, Rippling, and BambooHR for employee record sync
- Docusign for electronic grant execution
- QuickBooks and accounting platform integrations for ASC 718

**Known gaps**
- Fund administration features absent; not suitable for VC funds managing portfolio alongside fund
- Fewer integrations than Carta's mature ecosystem
- Less suitable for very late-stage or public company equity administration

**Licence / IP notes**
- Fully proprietary (Pulley Inc.; $43M Series B, 2022; independent as of 2026)

---

### Eqvista

**Core features**
- Cap table management for all security types including common, preferred, SAFEs, options, and RSUs
- 409A valuations starting from $990 (pre-seed/seed) with 1–2 day turnaround
- Unlimited 409A valuations included in paid annual plans at competitive pricing
- Share issuance, transfer, and cancellation workflows
- Vesting schedule management with cliff, graded, and custom vesting patterns
- Option exercise workflow with tax reporting
- Investor reporting with cap table snapshot and round history

**Differentiating features**
- Lowest-cost 409A delivery of any integrated platform: from $990/yr for unlimited valuations vs. $1,500–$8,000+ at Carta or traditional valuation firms
- Per-stakeholder pricing model (vs. flat annual fee) makes it cost-effective for companies with many shareholders but simpler cap tables
- Ranked independently as best value-for-money cap table tool; highest ease-of-use scores among standalone cap table platforms
- Strong for pre-seed and seed stage: free basic tier enables founders to start tracking equity before any institutional round

**UX patterns**
- Spreadsheet-style cap table view familiar to founders who previously managed equity in Excel
- Share issuance wizard with certificate generation
- 409A upload and reporting workflow embedded in the cap table interface

**Integration points**
- QuickBooks and accounting integrations for ASC 718
- E-signature integrations for grant execution
- API available for custom integrations

**Known gaps**
- Less suitable for Series B+ complexity: multi-class liquidation preferences, complex waterfall calculations, and sophisticated scenario modelling are weaker than Carta or Pulley
- Smaller legal and investor ecosystem compared to Carta's network effects
- Fund administration absent

**Licence / IP notes**
- Fully proprietary (Eqvista Inc.)

---

### Ledgy

**Core features**
- Cap table management for all security types including UK EMI options, growth shares, and European warrant structures
- Employee equity portal with vesting visualisation and grant acceptance workflow
- Fundraising modelling with round simulation and investor-facing reporting
- 409A valuations (for US companies) and HMRC valuations (for UK EMI)
- ASC 718 and IFRS 2 stock compensation expense calculation
- Board approval workflows for equity actions
- Investor portal with transparency reporting

**Differentiating features**
- Leading European equity management platform: deepest coverage of UK EMI, French BSPCE, German employee equity, and other EU/UK jurisdiction-specific instruments
- Employee equity UX is the most refined in the market: employees see a real-time valuation of their equity, vesting progress, and "what if" exit value calculator
- Free tier for early-stage European companies with generous feature limits

**UX patterns**
- Employee-focused equity portal is the primary differentiator: designed for employee understanding and engagement, not just legal compliance
- Modern, visually polished interface with data visualisations of cap table composition and dilution history
- Board and investor reporting with one-click sharing

**Integration points**
- Integrations with Personio, HiBob, Workday, and BambooHR for employee record sync
- DocuSign and HelloSign for grant execution
- Accounting integrations for IFRS 2 and ASC 718

**Known gaps**
- US market presence smaller than Carta or Pulley; fewer US law firm and investor integrations
- Fund administration absent
- 409A delivery speed and pricing less competitive than Eqvista for US-focused companies

**Licence / IP notes**
- Fully proprietary (Ledgy AG; $23M Series B, 2022; European-incorporated)

---

### Captable.io

**Core features**
- Cap table management for common and preferred shares with vesting schedule tracking
- SAFE and convertible note modelling
- Option pool management with grant issuance workflow
- Waterfall analysis for exit proceeds distribution
- Stakeholder management with investor and employee portals

**Differentiating features**
- Only functional open-source cap table platform available as of 2026 (MIT licence)
- Self-hostable with full data ownership; no vendor lock-in
- Community-developed alternative to Carta with transparent, auditable codebase

**UX patterns**
- Web application interface with cap table summary view
- Basic grant and share issuance workflows
- Stakeholder portal for investor and employee access

**Integration points**
- REST API for programmatic access and integration
- Self-hosted deployment on standard cloud infrastructure

**Known gaps**
- Early-stage project: lacks 409A valuation integration, ASC 718 calculation, multi-jurisdiction equity compliance, and the depth of commercial platforms
- No hosted SaaS tier; requires self-hosting and DevOps capability
- No AI features
- Smaller community than commercial tools; active development but limited roadmap visibility

**Licence / IP notes**
- MIT licence: maximally permissive; commercial use, modification, and distribution permitted without restriction
- No copyleft obligations; ideal base for a commercial open-source product with a hosted SaaS tier

---

### AngelList

**Core features**
- Cap table management for venture-stage companies
- SPV (Special Purpose Vehicle) creation and administration for syndicate investments
- Rolling fund management with recurring LP subscription
- Venture portfolio management for fund managers
- Cap table round modelling and SAFE management

**Differentiating features**
- Native integration with the VC deal flow ecosystem; investors and syndicates already live on AngelList
- SPV and rolling fund administration makes it the dominant platform for emerging fund managers
- Free cap table for portfolio companies as a mechanism to acquire companies into the AngelList ecosystem

**UX patterns**
- Fund and SPV management as primary interface (investor-first, not founder-first)
- Portfolio view for fund managers showing all investee companies, ownership stakes, and fund performance

**Integration points**
- AngelList Funds integration for direct link between fund records and portfolio company cap tables
- Legal document generation for SPV subscription agreements

**Known gaps**
- Cap table depth for company-side features is secondary to the fund management use case
- Less sophisticated for complex equity plan administration (RSUs, complex vesting, ASC 718) than Carta or Pulley
- Primarily US-focused; limited international equity instrument support

**Licence / IP notes**
- Fully proprietary (AngelList LLC)

---

## Cross-Cutting Feature Themes

### Table-Stakes Features
- Cap table tracking for all common security types: common stock, preferred stock, SAFEs, convertible notes, warrants, stock options (ISO and NSO), and RSUs
- Vesting schedule management: cliff vesting, graded vesting, and custom patterns with automated vest-date calculations
- Share issuance, transfer, cancellation, and repurchase workflows with board approval gating
- Option exercise workflow with tax type selection (ISO vs. NSO) and documentation generation
- 409A independent valuation service or integration: IRS-compliant fair market value determination for option grant exercise prices
- Fundraising round modelling with pro-forma dilution preview and investor allocation tables
- Waterfall analysis: exit proceeds distribution by security class at configurable valuation scenarios
- Investor portal: limited-access shareholder view showing holdings, documents, and vesting status
- Employee equity portal: grant acceptance, vesting schedule visualisation, and exercise estimator
- Board consent workflow for equity actions with e-signature execution
- ASC 718 stock compensation expense calculation for GAAP financial reporting

### Differentiating Features
- Scenario modelling at conversational speed: natural-language prompts answering "what happens to my ownership if we raise $8M at $40M pre-money with 10% option pool top-up?" — no existing platform delivers this without navigating complex UI
- AI-powered 409A valuation reducing cost from $2,000+ to under $500 via automated comparable selection and DCF modelling
- Intelligent compliance monitoring: proactive alerts when Rule 701 thresholds are approaching, when options are nearing expiration, when a secondary transfer may trigger tax consequences
- Migration tooling from Carta: explicit cap table import capability targeting the large base of Carta customers who may want to leave following the 2024 controversy
- Post-409A audit trail: full documentation of FMV determination methodology for IRS examination readiness
- Network integration: law firm and investor ecosystem integrations that reduce friction on new equity transactions

### Underserved Areas / Opportunities
- Trust deficit left by Carta data controversy (January 2024): a transparent OSS platform with a documented data non-use policy for the company's own commercial purposes would directly address this
- Open-source with self-hosted option: Captable.io exists but lacks maturity; a well-funded OSS project with hosted SaaS, AI-powered 409A, and scenario modelling would be a genuine alternative to Carta
- AI-assisted 409A: the $499–$999 AI-assisted valuation market is growing (vs. $1,500–$8,000 from traditional firms); an OSS platform with embedded AI valuation would eliminate the largest recurring cost for early-stage companies
- Mid-stage company gap ($5M–$50M raised): Carta is expensive and controversial; Pulley/Eqvista are lightweight; the mid-stage company with a complex but not Fortune 500-level cap table is underserved
- Investor update automation: founders spend 3+ hours per month manually compiling KPI reports for investors; an AI-native cap table that drafts investor updates would be a strong product differentiator

### AI-Augmentation Candidates
- Natural-language scenario modelling: answering complex dilution and ownership questions in plain English without platform navigation
- AI-powered 409A: automated FMV determination using ML-selected comparables, regression on private company transaction databases, and DCF modelling with defensible methodology documentation
- Compliance threshold monitoring: continuously monitoring cap table state against Rule 701, Rule 12g, and 83(b) election windows; proactively surfacing alerts
- Option expiration management: AI identifying options approaching expiration and surfacing exercise decisions before they lapse unexercised
- Investor update drafting: AI generating investor updates from cap table data, financial metrics, and milestone inputs; founder-reviewed before sending
- Secondary market readiness assessment: AI evaluating whether a secondary transaction would trigger tax or securities law issues before founder approval

---

## Legal & IP Summary

Cap table management involves securities regulation (SEC Rule 701, Rule 12g, IRC Section 409A, ASC 718) that is entirely public law with no IP constraints. The 409A valuation methodology is defined by IRS guidance (Rev. Proc. 2007-62, IRS Notice 2005-1) and is freely referenceable. ASC 718 stock compensation accounting is governed by FASB accounting standards, which are public. Standard waterfall calculation approaches (preference stack, participation rights, conversion modelling) are mathematical algorithms based on the economic terms defined in company charter documents — no patent risk. Captable.io is MIT-licensed, making it an ideal base for extension or reference without any copyleft obligations. Carta's data controversy creates a unique market opening for a trust-differentiated OSS platform; however, care should be taken to document and publish clear data usage policies. No patent-encumbered techniques were identified in any area of cap table management, equity plan administration, or 409A valuation methodology.

---

## Recommended Feature Scope

**Must-have (MVP)**:
- Cap table management for common stock, preferred stock, SAFEs, convertible notes, stock options (ISO/NSO), and RSUs
- Vesting schedule management with cliff, graded, and custom patterns; automated vest-date calculations and notifications
- Share issuance, transfer, cancellation, and board-approval workflow with e-signature execution
- Option exercise workflow with ISO/NSO tax type selection and documentation generation
- Fundraising round modelling with pro-forma dilution preview and investor allocation table
- Waterfall analysis showing exit proceeds distribution at multiple valuation scenarios
- Investor and employee portals with appropriate access tiers
- 409A valuation integration (own engine or third-party API)
- REST API and SSO from launch

**Should-have (v1.1)**:
- AI-powered natural-language scenario modelling answering dilution and ownership questions in plain English
- Proactive compliance monitoring: Rule 701 threshold alerts, option expiration warnings, 83(b) election windows
- ASC 718 stock compensation expense calculation for GAAP financial reporting
- Carta migration importer with high-fidelity data reconstruction
- AI-assisted investor update drafting from cap table and financial data

**Nice-to-have (backlog)**:
- AI-powered 409A valuation engine with automated comparable selection and DCF modelling
- UK EMI and EU jurisdiction-specific equity instrument support (BSPCE, growth shares)
- Fund and SPV administration for early-stage fund managers alongside portfolio company cap tables
- Secondary transaction marketplace or matching (with explicit data use consent and separation from cap table data)
- Integrated board management with equity action approvals embedded in a board portal
