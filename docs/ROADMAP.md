# ROADMAP.md – codecraft  

---  

## Vision  
Empower non‑technical founders, indie hackers, and small teams to **design, build, and launch software products** without writing code.  Leveraging Axentx’s AI‑driven generation pipelines (vLLM, SGLang) and our curated datasets, codecraft will turn high‑level specifications into production‑ready code, UI, and deployment artifacts in minutes.

---  

## MVP (Must‑Have for Launch) – **🚀 Release 0.1**  

| Feature | Description | Owner | Acceptance Criteria |
|---------|-------------|-------|----------------------|
| **Spec‑to‑Code Engine** | Convert a structured product spec (JSON/YAML) into a full‑stack codebase (frontend + backend + DB). | AI/ML Lead | • 80 % of generated projects compile & run locally on first try.<br>• Supports Node.js (Express) + React + PostgreSQL stack.<br>• Uses vLLM for inference and SGLang for structured output. |
| **Web UI Builder** | Drag‑and‑drop UI canvas that emits the spec consumed by the engine. | Front‑end Lead | • Users can create pages, forms, and navigation flows.<br>• Exportable spec ≤ 5 KB.<br>• Real‑time preview updates. |
| **One‑Click Deploy** | Deploy generated code to a managed container (Docker) on a cloud provider (AWS Fargate / Railway). | DevOps Lead | • Deploy button creates a live URL within 5 min.<br>• Logs and health‑check visible in UI.<br>• Free tier limits: ≤ 2 containers, 1 GB RAM. |
| **Project Management Dashboard** | List, clone, and delete user projects; basic versioning. | Product Lead | • Auth via email/password (OAuth optional).<br>• Projects persisted in PostgreSQL.<br>• Export as zip. |
| **Safety & Guardrails** | Prompt sanitization, licensing checks, and basic security linting of generated code. | QA Lead | • No GPL‑licensed snippets in output.<br>• OWASP Top‑10 checks run; warnings shown. |
| **Documentation & Onboarding** | Quick‑start guide, tutorial videos, and sample templates. | Content Lead | • 5‑minute “Build a Todo app” tutorial completed by 90 % of beta users. |

**MVP Success Metrics**  
- 100 + beta users sign‑up within 30 days.  
- ≥ 70 % of generated projects run without manual fixes.  
- Average time from spec creation to live URL ≤ 10 minutes.  

---  

## Post‑MVP Roadmap  

### v1.0 – **Productization & Extensibility**  (Quarter 2 2026)

| Theme | Key Features | Target Release |
|-------|--------------|----------------|
| **Multi‑Stack Support** | • Add Python (FastAPI) + Vue.js stack.<br>• Support SQLite & MySQL alternatives.<br>• Stack selector in UI. | 2026‑07 |
| **Advanced Prompt Engineering** | • Template library (e‑commerce, SaaS, marketplace).<br>• Prompt versioning & A/B testing. | 2026‑08 |
| **Collaboration** | • Real‑time multi‑user editing of specs.<br>• Role‑based permissions (owner, contributor, viewer). | 2026‑09 |
| **CI/CD Integration** | • GitHub/GitLab import/export.<br>• Automated tests generation (unit + API). | 2026‑09 |
| **Analytics & Insights** | • Usage dashboards (generated lines of code, cost, performance).<br>• Heat‑maps of UI component reuse. | 2026‑10 |
| **Marketplace** | • Community‑shared templates & components.<br>• Monetization (paid templates). | 2026‑11 |

### v2.0 – **Enterprise & AI‑First Enhancements**  (Quarter 4 2026 – Q1 2027)

| Theme | Key Features | Target Release |
|-------|--------------|----------------|
| **Custom Model Fine‑Tuning** | • Allow customers to upload domain data → fine‑tune vLLM for higher fidelity.<br>• UI for managing fine‑tuned endpoints. | 2027‑01 |
| **Low‑Code Logic Builder** | • Visual flow editor for business rules (if/else, loops).<br>• Generates server‑side functions in selected language. | 2027‑02 |
| **Enterprise Deployments** | • Private VPC, on‑prem Docker/K8s options.<br>• SSO (SAML/OIDC) and audit logs. | 2027‑03 |
| **Performance Optimizer** | • Static analysis → suggest indexing, caching, async patterns.<br>• Auto‑scale configuration for deployed services. | 2027‑03 |
| **Compliance & Security Suite** | • SOC‑2, GDPR, HIPAA checklists.<br>• Automated dependency vulnerability scanning (dependabot). | 2027‑04 |
| **AI‑Assisted Refactoring** | • Post‑generation code improvement (readability, test coverage).<br>• One‑click “Refactor” button. | 2027‑04 |

---  

## Milestone Timeline (High‑Level)

| Date | Milestone |
|------|-----------|
| **2026‑05‑30** | MVP feature freeze (spec‑to‑code, UI builder, deploy). |
| **2026‑06‑15** | Internal QA & safety audit complete. |
| **2026‑06‑30** | Private beta launch (invite‑only). |
| **2026‑07‑31** | Public MVP release (codecraft 0.1). |
| **2026‑09‑30** | v1.0 Feature Complete (multi‑stack, collaboration). |
| **2026‑11‑15** | Marketplace beta open. |
| **2027‑01‑31** | Custom model fine‑tuning pilot. |
| **2027‑04‑30** | Enterprise‑ready v2.0 GA. |

---  

## Success Metrics & KPIs  

| Metric | Target (12 mo) |
|--------|----------------|
| **Paid conversions** | 5 % of active users upgrade to Pro (monthly). |
| **Retention** | 60‑day cohort retention ≥ 45 %. |
| **Generated code quality** | < 5 % of projects require manual bug fixes after launch. |
| **Time‑to‑value** | Avg. spec‑to‑live ≤ 8 min (post‑MVP). |
| **Marketplace revenue** | $15 k ARR from paid templates by Q4 2027. |
| **Enterprise contracts** | ≥ 3 mid‑size customers (>$5k ARR each) by Q2 2027. |

---  

## Risks & Mitigations  

| Risk | Impact | Mitigation |
|------|--------|------------|
| **Generated code security flaws** | High (customer trust) | Integrated OWASP linting, continuous security testing, manual audit for first 100 releases. |
| **Model hallucination / incorrect specs** | Medium | Prompt guardrails, human‑in‑the‑loop review UI, fallback to template generation. |
| **Infrastructure cost spikes** | Medium | Autoscaling limits, cost‑monitoring dashboards, tiered pricing for compute usage. |
| **Regulatory compliance for user data** | High (enterprise) | Early design of GDPR‑ready data handling, opt‑in consent, audit logs. |
| **Competitive no‑code platforms** | Medium | Differentiate via AI‑first code quality, open‑source model stack, fine‑tuning capability. |

---  

## Ownership & Communication  

- **Product Lead:** Maya Chen – Roadmap governance, OKR alignment.  
- **Engineering Lead:** Luis Ortega – MVP delivery, architecture decisions.  
- **AI/ML Lead:** Priya Nair – Model integration, safety pipelines.  
- **Design Lead:** Samir Patel – UI/UX for spec builder & dashboard.  
- **DevOps Lead:** Elena Rossi – Deploy pipeline, cloud cost management.  
- **QA Lead:** Tomás García – Test strategy, security guardrails.  

Weekly syncs (Mon 10 am PT) + bi‑weekly stakeholder demo. All updates tracked in the **Axentx BRAIN** vector store for continuous learning.

---  

*Prepared by the codecraft senior product/engineering team – 2026‑05‑19*
