# Standards & API Reference

> Project: Startup Cap Table Manager · Generated: 2026-05-06

## Industry Standards & Specifications

### US Tax & Securities Law Standards

**IRS Section 409A — Fair Market Value of Private Company Stock**
- Official Reference: Treasury Regulation § 1.409A-1(b)(5)(iv); IRS Notice 2005-1; Rev. Proc. 2007-62
- URL: https://www.law.cornell.edu/cfr/text/26/1.409A-1
- Section 409A governs the tax treatment of deferred compensation including stock options and SARs in private companies. Requires that option exercise prices equal or exceed the fair market value (FMV) of the underlying stock on the date of grant. Non-compliance exposes option holders to immediate income tax, a 20% excise tax penalty, and interest. A cap table platform must record the 409A FMV in effect at the time of each grant and link grants to supporting valuation reports.

**IRC Section 422 — Incentive Stock Options (ISOs)**
- Official Reference: 26 U.S.C. § 422; 26 CFR §§ 1.422-1 and 1.422-2
- URL: https://www.law.cornell.edu/uscode/text/26/422
- Governs the statutory requirements for options to qualify as incentive stock options (ISOs), including: grant pursuant to a shareholder-approved plan, exercise price ≥ FMV at grant, per-employee annual ISO limit of $100,000 (by FMV), 2-year post-grant and 1-year post-exercise holding periods for favourable tax treatment, and Form 3921 reporting upon exercise. Cap table software must track ISO vs. NSO classification, apply the $100,000 annual limitation, and trigger Form 3921 data generation on exercise events.

**SEC Rule 701 — Compensatory Benefit Plan Exemption**
- Official Reference: 17 CFR § 230.701; SEC updated guidance March 2026
- URL: https://www.sec.gov/rules/final/33-7645.htm
- Exempts employee equity compensation from Securities Act registration for private companies. Key thresholds: aggregate issuances in any 12-month period must not exceed 15% of total assets or $1 million; issuances exceeding $10 million in a 12-month period trigger enhanced disclosure requirements (risk factors, financial statements). Following M&A transactions, target company equity issued under Rule 701 in the same 12-month period must be aggregated. Cap table software must track Rule 701 rolling 12-month issuance totals and provide proactive alerts as thresholds approach.

**SEC Rule 12g — Registration Threshold for Private Companies**
- Official Reference: 15 U.S.C. § 78l(g); 17 CFR § 240.12g-1
- URL: https://www.sec.gov/info/edgar/siccodes.htm
- Requires companies with more than 2,000 shareholders of record (or 500 non-accredited investors) and assets exceeding $10 million to register their securities with the SEC. Cap table software should track total shareholder counts and surface alerts approaching these thresholds.

**SEC EDGAR — Electronic Filing System**
- Official API: https://www.sec.gov/search-filings/edgar-application-programming-interfaces
- Data API: https://data.sec.gov/
- API Overview PDF: https://www.sec.gov/files/edgar/filer-information/api-overview.pdf
- EDGAR provides RESTful JSON APIs for accessing public company filings including XBRL-tagged financial data. Rate limit: 10 requests/second per user. Relevant for late-stage companies approaching public reporting requirements and for benchmarking comparable company data in 409A valuation models.

### US GAAP Accounting Standards

**FASB ASC Topic 718 — Stock-Based Compensation**
- Official Reference: FASB Accounting Standards Codification Topic 718; ASU 2021-07 (Private Company Council simplification for FMV determination)
- URL: https://www.fasb.org/page/document?pdf=ASU_2021-07.pdf
- Requires all stock-based compensation (options, RSUs, restricted stock, SARs, performance awards) to be recognised in the income statement at fair value, measured at grant date for equity-classified awards, over the vesting period. Requires detailed disclosure of grant activity (granted, exercised, forfeited, expired) and weighted-average exercise prices. Cap table software must export ASC 718 compliance reports including grant tables, option fair values (Black-Scholes or binomial), weighted-average assumptions, and compensation expense by period.

