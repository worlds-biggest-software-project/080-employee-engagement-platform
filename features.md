# Employee Engagement Platform — Feature & Functionality Survey

> Candidate #80 · Researched: 2026-05-02

## Solutions Analysed

| Tool | Type | Licence / Model | URL |
|------|------|-----------------|-----|
| Culture Amp | Commercial SaaS | Proprietary; $5–$9/person/mo | https://www.cultureamp.com |
| Microsoft Viva (Glint + Insights) | Commercial SaaS | Proprietary; ~$12/user/mo (M365 add-on) | https://www.microsoft.com/microsoft-viva |
| Workday Peakon Employee Voice | Commercial SaaS | Proprietary; bundled with Workday HCM | https://www.workday.com/peakon |
| Qualtrics EmployeeXM | Commercial SaaS | Proprietary; custom enterprise | https://www.qualtrics.com/employee-experience |
| Lattice | Commercial SaaS | Proprietary; $11/seat/mo (bundle) | https://www.lattice.com |
| 15Five | Commercial SaaS | Proprietary; $4/user/mo (Engage) | https://www.15five.com |
| Leapsome | Commercial SaaS | Proprietary; ~$8/user/mo est. | https://www.leapsome.com |
| Workleap (Officevibe) | Commercial SaaS | Proprietary; $3.50/user/mo | https://www.workleap.com |
| Happily.ai | Commercial SaaS | Proprietary; ~$3/user/mo | https://www.happily.ai |
| Quantum Workplace | Commercial SaaS | Proprietary; ~$5–$10/user/mo est. | https://www.quantumworkplace.com |

## Feature Analysis by Solution

### Culture Amp

**Core features**
- Annual, lifecycle, and pulse engagement surveys with 40+ validated, science-backed question templates grounded in academic engagement research (UWES, Gallup Q12, and proprietary constructs)
- Benchmark database from 6,500+ organisations enabling organisations to compare their engagement and driver scores against industry, region, and company-size peers
- Text analytics applied to open-text survey responses to identify themes and sentiment trends automatically without manual analyst review
- Action planning tools that convert engagement results into team-level priority lists for managers
- Manager dashboards showing direct report engagement scores with comparison to company and benchmark averages

**Differentiating features**
- Deepest survey science of any engagement platform — methodology developed with academic partners and validated against organisational outcomes
- AI Coach that translates engagement data into prioritised, manager-ready action recommendations rather than leaving interpretation to non-specialist managers
- Intersectionality analysis showing how engagement varies across combined demographic dimensions (e.g., by gender and ethnicity together, not separately)
- Heatmap visualisations making patterns across teams, locations, and tenure bands immediately visible without data analyst involvement
- Integration with performance review data to contextualise engagement alongside ratings and goal completion

**UX patterns**
- Survey admin experience allows configuring question selection, anonymity thresholds, and notification cadence without engineering support
- Manager action planner converts survey output into a specific, prioritised to-do list with suggested initiatives
- Employee-facing survey interface designed for completion in under three minutes on mobile

**Integration points**
- HRIS sync via SFTP and REST API with all major providers (Workday, BambooHR, ADP, Rippling, SAP SuccessFactors)
- Slack and Microsoft Teams for survey distribution and notification
- Performance data sync with Lattice and Workday for combined people analytics

**Known gaps**
- Expensive at scale; per-person pricing compounds for large organisations (1,000 employees at $7/person/month = $84,000/year for engagement alone)
- Real-time signalling limited; survey-based approach captures point-in-time sentiment rather than continuous behavioural signals
- No native behavioural data from productivity or collaboration tools; less predictive than Microsoft Viva's M365-behavioural approach
- OKR and performance module less mature than Lattice

**Licence / IP notes**
- Proprietary SaaS; no open-source components
- Survey methodology is well-documented publicly; AI Coach recommendation logic is not fully transparent
- Employee demographic data collected for DEI analysis requires explicit GDPR consent and data minimisation controls

---

### Microsoft Viva (Glint + Insights)

**Core features**
- Glint (acquired from LinkedIn): continuous listening platform with pulse surveys, lifecycle surveys, and manager-level engagement reporting
- Viva Insights: behavioural analytics drawn from Microsoft 365 usage data (meeting hours, collaboration patterns, after-hours work, network connectivity) providing a continuous signal stream independent of survey responses
- Viva Amplify: employee communication platform for cascading leadership messages and measuring readership
- Viva Goals: OKR management tool integrated into the M365 productivity suite
- Viva Learning: LMS-lite connecting Microsoft Teams to external learning content providers

