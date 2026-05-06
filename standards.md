# Standards & API Reference

> Project: Employee Engagement Platform · Generated: 2026-05-06

## Industry Standards & Specifications

### ISO Standards

**ISO 23326:2022 — Human Resource Management: Employee Engagement Guidelines**
- URL: https://www.iso.org/standard/75238.html
- Provides guidelines for organizations to establish, implement, maintain, and improve employee engagement. Defines engagement in terms of cognitive, emotional, and behavioural components — directly relevant to the survey methodology and scoring frameworks used in an engagement platform.

**ISO/TS 30438:2024 — Human Resource Management: Employee Engagement Metrics**
- URL: https://www.iso.org/standard/68715.html
- Technical specification defining quantitative and qualitative metrics for measuring employee engagement. Sets a standardised vocabulary and measurement approach, useful for benchmarking and cross-organisation comparisons.

**ISO 30414:2025 — Human Capital Reporting and Disclosure**
- URL: https://www.iso.org/standard/30414
- Requires organisations to measure and disclose workforce engagement metrics as part of human capital reporting. The 2025 revision expands coverage to include AI and data governance, aligns with ESG frameworks (GRI, SASB), and introduces requirements for ethical workforce analytics.

**ISO 45003:2021 — Psychological Health and Safety at Work**
- URL: https://www.iso.org/standard/64283.html
- Guidelines for managing psychosocial risks in the workplace, covering factors such as poor communication, excessive pressure, and organisational culture. Engagement platforms that include wellbeing dashboards or manager effectiveness scoring should align with this standard's risk categories and recommended interventions.

**ISO 10667 — Assessment Service Delivery in Work and Organisational Settings**
- Applies to psychometric validity and reliability of engagement surveys. Relevant when designing scientifically grounded pulse survey instruments with defensible scoring.

**ISO/IEC 27001 — Information Security Management Systems**
- URL: https://www.iso.org/standard/27001
- The baseline security standard for platforms storing personal employee sentiment data. Enterprise HR buyers routinely require ISO 27001 certification or equivalent as a procurement prerequisite.

### W3C & IETF Standards

**WCAG 2.2 — Web Content Accessibility Guidelines**
- URL: https://www.w3.org/TR/WCAG22/
- Published October 2023 (updated December 2024); approved as ISO/IEC 40500:2025. Level AA compliance is now mandatory under the European Accessibility Act (EAA, in force June 2025) and the U.S. DOJ Title II rule (April 2024). Survey forms, dashboards, and recognition feeds must meet Level AA to serve employees with disabilities.

**RFC 6749 — The OAuth 2.0 Authorization Framework**
- URL: https://datatracker.ietf.org/doc/html/rfc6749
- Defines the authorisation framework used by all major engagement and HRIS APIs (Culture Amp, Rippling, Workday, Qualtrics). An engagement platform must implement OAuth 2.0 client credentials flow for machine-to-machine HRIS sync and authorisation code flow for user-facing SSO.

**RFC 6750 — The OAuth 2.0 Bearer Token Usage**
- URL: https://www.ietf.org/rfc/rfc6750.txt
- Specifies how bearer tokens are transmitted in HTTP requests. Required reading when consuming or exposing OAuth-protected APIs.

**OpenID Connect Core 1.0**
- URL: https://openid.net/specs/openid-connect-core-1_0.html
- Authentication layer on top of OAuth 2.0; enables single sign-on with enterprise identity providers (Okta, Azure AD, Google Workspace). Nearly all enterprise engagement platforms require OIDC-based SSO as a table-stakes capability.

**RFC 7643 & RFC 7644 — SCIM 2.0 (System for Cross-domain Identity Management)**
- URL: https://datatracker.ietf.org/doc/html/rfc7643 | https://datatracker.ietf.org/doc/html/rfc7644
- Defines the standard schema and REST protocol for automated user provisioning and de-provisioning. SCIM 2.0 is the predominant standard for syncing employee rosters from HRIS (Workday, BambooHR, Rippling) to downstream engagement platforms. Leapsome, Bonusly, and others already expose SCIM endpoints.

