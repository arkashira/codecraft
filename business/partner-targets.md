# partner-targets.md  

## Integration Roadmap for **codecraft**  

| # | Partner / API | Free‑Tier Limits (as of 2026‑06) | Integration Effort* | Core User Job Solved | Affiliate / Revenue‑Share Potential | Target Phase |
|---|---------------|----------------------------------|----------------------|----------------------|--------------------------------------|--------------|
| 1 | **OpenAI (GPT‑4o / Codex)** | $18 credit (~3 M tokens) – unlimited requests until credit exhausted | **S** (single REST wrapper, token‑based auth) | *Generate code snippets, refactor, write tests* – the core AI‑coding engine | OpenAI Partner Program (usage‑based revenue share) | **Phase 1** – Core MVP |
| 2 | **GitHub** (Repos, Actions, Marketplace) | Unlimited public repos; 2 k private repo minutes/mo for free accounts | **M** (OAuth, webhook handling, Actions API) | *Version control, CI/CD pipelines, one‑click push to repo* | GitHub Marketplace affiliate (15 % of paid plan upgrades) | **Phase 1** |
| 3 | **Vercel** (Frontend & Edge Deploy) | 100 GB bandwidth, 12 builds/day, 1 GB storage | **S** (Deploy API + preview URLs) | *Instant preview & production deployment of generated front‑ends* | Vercel Partner Program (referral credits + revenue share) | **Phase 2** |
| 4 | **Supabase** (PostgreSQL + Auth + Storage) | 500 MB DB, 2 GB bandwidth, 1 GB storage, 5 k auth users | **M** (client SDK, Row‑Level Security config) | *Zero‑code backend (DB, auth, file storage) for generated apps* | Supabase Referral (up‑to $10 per paid conversion) | **Phase 2** |
| 5 | **Stripe** (Payments & Billing) | No‑upfront fees; pay‑as‑you‑go, $0 setup | **M** (Checkout Sessions, Webhooks) | *Monetize launched SaaS products – subscription & one‑time payments* | Stripe Connect (2 % of transaction volume) | **Phase 3** |
| 6 | **Auth0** (Identity & SSO) | 7 k active users, unlimited logins, 2 social connections | **M** (OAuth2 flow, Rules) | *Secure authentication for generated apps, SSO across providers* | Auth0 Referral (10 % of first‑year ARR) | **Phase 3** |
| 7 | **Algolia** (Search‑as‑a‑Service) | 10 k records, 100 k operations/mo | **M** (Search API, indexing pipelines) | *Add instant search to generated dashboards / marketplaces* | Algolia Partner (revenue share on paid tier upgrades) | **Phase 4** |
| 8 | **Zapier** (Workflow Automation) | 100 tasks/mo, 5 Zaps, 15‑min update interval | **L** (Mapping 3k+ app triggers, OAuth per app) | *Connect generated apps to any of 3 k SaaS tools (CRM, email, etc.)* | Zapier Affiliate (20 % of paid Zapier plan revenue) | **Phase 4** |

\*Effort scale: **S** = ≤1 week (single endpoint, minimal auth); **M** = 2‑4 weeks (multiple endpoints, webhook handling, UI config); **L** = >4 weeks (complex mapping, multi‑step flows, extensive UI).

---

## Phase‑by‑Phase Timeline (Quarterly)

| Quarter | Milestones | Primary Integrations |
|---------|------------|----------------------|
| **Q1 2026** | • Core AI‑code generation engine live<br>• User onboarding & project scaffolding<br>• Deployable preview URLs | OpenAI (core), GitHub (repo + CI) |
| **Q2 2026** | • One‑click production deploy<br>• Built‑in backend services (DB, auth) | Vercel, Supabase |
| **Q3 2026** | • Monetization layer for launched apps<br>• Secure auth for end‑user sign‑in | Stripe, Auth0 |
| **Q4 2026** | • Advanced features: search & automation<br>• Marketplace readiness (partner referrals) | Algolia, Zapier |
| **Beyond** | • Expand to niche vertical APIs (e.g., Twilio, SendGrid) based on user demand | TBD |

---

### Prioritization Rationale  

1. **Revenue‑share & affiliate upside** – OpenAI, GitHub, Vercel, Supabase, Stripe, Auth0, Algolia, Zapier all run partner programs that return a percentage of paid conversions or usage fees.  
2. **Free‑tier sufficiency for early adopters** – Limits are generous enough for indie‑hacker prototypes, ensuring no friction before they upgrade.  
3. **Direct alignment with user jobs** – Each integration removes a manual step: code generation, version control, deployment, backend provisioning, payment processing, authentication, search, and workflow automation.  
4. **Technical feasibility** – All APIs are well‑documented, support OAuth2 / API keys, and have SDKs for Node/TS (our stack).  

---  

**Next steps for the Business‑Synthesis team**  

1. Draft partnership outreach decks for each high‑value partner (OpenAI, GitHub, Vercel, Stripe).  
2. Assign engineering owners to Phase 1 integrations (OpenAI & GitHub) – target **2‑week sprint**.  
3. Set up tracking of affiliate referrals in the BRAIN to feed back revenue impact for future prioritization.  