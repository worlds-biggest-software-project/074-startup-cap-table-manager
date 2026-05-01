# Startup Cap Table Manager

> Candidate #74 · Researched: 2026-05-01

## Existing Products and Software Packages

| Tool | Description | Type | Pricing | Strengths / Weaknesses |
|------|-------------|------|---------|------------------------|
| **Carta** | Industry-standard cap table, equity plan administration, 409A valuations, fund administration, and investor relations | Commercial | Launch: $280/yr (≤25 stakeholders); Build: $2,800/yr; Growth/Scale: $6K–$77K+/yr | Strength: dominant network effects (50K+ companies, 2.5M shareholders), broadest feature set. Weakness: expensive at scale, controversy over using client data for secondary marketplace |
| **Pulley** | Founder-friendly cap table with 409A valuations, SAFEs, fundraising modeling, and option grants | Commercial | Startup: ~$1,200/yr; Growth: ~$3,500/yr (includes 409A); Enterprise: custom | Strength: faster 409A (3–5 days vs Carta's 10), transparent bundled pricing. Weakness: smaller ecosystem, fewer fund admin features |
| **Eqvista** | Cap table management with 409A, equity plan admin, and investor reporting; ranked #1 for value/ease of use | Commercial | Free tier (basic); Paid from ~$500/yr; 409A from $990 | Strength: low cost, fast 409A, good for pre-seed/seed. Weakness: less mature for Series B+ complexity |
| **Ledgy** | European-focused equity management for startups through public company, including employee portal | Commercial | Free for early-stage; Growth: ~€3,600/yr; Enterprise: custom | Strength: strong EU/UK compliance, employee equity UX. Weakness: smaller US market presence |
| **Cake Equity** | APAC-focused cap table platform with a global employee equity portal and secondary market features | Commercial | Free starter; Paid plans from ~$1,500/yr | Strength: strong ESOP workflow, APAC compliance. Weakness: limited 409A support (US-centric need) |
| **Gust Equity Management (GEM)** | Free cap table with basic round modeling and 409A for very early-stage companies | Commercial (freemium) | Free tier; paid 409A add-on | Strength: zero cost for early founders. Weakness: limited scalability, no advanced modeling |
| **Diligent Equity (fka Solium/Shareworks)** | Enterprise equity administration for late-stage and public companies, acquired by Morgan Stanley | Commercial | Custom enterprise pricing (~$50K+/yr) | Strength: brokerage integration, global compliance. Weakness: overbuilt for startups, expensive |
| **AngelList** | Venture ecosystem platform with cap table, SPV management, and rolling funds | Commercial | Free cap table; fees on fund management (1–2%) | Strength: integrated with VC deal flow. Weakness: less comprehensive for complex equity plans |
| **Captable.io (open source)** | Open-source cap table platform on GitHub; alternative to Carta/Pulley | Open Source | Free (self-hosted) | Strength: full transparency, no vendor lock-in. Weakness: early-stage project, limited 409A integration, no hosted SaaS tier |
| **LTSE Equity** | Equity management platform tied to Long-Term Stock Exchange ecosystem | Commercial | Free for early stage; paid at scale | Strength: alignment with governance-focused founders. Weakness: niche positioning, limited ecosystem |

## Relevant Industry Standards or Protocols

- **IRS Section 409A** — US tax code governing fair market value of private company stock; non-compliance exposes option holders to immediate taxation + 20% penalty. Requires independent annual valuation.
- **ASC 718 (FASB)** — US GAAP standard for stock-based compensation expense; drives equity plan accounting requirements for audit-ready companies.
- **SAFE (Simple Agreement for Future Equity)** — YCombinator standard instrument; now dominant for pre-seed/seed financing; platforms must model MFN provisions and pro-rata rights.
- **Rule 701 (SEC)** — Exemption for employee equity compensation; triggers disclosure requirements above $10M in issuances in a 12-month period.
- **ISO/NSO stock option rules (IRC §422)** — Governs incentive stock options vs non-qualified stock options; affects tax treatment for employees and companies.
- **UK EMI (Enterprise Management Incentives)** — UK equivalent to ISOs; requires HMRC notification and valuation; relevant for UK-based platforms.
- **GDPR / CCPA** — Privacy regulations affecting storage of shareholder PII across jurisdictions.

## Available Research Materials

1. Data Insights Market (2025). *Cap Table Management Software Market Demand and Consumption Trends: Outlook 2025–2033*. https://www.datainsightsmarket.com/reports/cap-table-management-software-1387384 — Industry market research; preprint-style.

2. Zion Market Research (2024). *Equity Management Software Market Size, Share, Trends & Forecast 2034*. https://www.zionmarketresearch.com/report/equity-management-software-market — Quantitative market sizing report.

3. 409A Valuation Insights (2026). *409A Valuation Cost in 2026: Current Pricing Benchmarks*. https://409a-valuation.com/insights/409a-valuation-cost-2026 — Practitioner pricing benchmark report.

4. Carta (2026). *Best Cap Table Software for 2026: Buying Guide*. Carta Blog. https://carta.com/best-cap-table-software/ — Vendor-authored buyer guide; useful for market framing (note bias).

5. BizBot (2026). *Carta vs. Pulley: Cap Table Software Comparison*. https://www.bizbot.com/blog/carta-vs-pulley-cap-table-software-comparison/ — Independent comparative review.

6. Eqvista (2026). *Top Carta Alternatives for Startups in 2026*. https://eqvista.com/carta-alternative-eqvista-for-cap-table-management/ — Competitor analysis; useful for feature gap identification.

7. Qapita (2026). *Top 6 Cap Table Management Software Tools for Startups 2026*. https://www.qapita.com/blog/top-cap-table-management-software-for-startups-2026 — Asia-Pacific perspective on global platforms.

8. CostBench (2026). *Carta Pricing 2026: 4 Plans from $2,988–$11,988/month*. https://costbench.com/software/equity-management/carta/ — Verified pricing benchmarks from procurement database.

## Market Research

**Market Size & Growth**
- Cap table management software market: ~USD $6.3B (2026), projected USD $15B by 2033 at ~12% CAGR (Data Insights Market)
- Equity management software market: projected $12%+ CAGR through 2034 (Zion Market Research)
- Global VC investment in 2025 exceeded $350B, directly driving demand for cap table platforms at the seed/Series A stage

**Pricing Table**

| Vendor | Free Tier | Seed/Early | Series A–B | Late Stage/Enterprise |
|--------|-----------|------------|------------|----------------------|
| Carta | Yes (raised <$1M) | $280–$2,800/yr | $6,000–$20,000/yr | $40K–$77K+/yr |
| Pulley | No | ~$1,200/yr | ~$3,500/yr | Custom |
| Eqvista | Yes | ~$500–$990/yr | ~$2,500/yr | Custom |
| Ledgy | Yes | €3,600/yr | Custom | Custom |
| Captable.io | Yes (OSS) | Free (self-hosted) | Free (self-hosted) | N/A |

**409A Valuation Pricing (2026)**

| Stage | Traditional Firms | AI-Assisted Platforms | Carta | Pulley (bundled) |
|-------|------------------|----------------------|-------|-----------------|
| Pre-seed / Seed | $1,200–$2,000 | $499–$999 | ~$1,500 | Included in Growth plan |
| Series A | $2,000–$4,000 | $1,200–$2,500 | ~$2,500 | Included |
| Series B+ | $4,000–$8,000+ | $2,500–$5,000 | $4,000–$8,000 | Custom |

**Buyer Personas**
- **First-time founder (pre-seed):** Needs free or very low-cost cap table with SAFE support and basic 409A; evaluates GEM, Eqvista free tier, Captable.io.
- **Seed-stage founder ($1M–$5M raised):** Needs SAFE/priced round modeling, option grant workflow, IRS 409A compliance; budget $1,200–$3,500/yr; evaluates Pulley, Eqvista, Carta Launch.
- **Series A–B CFO (10–100 employees):** Needs ASC 718 accounting, board approval workflows, investor portal; budget $6K–$20K/yr; evaluates Carta, Pulley Growth, Ledgy.
- **Late-stage / Pre-IPO CFO:** Needs full ESOP administration, global compliance (Rule 701, EMI), secondary liquidity programs; budget $40K–$100K+/yr; evaluates Carta Scale, Diligent Equity.

**Notable Acquisitions / Funding**
- Carta raised $500M+ total; last known valuation ~$7.4B (2021); faced significant controversy in 2024 over using client secondary transaction data for its own marketplace.
- Carta acquired Capdesk (UK equity management, 2022) to expand European presence.
- Morgan Stanley acquired Solium (later Shareworks, then Diligent Equity) for $900M in 2019.
- Pulley raised $43M Series B (2022, led by Stripe); remains independent in 2026.
- Ledgy raised $23M Series B (2022); focused on European expansion.

## AI-Native Opportunity

- **Automated 409A valuation with AI-driven defensibility:** The 409A market is being disrupted by AI-assisted platforms that deliver compliant valuations at $499 vs. $2,000+ from traditional firms. An OSS platform with a built-in AI valuation engine (trained on comparable transaction data and DCF models) could eliminate the biggest recurring cost for early-stage companies.
- **Scenario modeling and dilution simulation at chat speed:** Founders and CFOs currently model fundraising rounds in spreadsheets or spend hours in platform UIs. An AI assistant that answers "what happens to my ownership if we raise $8M at $40M pre-money with a 10% option pool top-up?" in natural language would remove the primary friction point in cap table software adoption.
- **Intelligent compliance monitoring:** Platforms do not proactively alert founders when they cross Rule 701 thresholds, when options are approaching expiration, or when a secondary transfer may trigger tax consequences. An AI layer monitoring the cap table state against regulatory thresholds and proactively surfacing alerts is a clear unmet need.
- **Investor update automation:** Founders manually compile KPI reports for investors. An AI-native cap table that ingests financial data and drafts investor updates (with waterfall analysis, dilution history, and narrative) would compress a 3-hour task to minutes.
- **OSS differentiation:** Captable.io exists as an early OSS project but lacks hosted SaaS, 409A integration, and AI features. A well-funded OSS alternative to Carta — with a permissive license, self-hosted option, and AI-powered 409A + scenario modeling as a premium SaaS tier — directly targets Carta's controversial data practices and high pricing as a wedge.