**RFC 7231 — HTTP/1.1 Semantics and Content**
- URL: https://datatracker.ietf.org/doc/html/rfc7231
- Foundational HTTP semantics underpinning all REST API interactions. Referenced here as the normative basis for consistent HTTP status codes and method semantics across an engagement platform's API.

### Data Model & API Specifications

**OpenAPI Specification 3.1.1**
- URL: https://spec.openapis.org/oas/v3.1.1.html
- The standard interface description language for REST APIs. Version 3.1 achieves full alignment with JSON Schema 2020-12 and adds native webhook definitions. All publicly documented engagement platform APIs (Leapsome, Qualtrics, SurveyMonkey) publish OpenAPI specs. An AI-native engagement platform should ship an OpenAPI 3.1 spec from day one.

**JSON Schema 2020-12**
- URL: https://json-schema.org/specification
- Used for validating API request/response bodies. Full support is built into OpenAPI 3.1; relevant for defining survey response payloads, engagement score schemas, and webhook event envelopes.

**iCalendar / RFC 5545**
- URL: https://datatracker.ietf.org/doc/html/rfc5545
- Standard format for calendar event data; relevant when scheduling recurring pulse surveys or syncing survey cadences with employees' calendar systems (Google Calendar, Outlook).

### Security & Compliance Standards

**GDPR — General Data Protection Regulation**
- URL: https://gdpr-info.eu/
- EU regulation governing personal data processing, including employee survey responses. Key obligations: lawful basis for processing (contract or legal obligation, not consent in employment contexts), data minimisation, right of access, right to erasure, 72-hour breach notification, and Data Protection Impact Assessments (DPIAs) for automated profiling. Fines up to €20M or 4% of global turnover.

**CCPA / CPRA — California Consumer Privacy Act / California Privacy Rights Act**
- URL: https://oag.ca.gov/privacy/ccpa
- California equivalent of GDPR. Applies to employee data for organisations with California employees above certain thresholds. Requires disclosure of data categories collected, opt-out rights, and data deletion on request.

**SOC 2 Type II**
- URL: https://www.aicpa-cima.com/resources/article/soc-2-type-2-report
- The de-facto US security audit standard expected by enterprise HR buyers. Covers the Trust Services Criteria: Security, Availability, Confidentiality, Processing Integrity, and Privacy. Engagement platforms handling employee sentiment data are routinely evaluated against SOC 2 Type II reports.

**NIST Cybersecurity Framework 2.0**
- URL: https://www.nist.gov/cyberframework
- Published February 2024. Governs, identifies, protects, detects, responds, and recovers — a governance framework increasingly referenced alongside SOC 2 by enterprise IT security teams evaluating SaaS HR tools.

**OWASP Top 10 (2021)**
- URL: https://owasp.org/www-project-top-ten/
- Canonical list of the most critical web application security risks. Survey platforms processing sensitive employee responses are common targets for injection, broken access control, and insecure design vulnerabilities.

---

## Similar Products — Developer Documentation & APIs

### Culture Amp

- **Description:** Leading employee engagement and performance platform used by 6,500+ organisations. Provides survey, analytics, and manager enablement capabilities.
- **API Documentation:** https://docs.api.cultureamp.com/docs/resources-getting-started
- **API Reference:** https://docs.api.cultureamp.com
- **Support Guide:** https://support.cultureamp.com/en/articles/8675204-culture-amp-api
- **SDKs/Libraries:** No official SDKs listed; REST/JSON via any HTTP client
- **Standards:** REST, OAuth 2.0 Client Credentials Flow
- **Authentication:** OAuth 2.0 (Client Credentials)
- **Notes:** Currently read-only (outbound data retrieval). No data ingestion via API. Access tokens are scoped per API consumer.