**Differentiating features**
- Unique behavioural data layer from M365 usage — the only engagement platform that can correlate survey sentiment with actual work patterns (e.g., whether high-engagement scores correspond to healthy meeting loads)
- Embedded in Microsoft Teams; employees encounter engagement features in the same interface they use for daily work rather than a separate tool
- Deployed at 60%+ of Fortune 500 organisations, making it the de facto enterprise standard
- Manager privacy protection: individual M365 behavioural data is only shown at aggregate team level to managers; individuals cannot be singled out

**UX patterns**
- Glint survey experience delivered in-browser or via Microsoft Teams notification
- Viva Insights personal dashboard showing individuals their own productivity patterns with wellbeing recommendations
- Manager briefings: weekly AI-generated summary of team collaboration health and suggested focus areas

**Integration points**
- Native Microsoft 365 and Azure AD integration; no additional SSO configuration required
- Workday and SAP SuccessFactors for HRIS data sync
- External learning providers (LinkedIn Learning, Coursera) via Viva Learning

**Known gaps**
- Complex licensing — Viva modules are sold as a bundle and as individual add-ons; actual cost and module scope confusing to buyers
- Glint-Viva integration still maturing as of 2026; some organisations report data inconsistencies between Glint survey data and Viva Insights visualisations
- Survey methodology less rigorously documented than Culture Amp's academic approach
- Requires M365 E3/E5 for full Viva value; organisations without M365 cannot access the behavioural data layer
- Works council restrictions in Germany and France around M365 behavioural monitoring require legal review before deployment

**Licence / IP notes**
- Proprietary; part of Microsoft M365 ecosystem
- GDPR compliance documentation available; EU Standard Contractual Clauses in place
- M365 behavioural analytics may trigger works council consultation obligations in Germany (Betriebsrat), France (CSE), and the Netherlands under GDPR and national labour law

---

### Workday Peakon Employee Voice

**Core features**
- Continuous listening platform issuing adaptive micro-surveys to employees on a rolling cadence, rather than single annual events
- Real-time driver analysis that identifies the specific factors most strongly correlated with engagement scores in the organisation at any given time
- Predicted attrition modelling: Peakon's AI identifies individuals at high resignation risk based on engagement trajectory and driver pattern changes
- Manager feedback: anonymous upward feedback collected automatically and surfaced to managers with coaching recommendations
- Native Workday integration enabling engagement data to be viewed alongside HRIS, performance, and compensation data in one platform

**Differentiating features**
- Continuous adaptive survey cadence — instead of a fixed annual survey, each employee receives questions on a rolling schedule, generating a continuously updated organisational health score
- Predicted attrition AI that flags at-risk individuals before they resign — not after; reportedly achieves 85%+ prediction accuracy within a 90-day window
- Direct Workday data integration means no manual roster sync and engagement scores can be sliced by Workday job attributes (department, location, pay grade, manager)

**UX patterns**
- Employee survey delivered via email and Workday mobile app
- Manager engagement dashboard surfacing team health scores, driver analysis, and attrition risk indicators
- Confidentiality controls with minimum group sizes to prevent identification of individual respondents

**Integration points**
- Native Workday HCM integration (deepest of any engagement platform)
- Microsoft Teams and Slack for survey delivery notifications

**Known gaps**
- Full value only available to Workday HCM customers; standalone purchase less compelling
- Workday's acquisition (2021, $700M) has slowed independent innovation; product roadmap now tied to Workday release cycles
- Higher effective cost when bundled with Workday HCM licensing
- Less benchmark comparison data than Culture Amp's 6,500+ organisation database

**Licence / IP notes**
- Proprietary; part of Workday HCM suite
- Predicted attrition AI is a closed model; no external audit methodology published
- EU AI Act high-risk classification may apply to attrition prediction AI used in HR decisions

---

### Qualtrics EmployeeXM