**FASB ASC Topic 820 — Fair Value Measurement**
- Official Reference: FASB ASC 820
- URL: https://asc.fasb.org/820
- Provides the framework for measuring fair value used in 409A valuations and ASC 718 option pricing. Defines Level 1/2/3 inputs hierarchy. Relevant to the methodology documentation required in defensible 409A reports.

### Financial Reporting Standards

**XBRL / iXBRL — Extensible Business Reporting Language**
- Official Body: XBRL International; US GAAP Taxonomy maintained by FASB in collaboration with the SEC
- URL: https://xbrl.us/home/priorities/filers/sec-reporting/taxonomies/
- EDGAR XBRL Guide (April 2026): https://www.sec.gov/files/edgar/filer-information/specifications/xbrl-guide.pdf
- XBRL is the machine-readable format required by the SEC for financial statement filing. The US GAAP Taxonomy includes tags for stock-based compensation disclosures under ASC 718. Inline XBRL (iXBRL) is mandatory for all SEC filers. Relevant for cap table platforms targeting pre-IPO companies approaching public reporting.

**IFRS 2 — Share-Based Payment**
- Official Body: International Accounting Standards Board (IASB)
- URL: https://www.ifrs.org/issued-standards/list-of-standards/ifrs-2-share-based-payment/
- International equivalent of ASC 718 for companies reporting under IFRS (common in EU/UK and APAC companies). Requires recognition of share-based payment transactions in the income statement. Relevant for platforms serving European companies alongside US entities.

### Data Interchange Standards

**Open Cap Format (OCF) — Open Cap Table Coalition**
- Official Body: Open Cap Table Coalition (49+ member law firms and equity platforms)
- Repository: https://github.com/Open-Cap-Table-Coalition/Open-Cap-Format-OCF
- Documentation: https://open-cap-table-coalition.github.io/Open-Cap-Format-OCF/
- Schema Registry: https://schema.opencaptablecoalition.com/
- The industry-standard open data format for cap table data interchange. JSON Schema-based specification covering: manifest file, issuer data, stakeholder records, stock classes, stock plans, vesting schedules, valuations, and all transaction types (issuances, transfers, cancellations, exercises, conversions). Founding coalition members include Carta, Cooley, Fenwick, Goodwin Proctor, Gunderson Dettmer, LTSE Equity, Morgan Stanley, Orrick, and Wilson Sonsini. Pulley has implemented OCF import/export for law firm integrations. An OCF-compliant cap table platform gains automatic interoperability with the broader ecosystem of law firms and investors.

**Open Cap Table Excel Standard (OCX)**
- Official Body: Open Cap Table Coalition
- Announcement: https://medium.com/@opencaptable/announcing-the-open-cap-table-excel-standard-ocx-d70f5c6db4b0
- Complementary to OCF; standardises Excel-based cap table spreadsheet structure across law firms and software vendors for data ingestion and migration. Relevant for import functionality when onboarding companies from spreadsheet-managed cap tables.

**OpenAPI Specification (OAS) 3.1.1**
- Official Body: OpenAPI Initiative (Linux Foundation)
- Specification: https://spec.openapis.org/oas/v3.1.1.html
- Industry standard for documenting REST APIs. OAS 3.1 achieved full alignment with JSON Schema Draft 2020-12. A cap table platform should publish its API under an OAS 3.1-compliant specification to enable law firm integrators, HRIS vendors, and accounting platforms to auto-generate client SDKs.

**JSON Schema — Data Validation**
- Official Specification: https://json-schema.org/specification
- Draft 2020-12 is the current stable version. Used by OCF for its schema definitions. All cap table API request/response payloads and OCF-compatible export formats should validate against JSON Schema definitions.

### Privacy & Data Protection

**GDPR — General Data Protection Regulation (EU)**
- Official Reference: Regulation (EU) 2016/679
- URL: https://gdpr-info.eu/
- Governs processing of personal data of EU residents. Cap table software storing shareholder PII (name, address, national ID, tax identification numbers) for EU residents must comply with GDPR: lawful basis for processing (typically legitimate interest or contract performance), data subject rights (access, erasure, portability), data minimisation, and data processing agreements with sub-processors. Article 83 penalties: up to €20M or 4% of global annual turnover.