### Qualtrics EmployeeXM

- **Description:** Enterprise experience management platform with rigorous academic survey methodology, text analytics, and advanced reporting.
- **API Documentation:** https://www.qualtrics.com/support/integrations/api-integration/overview/
- **Developer Portal:** https://developer.qualtrics.com/developer/portal/
- **API Reference:** https://api.surveymonkey.com/v3/docs (v3 REST API)
- **Code Examples:** Python and Java snippets provided in official docs
- **Standards:** REST/JSON, OpenAPI
- **Authentication:** API Token (X-API-TOKEN header)
- **Notes:** Separate EU data centre endpoint available. Postman collection provided.

### Microsoft Viva Glint (via Microsoft Graph)

- **Description:** Employee engagement survey platform integrated into the Microsoft 365 ecosystem. Acquired from LinkedIn Glint, now part of Microsoft Viva.
- **API Documentation:** https://learn.microsoft.com/en-us/graph/social-intel-concept-overview
- **Microsoft Graph Overview:** https://learn.microsoft.com/en-us/viva/microsoft-viva-overview
- **Developer Centre:** https://developer.microsoft.com/en-us/viva
- **SDKs/Libraries:** Microsoft Graph SDKs (JavaScript, Python, Java, Go, .NET, PHP)
- **Standards:** REST/JSON, OData, OpenAPI, Microsoft identity platform (OIDC/OAuth 2.0)
- **Authentication:** OAuth 2.0 / Microsoft Entra ID (formerly Azure AD)
- **Notes:** Viva Glint does not expose a standalone public API; data access is mediated through Microsoft Graph. Viva Insights analytics API is available for productivity and wellbeing signal data.

### Lattice

- **Description:** All-in-one performance and engagement platform covering reviews, OKRs, pulse surveys, and manager tools.
- **API Documentation:** https://lattice.com/api | https://help.lattice.com/hc/en-us/articles/360059449534-Lattice-s-Public-API
- **Developer Docs:** https://api.latticehq.com/v1/
- **Standards:** REST/JSON
- **Authentication:** API Key (requires prior approval from Lattice via request-api-access@lattice.com)
- **Notes:** API key is generated once and shown only at creation time. Approval-gated access model.

### Leapsome

- **Description:** Performance, learning, and engagement platform with AI manager assistant features. Published OpenAPI 3.0 specification.
- **API Documentation (Swagger):** https://api.leapsome.com/v1/api-docs/
- **SCIM API Docs:** https://api.leapsome.com/scim/v1/api-docs/
- **Help Articles:** https://help.leapsome.com/hc/en-us/articles/27607742571933
- **Standards:** REST/JSON, OpenAPI 3.0 (OAS3), SCIM 2.0
- **Authentication:** API Token; SCIM uses a separate provisioning token
- **Notes:** SCIM 2.0 endpoint available for automated user provisioning from identity providers and HRIS systems.

### BambooHR

- **Description:** HR information system (HRIS) for small and mid-size businesses; core employee data store that engagement platforms commonly integrate with for roster sync.
- **API Documentation:** https://documentation.bamboohr.com/docs
- **API Reference:** https://documentation.bamboohr.com/reference
- **SDKs/Libraries:** Official Python SDK (BambooHRClient); PHP SDK; works with any HTTP client
- **Developer Guide:** https://documentation.bamboohr.com/docs/getting-started
- **Standards:** REST/JSON
- **Authentication:** API Key via HTTP Basic Auth (key as username, any string as password)
- **Notes:** New paginated GET /api/v1/employees endpoint added with filtering and sorting. A common upstream data source for employee roster provisioning into engagement tools.

### Rippling

