# Employee Engagement Platform

> Part of the [worlds-biggest-software-project](https://github.com/worlds-biggest-software-project) initiative.
>
> An open-source, AI-native engagement platform delivering pulse surveys, recognition, and manager effectiveness scoring with auditable models and data sovereignty.

The Employee Engagement Platform is a continuous listening, recognition, and manager-coaching system for organisations that want rigorous engagement measurement without locking themselves into proprietary SaaS. It is built for Chief People Officers, HR business partners, and HRIS administrators who need defensible engagement metrics, predictive attrition signals, and works council-compliant deployment options that no incumbent currently provides on open-source terms.

---

## Why Employee Engagement Platform?

- **No open-source platform of any substance exists in this market.** The entire engagement category — Culture Amp, Microsoft Viva, Peakon, Qualtrics, Lattice, 15Five, Leapsome — is proprietary SaaS, leaving no credible self-hostable option for organisations that need data sovereignty.
- **Incumbent pricing compounds painfully at scale.** Culture Amp at $5–$9/person/month means a 1,000-employee organisation pays roughly $84,000/year for engagement alone; Lattice bundles run $11/seat/month and Microsoft Viva Suite is ~$12/user/month.
- **Predictive attrition models are black boxes.** Peakon's attrition AI and Viva's behavioural signals are closed; under the EU AI Act, HR-decision AI faces high-risk classification and demands transparency that proprietary vendors do not deliver.
- **Works council compliance is poorly served.** Germany (Betriebsrat), France (CSE), Austria, and the Netherlands legally require formal consultation before behavioural monitoring; cloud-only SaaS with opaque data flows complicates this, while a self-hostable OSS platform with auditable models addresses it directly.
- **2.7 billion deskless workers are unserved.** Every leading platform assumes corporate email and M365 or Slack access; frontline retail, healthcare, manufacturing, and logistics workforces are an untapped market for a mobile-first, multilingual, SMS-capable platform.

---

## Key Features

### Continuous Listening & Surveys

- Annual and pulse engagement surveys with a validated, science-backed question library based on UWES constructs (Creative Commons-licensed) to avoid Gallup Q12 trademark constraints
- Continuous adaptive survey cadence with AI-determined per-employee question scheduling to prevent response fatigue while maintaining data quality
- Open-text collection with automated theme clustering and sentiment analysis of verbatim comments
- Demographic filtering with minimum group size anonymity thresholds to protect individual respondent identity
- Mobile-first survey delivery with multilingual content support for non-English-speaking workforces

### Manager Enablement & Action Planning

- Manager engagement dashboards with team scores, driver analysis, and suggested actions accessible without analytics training
- AI-generated manager action plans derived from survey driver analysis, converting results into prioritised to-do lists
- Manager effectiveness scoring derived continuously from 360 feedback patterns and team engagement trends
- Anonymous upward feedback collection with coaching recommendations surfaced to managers
- Recognition and peer praise module integrated into the daily workflow with manager visibility

### Predictive Analytics & Attrition Risk

- Predictive attrition risk scoring with interpretable risk factors rather than an opaque score
- Driver analysis identifying the specific factors most strongly correlated with engagement at any given time
- Benchmark comparison against industry, region, and company-size peer data
- Intersectionality demographic analysis across combined dimensions (e.g. gender and ethnicity together)

### Compliance & Enterprise Readiness

- Works council-compliant deployment configuration including minimum group sizes, data residency, and co-determination audit trail
- HRIS roster sync via SFTP, REST, and SCIM with all major providers
- SAML 2.0 SSO and SOC 2 Type II certification path
- GDPR and CCPA controls covering lawful basis, data minimisation, and right-to-erasure
- ISO 30414:2018-aligned human capital reporting outputs

---

## AI-Native Advantage

AI is used to fuse engagement signals, calendar behaviour, performance trajectory, and external job market activity into individual-level attrition probability, enabling intervention before resignations rather than after. NLP models cluster open-text themes, detect sentiment drift, and generate manager-ready action plans from thousands of verbatim comments — work that incumbents currently sell as expensive professional services. Survey cadence is personalised per employee based on response fatigue signals, and recognition nudges are timed to project completions and contribution events surfaced from calendar and project data. Crucially, every model is auditable: weights, features, and recommendation logic are inspectable to satisfy EU AI Act high-risk obligations and build trust with works councils.

---

## Tech Stack & Deployment

The platform targets self-hosted, cloud, and hybrid deployment so organisations can keep employee sentiment data on private infrastructure where required by GDPR, works council agreements, or internal policy. Integration is via REST APIs, SFTP, and SCIM for HRIS roster sync (Workday, BambooHR, ADP, Rippling, SAP SuccessFactors), with Slack and Microsoft Teams for survey delivery. Survey content is built on UWES (Creative Commons) constructs; ISO 10667 and ISO 30414:2018 inform assessment delivery and human capital reporting outputs.

---

## Market Context

The global employee engagement software market is valued at ~$1.27B in 2026 and is projected to reach $2.58B by 2031 at a 15.28% CAGR (Mordor Intelligence); the broader employee experience management market sits at $7–$9B when adjacencies are included. Incumbent pricing ranges from $3.50/user/month at the SMB end (Workleap) to ~$12/user/month for Microsoft Viva Suite, with Culture Amp at $5–$9 and Lattice at $11. Primary buyers are Chief People Officers at 500–10,000-employee companies, VPs of HR at mid-market firms, HR business partners, and HRIS administrators.

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