**CCPA / CPRA — California Consumer Privacy Act / California Privacy Rights Act**
- Official Reference: California Civil Code §§ 1798.100–1798.199.100; amended 2026
- URL: https://oag.ca.gov/privacy/ccpa
- Applies to businesses processing personal information of California residents meeting revenue or data volume thresholds. 2026 CPRA updates require formal privacy risk assessments before processing presenting significant risk, mandatory cybersecurity audits, and opt-out mechanisms for data sharing. Cap table software must provide data export and deletion capabilities for California shareholders.

### Authentication & Security Standards

**OAuth 2.0**
- Official Specification: RFC 6749 (IETF)
- URL: https://oauth.net/2/
- Industry-standard protocol for API authorisation delegation. Required for all third-party integrations (HRIS, accounting, e-signature) and for the issuer, investor, and employee portal API endpoints. OAuth 2.1 (advanced IETF standardisation as of 2026) consolidates best practices including mandatory PKCE for public clients.

**OpenID Connect (OIDC)**
- Official Specification: https://openid.net/developers/how-connect-works/
- Authentication layer built on OAuth 2.0. Required for SSO integration with identity providers (Okta, Auth0, Google Workspace, Microsoft Entra ID) for enterprise cap table platform customers.

**Financial-grade API (FAPI) Security Profile**
- Official Body: OpenID Foundation FAPI Working Group
- Specification: https://openid.net/specs/openid-financial-api-part-1-1_0.html
- Enhanced security profile for OAuth 2.0 and OIDC in financial services contexts. Requires sender-constrained tokens, PAR (Pushed Authorisation Requests), and stricter client authentication. Relevant for any cap table platform exposing APIs to financial institutions or fund administrators.

**DPoP — Demonstrating Proof of Possession (RFC 9449)**
- Official Specification: https://www.rfc-editor.org/rfc/rfc9449
- Binds access tokens to the client's private key, preventing token theft and replay attacks. Now considered best practice for public clients and financial-grade APIs. Should be implemented on all Issuer and Investor API endpoints.

### UK & European Equity Standards

**UK EMI — Enterprise Management Incentives**
- Official Reference: HMRC ITEPA 2003, ss 527–541
- URL: https://www.gov.uk/guidance/enterprise-management-incentives-overview
- UK tax-advantaged employee option scheme. Requires HMRC notification within 92 days of grant, independent valuation approved by HMRC Shares and Assets Valuation, and specific plan documentation. Cap table platforms serving UK companies must support EMI grant workflows, HMRC valuation linkage, and EMI notification reporting.

**French BSPCE — Bons de Souscription de Parts de Créateur d'Entreprise**
- Official Reference: Article 163 bis G of the Code général des impôts
- URL: https://www.impots.gouv.fr/
- French tax-advantaged founder and employee warrant scheme. Specific eligibility requirements (company age, shareholder structure) and reporting obligations to French tax authorities. Relevant for platforms targeting European startups.

---

## Similar Products — Developer Documentation & APIs

### Carta Developer Platform

- **Description:** Carta is the dominant US cap table and equity management platform (50,000+ companies, 2.5M shareholders). Its API platform targets HRIS providers, law firms, incorporation partners, personal wealth management tools, and investor portfolio platforms.
- **API Documentation:** https://docs.carta.com/api-platform/docs/introduction
- **API Landing Page:** https://carta.com/api/
- **Standards:** REST/JSON; OAuth 2.0 for authentication
- **Authentication:** OAuth 2.0 (partner integration); API keys for some endpoints
- **Key API Surfaces:**
  - **Issuer API** — full cap table data access for downstream platforms (HRIS, law firm portals, financial services)
  - **Launch API** — incorporation partner onboarding (e.g., Stripe Atlas integration for automatic cap table setup after company incorporation)
  - **Portfolio API** — individual shareholder holdings for wealth management, tax prep, option financing
  - **Investor API** — fund operator access to portfolio company cap table summaries

### Ledgy GraphQL API