- **Description:** Workforce management platform combining HR, IT, and Finance. One of the most comprehensive HRIS/payroll APIs available.
- **API Documentation:** https://developer.rippling.com/documentation/rest-api/reference/rippling-platform-api
- **Developer Portal:** https://developer.rippling.com
- **Blog (API Architecture):** https://www.rippling.com/blog/enterprise-grade-apis
- **Standards:** REST/JSON, OAuth 2.0
- **Authentication:** OAuth 2.0 (authorisation code flow); API tokens also supported
- **Notes:** Well-documented REST API with standard pagination and metadata conventions. A primary HRIS integration target for employee roster synchronisation.

### Workday (HCM & Peakon)

- **Description:** Enterprise HCM platform; Peakon (acquired 2021) provides the continuous listening and engagement module natively integrated into Workday.
- **API Documentation:** https://community.workday.com/sites/default/files/file-hosting/productionapi/index.html
- **REST API Guide:** https://www.reco.ai/hub/workday-rest-api-integration-security
- **Standards:** REST/JSON (modern); SOAP/WSDL (legacy WWS endpoints)
- **Authentication:** OAuth 2.0 (API client registration in Workday tenant)
- **Notes:** Workday requires tenant-specific setup. SOAP WWS remains the most complete API surface; REST is expanding. Access typically requires a Workday partner or customer account.

### SurveyMonkey

- **Description:** General-purpose survey platform widely used for employee pulse surveys, especially by teams without a dedicated engagement tool.
- **API Documentation:** https://api.surveymonkey.com/v3/docs
- **Developer Portal (US):** https://developer.surveymonkey.com/
- **Developer Portal (EU):** https://developer.eu.surveymonkey.com/
- **Standards:** REST/JSON, OpenAPI, webhooks
- **Authentication:** OAuth 2.0
- **Notes:** Draft apps have a 90-day development window before requiring public or private deployment. Postman collection available. Code samples in Python and cURL.

### 15Five

- **Description:** AI-powered performance and engagement platform with pulse surveys (1–5 scale), check-ins, and HR outcomes dashboards.
- **API Documentation:** https://my.15five.com/api/public/ (API key required)
- **Standards:** REST/JSON
- **Authentication:** API Key (header-based)
- **Notes:** API supports check-in details, 1-on-1 events, and recognition ("high fives") data. Lighter API surface than enterprise platforms; primarily targeted at integration partners.

---

## Notes

### Emerging Standards

- **ISO 30414:2025** alignment with ESG/sustainability reporting (GRI, SASB, IFRS S2) is becoming a procurement requirement for listed companies and public-sector organisations. An AI-native engagement platform that auto-generates ISO 30414-compliant human capital disclosures would address a significant gap.
- **SCIM 2.0** is the de-facto provisioning standard for HRIS-to-SaaS employee sync. Platforms without a SCIM endpoint face manual CSV upload workflows — a major source of data quality issues and administrative friction.
- **EU AI Act (effective 2025–2026)** classifies AI systems used for recruitment, performance evaluation, and promotion as "high-risk." An engagement platform that uses AI to score managers or predict attrition must implement conformity assessments, transparency obligations, and human oversight mechanisms under the Act. This is an under-addressed area in current vendor documentation.
- **AsyncAPI 3.0** is emerging as the OpenAPI equivalent for event-driven and webhook APIs. Engagement platforms with rich real-time event streams (survey submitted, recognition given, alert triggered) should consider publishing an AsyncAPI specification alongside their OpenAPI REST spec.

### API Integration Gaps Observed

- Most engagement platforms (Culture Amp, Lattice, 15Five) are currently read-only or have limited write capabilities via API. Creating surveys, dispatching them, and ingesting responses programmatically remains poorly supported — a meaningful developer experience gap an open-source tool could close.
- No major platform publishes an AsyncAPI or webhook schema specification; webhook payload shapes are documented in prose rather than machine-readable form.
- Bonusly's API is functional but sparsely documented; recognition data extraction relies heavily on third-party integration platforms (Zapier, Make) rather than direct API access.
