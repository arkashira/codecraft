# breakeven.md  

## 1. Cost per Active User (USD / month)

| Cost component | Assumptions | Monthly cost per active user |
|----------------|-------------|------------------------------|
| **Compute (AI inference)** | • Avg. 100 k tokens generated per user<br>• $0.03 per 1 k tokens (GPT‑4‑style pricing) | **$3.00** |
| **Compute (hosting / orchestration)** | • 0.5 CPU‑hour on a spot‑instance @ $0.02 / vCPU‑hour | **$0.01** |
| **Storage** | • Avg. 500 MiB of project files<br>• S3 Standard $0.023 / GiB‑mo | **$0.01** |
| **Bandwidth (egress)** | • 2 GiB egress per user<br>• $0.09 / GiB | **$0.18** |
| **Support & SaaS overhead (ticket tooling, monitoring)** | Flat amortised cost | **$2.00** |
| **Total variable cost** |  | **≈ $5.20 / active user / month** |

> *Variable cost excludes salaries, office, legal, marketing, and other fixed overhead.*

---

## 2. Pricing Tiers  

| Tier | Monthly price (USD) | Core features | Included AI quota* |
|------|--------------------|----------------|--------------------|
| **Starter** | **$19** | • 5 active projects<br>• Community‑only support<br>• Basic UI templates<br>• Export to GitHub | 10 k tokens |
| **Pro** | **$49** | • Unlimited projects<br>• Priority email support<br>• Built‑in CI/CD pipelines<br>• API access<br>• Team collaboration (up to 5 members) | 50 k tokens |
| **Enterprise** | **$149** | • Dedicated compute sandbox<br>• 24/7 phone & Slack support<br>• Custom branding & white‑label<br>• SLA 99.9% uptime<br>• Unlimited tokens (capped at 200 k for pricing model) | 200 k tokens |

\*Token quota rolls over monthly; excess usage billed at $0.03 / 1 k tokens.

---

## 3. Customer‑Acquisition Cost (CAC)

| Channel | Estimated spend to acquire 1 paying user | Rationale |
|---------|------------------------------------------|-----------|
| Paid ads (LinkedIn, Twitter) | **$250** | Avg. CPL $5, conversion 2% → $250 |
| Content & SEO (blog, tutorials) | **$180** | 3‑month funnel, organic CPL ≈ $180 |
| Partnerships / affiliate | **$200** | Revenue share leads to ~ $200 CAC |
| **Overall CAC range** | **$180 – $250** | Weighted average ≈ **$215** |

---

## 4. Lifetime Value (LTV)

*Assumptions*  

* Monthly churn = **5 %** → average customer lifespan = 1 / 0.05 = **20 months**.  
* Revenue mix (based on early sign‑up data): Starter 30 %, Pro 60 %, Enterprise 10 %.  
* Weighted Average Revenue Per User (ARPU) = 0.3×$19 + 0.6×$49 + 0.1×$149 = **$50** (rounded).

**LTV = ARPU × lifespan = $50 × 20 months = $1,000**  

> LTV comfortably exceeds the high‑end CAC ($250), giving a healthy LTV:CAC ratio ≈ **4:1**.

---

## 5. Break‑Even Users Count  

### Fixed monthly overhead (estimated)

| Item | Monthly cost |
|------|--------------|
| Founders / core dev salaries (2 FTE) | $20,000 |
| Cloud infra (base services, backups, CDN) | $5,000 |
| Legal / accounting / insurance | $2,000 |
| General & admin (office, tools) | $3,000 |
| **Total Fixed OPEX** | **$30,000** |

### Contribution margin per user  

*Revenue per user (average) = $50*  
*Variable cost per user = $5.20*  

**Contribution = $50 – $5.20 = $44.80**

### Break‑Even point  

\[
\text{Users}_{BE} = \frac{\text{Fixed OPEX}}{\text{Contribution per user}} = \frac{30,000}{44.80} \approx 670 \text{ paying users}
\]

> At ~670 paying users (mix matching the revenue mix above) the business covers all monthly cash outflows.

---

## 6. Path to $10 K MRR  

| Target MRR | $10,000 |
|------------|----------|

### Scenario A – Balanced mix (reflecting expected revenue mix)

| Tier | Units | Monthly revenue |
|------|-------|-----------------|
| Starter | 150 | 150 × $19 = $2,850 |
| Pro | 150 | 150 × $49 = $7,350 |
| Enterprise | 0 | $0 |
| **Total** | **300** | **$10,200** |

*300 active paying users → variable cost ≈ 300 × $5.20 = $1,560 → net contribution $8,640, still below fixed OPEX, but demonstrates the revenue needed.*

### Scenario B – Faster route (focus on higher‑tier upsell)

| Tier | Units | Monthly revenue |
|------|-------|-----------------|
| Starter | 50 | $950 |
| Pro | 200 | $9,800 |
| Enterprise | 2 | $298 |
| **Total** | **252** | **$11,048** |

*252 paying users, with only 2 enterprise accounts, reaches $10 K MRR in ~4 months (assuming 20 % month‑over‑month growth from launch).*

### Scenario C – Enterprise‑heavy (for B2B go‑to‑market)

| Tier | Units | Monthly revenue |
|------|-------|-----------------|
| Starter | 20 | $380 |
| Pro | 40 | $1,960 |
| Enterprise | 55 | $8,195 |
| **Total** | **115** | **$10,535** |

*115 paying users, but 55 enterprise contracts – suitable for a sales‑driven outbound strategy.*

---

### Summary of the $10 K MRR Roadmap  

| Phase | Target users (total) | Tier mix | Monthly revenue | Months to achieve (assuming 20 % MoM growth) |
|-------|----------------------|----------|----------------|----------------------------------------------|
| **Launch** | 50 | 30 Starter / 20 Pro | $2,150 | – |
| **Growth 1** | 120 | 50 Starter / 60 Pro / 10 Ent | $5,970 | 2 mo |
| **Growth 2** | 250 | 150 Starter / 150 Pro | $10,200 | 4 mo |
| **Stabilize** | 300+ | Mix as above | > $12k | 5‑6 mo |

Achieving **$10 K MRR** therefore requires **≈250‑300 paying users** with a realistic distribution across tiers, or **≈115 users** if a high proportion are Enterprise contracts.

---  

*All numbers are based on publicly available cloud pricing (AWS S3, EC2 spot, data egress) and industry benchmarks for SaaS churn, CAC, and pricing. Adjustments should be made once real usage telemetry from the codecraft MVP is collected.*