- **Description:** Ledgy is the leading European equity management platform, with strong UK EMI, French BSPCE, and IFRS 2 coverage. Its API exposes transaction data, stakeholder records, and equity plan details via GraphQL.
- **API Documentation:** https://docs.ledgy.com/
- **API Tracker:** https://apitracker.io/a/ledgy
- **Standards:** GraphQL; OAuth 2.0
- **Authentication:** OAuth 2.0
- **Notes:** The GraphQL API is self-documenting via introspection. Supports querying grants, vesting schedules, stakeholder profiles, and equity transactions. EU GDPR compliance built in for shareholder data handling.

### AngelList Investor Management API

- **Description:** AngelList's Investor Management API targets fund operators for SPV and rolling fund administration. AngelList has announced it is no longer adding features to its original cap table product; portfolio companies are directed to migrate to other platforms.
- **API Documentation:** https://docs.angellist.com/docs/overview
- **Staging Endpoint:** https://portal-api-staging.angellist.com/beta
- **Production Endpoint:** https://portal-api.angellist.com/beta
- **Standards:** GraphQL (self-documenting via introspection)
- **Authentication:** Bearer API key (prefix sk_test for staging; sk_live for production)

### Captable.io (Open Source)

- **Description:** Open-source alternative to Carta (MIT licence). Supports cap table management, SAFE/convertible note modelling, option pool management, waterfall analysis, stakeholder portals, eSign documents, data rooms, and investor update workflows.
- **GitHub Repository:** https://github.com/captableinc/captable
- **API Tracker:** https://apitracker.io/a/captable-io
- **Standards:** REST API; self-hosted deployment on standard cloud infrastructure
- **Licence:** MIT — maximally permissive, ideal base for commercial open-source product
- **Notes:** No hosted SaaS tier as of 2026. Lacks 409A integration, ASC 718 calculation, and AI features. OCF-compatible import/export would be a valuable contribution.

### SEC EDGAR Data API

- **Description:** The SEC's public API for accessing EDGAR filings, company submissions, and XBRL-tagged financial data. Free, publicly available, no authentication required. Useful for 409A comparable company data retrieval (publicly reported compensation benchmarks) and for pre-IPO regulatory readiness tooling.
- **API Overview:** https://www.sec.gov/search-filings/edgar-application-programming-interfaces
- **Data Endpoint:** https://data.sec.gov/
- **Developer Resources:** https://www.sec.gov/about/developer-resources
- **Standards:** REST/JSON; XBRL
- **Authentication:** None (public API); rate limit 10 requests/second
- **Notes:** Submissions API updates with <1 second processing delay; XBRL APIs update within 1 minute of filing dissemination.

### DocuSign eSignature API

- **Description:** Industry-standard e-signature platform. Required for executing equity grant agreements, SAFE documents, exercise notices, board consents, and investor subscription agreements. All major cap table platforms integrate DocuSign or a comparable e-signature provider.
- **Developer Center:** https://developers.docusign.com/
- **REST API Reference:** https://developers.docusign.com/docs/esign-rest-api/reference/
- **SDKs:** C#, PHP, Java, Node.js, Python, Ruby — https://developers.docusign.com/docs/esign-rest-api/
- **Standards:** REST/JSON; OpenAPI; Webhook events
- **Authentication:** OAuth 2.0 (Authorization Code Grant or JWT Grant)
- **Notes:** Supports 153+ code examples. Free developer plan available. Dropbox Sign (formerly HelloSign) provides an alternative REST API at https://developers.hellosign.com/ with similar capability at lower cost for lower document volumes.

### Gusto Payroll & HR API

- **Description:** Gusto is a widely-used US payroll, benefits, and HRIS platform for startups. Cap table platforms integrate Gusto to sync employee records (for option grant eligibility), new hire/termination events (triggering vesting acceleration/cessation), and payroll withholding data for option exercises.
- **Developer Documentation:** https://docs.gusto.com/
- **Standards:** REST/JSON; OAuth 2.0
- **Authentication:** OAuth 2.0
- **Notes:** Gusto's API provides access to employee records, employment status, compensation data, and company info. Carta and Pulley both maintain native Gusto integrations.