**Core features**
- Enterprise-grade survey platform with advanced question logic, branching, and experimental design capabilities
- Text iQ: AI-powered text analytics classifying open-text responses into themes and sentiment categories at scale
- Stats iQ: statistical modelling tools allowing power users to run regression analysis and significance testing on survey data
- Benchmark data from Qualtrics' XM Benchmark Database for industry comparisons
- 360-degree feedback and development survey modules alongside engagement

**Differentiating features**
- Highest methodological rigour of any commercial engagement platform; built on academic survey research principles
- Unique ability to run conjoint analysis, experimental designs, and structural equation modelling within the platform — capabilities far beyond standard HR use cases
- Cross-functional experience data management connecting employee experience data to customer experience (CX) data for unified experience management
- Pre-built programme templates validated against industry-standard constructs (Gallup Q12, UWES)

**UX patterns**
- Power-user analytics interface with configurable dashboards, filter drill-downs, and export to BI tools
- Executive-level summary dashboards with KPI-style engagement health cards

**Integration points**
- REST API for integration with any HRIS or data warehouse
- Workday, SAP SuccessFactors, and ServiceNow connectors
- Tableau and Power BI for analytics export

**Known gaps**
- Overpowered for most HR teams; statistical capabilities require data analysts to extract full value
- Complex and expensive; overkill for companies under 1,000 employees
- Manager-facing UX less intuitive than Culture Amp or 15Five for non-analyst users

**Licence / IP notes**
- Proprietary; KKR/Silver Lake-backed after SAP spin-out (2023, $12.5B valuation)
- No open-source components

---

### Workleap (Officevibe)

**Core features**
- Weekly automated pulse surveys with 10 core engagement dimensions measuring key engagement drivers on a rolling basis
- Recognition and peer praise module integrated into the weekly survey flow
- Manager reports highlighting team-specific engagement scores with suggested actions
- Anonymous direct messaging allowing employees to share concerns with managers confidentially
- Good Vibes: peer-to-peer recognition integrated into daily workflow

**Differentiating features**
- Fastest time-to-value of any engagement platform; most teams deploy in under a day without configuration
- Affordable pricing ($3.50/user/month) making engagement measurement accessible to SMBs and teams within larger organisations
- Free tier for up to 10 users enables risk-free trial by small teams

**UX patterns**
- Minimal survey experience — weekly check-in takes under two minutes
- Team-level reports designed for managers with no analytics training
- Simple red/amber/green team health indicators requiring no interpretation

**Integration points**
- Slack and Microsoft Teams for survey delivery
- BambooHR and basic HRIS CSV sync

**Known gaps**
- Analytics limited compared with Culture Amp or Qualtrics
- No DEI intersectionality analysis or advanced text analytics
- No compensation or performance data integration
- Not suitable for enterprise compliance reporting or works council requirements

**Licence / IP notes**
- Proprietary SaaS; part of Workleap portfolio (formerly GSoft)
- No open-source components

---

### Happily.ai

**Core features**
- Daily micro-check-in collecting a single sentiment signal per employee to generate continuous team health trends
- DEBI score: proprietary 0–100 composite engagement index combining daily check-in, recognition, and interaction signals
- Peer recognition with social feed of public praise visible to the whole team
- AI manager coaching recommendations based on team DEBI score trends and patterns

**Differentiating features**
- Highest survey cadence in the market — daily single-question check-in generates a continuous real-time health signal rather than point-in-time snapshots
- Designed for small, high-growth teams where relationship quality is the primary engagement driver
- Very affordable ($3/user/month) entry point

**UX patterns**
- Mobile-first daily check-in delivered via app notification
- Team health trend line visible to all team members (not just managers) fostering collective ownership

**Integration points**
- Slack for daily check-in delivery
- Basic HRIS CSV import

**Known gaps**
- No enterprise compliance, benchmark, or DEI analytics capabilities
- DEBI score methodology not independently validated against academic engagement constructs
- Not suitable for organisations with works council compliance requirements
- Limited enterprise integration library

**Licence / IP notes**
- Proprietary SaaS; no open-source components

---

## Cross-Cutting Feature Themes

### Table-Stakes Features
- Annual or semi-annual engagement survey with validated, science-backed question library
- Pulse survey capability (weekly or monthly micro-surveys) with configurable question sets
- Open-text collection with automated theme and sentiment analysis
- Manager-level dashboards with team engagement scores, driver analysis, and suggested actions
- Demographic filtering with minimum group size anonymity controls to protect individual privacy
- HRIS roster sync for automated employee lifecycle management
- Peer recognition and appreciation features integrated into the daily workflow
- SOC 2 Type II certification for enterprise security requirements

### Differentiating Features
- Continuous adaptive survey cadence (Peakon model) replacing fixed annual events
- Predictive attrition risk scoring fusing engagement trajectory with behavioural and performance data
- Behavioural analytics from productivity tool usage (M365/Google Workspace) as an independent signal layer
- Intersectionality demographic analysis beyond single-dimension breakdowns
- AI-generated manager action plans derived from survey driver analysis
- Benchmark database enabling comparison against industry, region, and company-size peers
- Cross-functional integration of employee and customer experience data (Qualtrics model)

### Underserved Areas / Opportunities
- No open-source employee engagement platform of any substance exists in 2026
- Frontline and deskless worker engagement — all leading platforms are designed for knowledge workers with corporate email and M365 access; 2.7 billion deskless workers remain largely unserved
- Explainable attrition prediction with auditable model weights — current predictive tools are black boxes
- Works council-compliant deployment templates for Germany, France, and the Netherlands where employee monitoring requires formal consultation
- Multilingual survey delivery for non-English-speaking workforces without translation quality degradation
- SMB-accessible benchmark data from broad industry panels at sub-$5/user/month pricing

### AI-Augmentation Candidates
- Predictive attrition modelling fusing engagement signals, calendar behaviour, performance trajectory, and external job market activity
- Automated qualitative synthesis: clustering open-text themes and generating manager-ready action plans from thousands of verbatim comments
- Personalised survey cadence optimisation to prevent response fatigue while maximising data quality
- Manager coaching recommendations tailored to specific team dynamics, not generic engagement advice
- Recognition nudge delivery timed to project milestones and individual contribution events identified from calendar and project data

---

## Legal & IP Summary

- No open-source employee engagement platform of any substance exists; the entire market is proprietary SaaS
- Employee survey data is personal data under GDPR and CCPA; requires lawful basis (typically legitimate interest or consent), data minimisation, and right-to-erasure capabilities
- Works council consultation is legally mandatory in Germany (Betriebsrat), France (CSE), Austria, and the Netherlands before deploying any system that monitors employee behaviour — including engagement survey platforms and any tool using M365 behavioural data (Viva Insights)
- ISO 30414:2018 requires listed companies in many jurisdictions to report workforce engagement metrics as part of human capital disclosures
- Predictive attrition AI may be classified as high-risk under the EU AI Act if used to inform HR decisions about individuals; requires transparency documentation and human oversight mechanisms
- Gallup Q12 survey items are trademarked; platforms using them require a Gallup licence or partnership
- UWES (Utrecht Work Engagement Scale) items are licensed under Creative Commons; freely usable with attribution
- No patent-encumbered techniques identified in standard pulse survey workflows; predictive ML models may be subject to broad algorithmic patents (currently unenforced in HR context)
- SOC 2 Type II is a practical prerequisite for enterprise sales

---

## Recommended Feature Scope

**Must-have (MVP)**
- Annual and pulse engagement surveys with validated question library (UWES-based constructs; avoid Gallup Q12 without licence)
- Open-text collection with automated sentiment theme analysis
- Manager engagement dashboard with team scores, driver analysis, and suggested actions
- Demographic filtering with minimum group size anonymity thresholds
- Peer recognition module with social feed and manager visibility
- HRIS roster sync and SAML 2.0 SSO
- SOC 2 Type II certification path

**Should-have (v1.1)**
- Continuous adaptive survey cadence with AI-determined per-employee question scheduling
- Predictive attrition risk scoring with interpretable risk factors (not a black box score)
- AI-generated manager action plans derived from survey driver analysis
- Benchmark comparison against industry and region peer data
- Works council-compliant deployment configuration (minimum group sizes, data residency, co-determination audit trail)
- Mobile-first survey delivery with multilingual content support

**Nice-to-have (backlog)**
- Behavioural signal integration from collaboration tools (calendar, messaging) as a non-survey engagement signal
- Intersectionality demographic analysis across combined dimensions
- Manager effectiveness scoring derived from 360 feedback patterns and team engagement trends
- Integration with external job market signals for attrition risk enrichment
- Deskless worker engagement module with SMS and QR-code survey delivery