### Merge Unified HR API

- **Description:** Merge provides a single unified API for integrating with 200+ HRIS, ATS, payroll, and CRM platforms simultaneously (Workday, BambooHR, Rippling, Gusto, ADP, Personio, HiBob, and others). AngelList Equity uses Merge to scale HRIS integrations. Building native HRIS integrations costs $10K–$50K per connector; Merge reduces this to a single integration.
- **Documentation:** https://docs.merge.dev/hris/overview
- **Case Study (AngelList Equity):** https://www.merge.dev/case-studies/angellist
- **Standards:** REST/JSON; Unified data model across HRIS vendors
- **Authentication:** OAuth 2.0; per-integration token management handled by Merge
- **Notes:** A cap table platform integrating Merge's Unified HRIS API acquires interoperability with 224+ HR platforms in a single implementation — the most efficient path to broad HRIS coverage.

### Stripe Atlas Incorporation API

- **Description:** Stripe Atlas incorporates Delaware C-corps and LLCs, issues founder equity, files 83(b) elections, and obtains EINs from the IRS. The Carta/Stripe Atlas integration automatically creates a new company's cap table on Carta immediately after incorporation. An OSS platform could replicate this integration to capture companies at the incorporation moment.
- **Atlas Documentation:** https://docs.stripe.com/atlas
- **Equity Terms Documentation:** https://docs.stripe.com/atlas/equity-terms
- **Carta/Atlas Integration Announcement:** https://carta.com/product-updates/carta-stripe-atlas-api-partnership/
- **Standards:** REST/JSON; Stripe API standard
- **Authentication:** Stripe API key; OAuth 2.0 for partner integrations
- **Notes:** Atlas incorporates 1 in 5 Delaware C-corps. Capturing this pipeline via an open-source cap table integration would be a significant distribution strategy.

### Open Cap Table Coalition OCF Tools

- **Description:** The OCF-Tools library provides xState-based validation tooling for OCF-format cap table files. Useful for verifying OCF import/export correctness during platform development.
- **Repository:** https://github.com/Open-Cap-Table-Coalition/OCF-Tools
- **Schema Repository:** https://github.com/Open-Cap-Table-Coalition/Open-Cap-Format-OCF
- **Standards:** JSON Schema; xState for validation workflow
- **Licence:** Open source (Open Cap Table Coalition)

---

## Notes

**OCF as the portability foundation:** The Open Cap Format (OCF) standard, backed by 49+ law firms and equity platforms including Carta, should be treated as the mandatory data interchange format for any new cap table platform. OCF compliance enables law firm integrations, migration from/to other platforms, and participation in the broader startup ecosystem without bespoke bilateral integrations.

**409A API gap:** There is no public, standardised API for delivering or retrieving IRS 409A valuations. Carta, Pulley, Eqvista, and Ledgy each deliver 409A as a proprietary internal service. An OSS platform building an AI-assisted 409A engine would be operating in a green-field API space with no incumbent standard to conform to — an opportunity to define the first open 409A valuation API specification.

**HRIS integration strategy:** The Merge Unified HRIS API (or equivalent unified middleware such as Finch or Unified.to) is the most efficient integration path for broad HRIS coverage. Building native bilateral integrations to Gusto, Rippling, and BambooHR individually would require $30K–$150K in engineering effort versus a single Merge integration.

**Emerging — OAuth 2.1 and DPoP:** OAuth 2.1 is in advanced IETF standardisation as of 2026. Cap table platforms serving financial institutions or fund administrators should implement DPoP (RFC 9449) token binding and PAR (Pushed Authorisation Requests) to align with Financial-grade API (FAPI) security profiles and future-proof their authentication architecture.

**XBRL relevance window:** XBRL/iXBRL is currently mandatory only for SEC-reporting (public) companies. However, pre-IPO companies increasingly need to produce XBRL-ready financial data for late-stage fundraising and dual-track IPO processes. A cap table platform could differentiate by generating draft XBRL-tagged equity disclosures for pre-IPO companies as an AI-assisted compliance feature.
