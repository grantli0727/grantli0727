<div align="center">

# Grant Li

**Senior Software Engineer**  
AI / LLM Applications · Backend Systems · React / Next.js

New York, NY · [Portfolio](https://grant-li.vercel.app/) · [LinkedIn](https://www.linkedin.com/in/grant-li/) · [Email](mailto:grantli0727@gmail.com)

<br/>

<img src="https://readme-typing-svg.demolab.com?font=Poppins&weight=600&size=24&duration=3400&pause=1000&color=E91D25&center=true&vCenter=true&width=780&lines=I+build+AI+systems+people+can+trust;RAG+%C2%B7+Agents+%C2%B7+Evals+%C2%B7+Guardrails;Python+%2F+FastAPI+%C2%B7+Node+%C2%B7+TypeScript;Next.js+at+production+scale" alt="Typing headline" />

</div>

---

## Technical introduction

I am a **Senior Software Engineer** with **7+ years** shipping production software at **Pinterest**, **OpenSea**, and **Facebook**. My work sits at the intersection of **large language model applications**, **reliable backend services**, and **high-quality React / Next.js interfaces**.

I care less about demos that look clever in a slide deck and more about systems that survive real traffic: grounded answers, predictable latency, controlled cost, observable failure modes, and UIs that stay fast under load. My training is **B.S. Statistics & Computer Science (UIUC)** — I still think in measurements first: eval sets, p95s, conversion lifts, error budgets.

Below is how I work technically, end to end.

---

## AI & LLM engineering

I design and ship **end-to-end LLM features** — not just prompt experiments.

### Retrieval-augmented generation (RAG)

- Build retrieval pipelines that mix **structured routing** (exact SQL / deterministic paths for known question shapes) with **vector search** for open-ended queries.
- Use **pgvector** (and similar embedding stores) for semantic retrieval, with careful chunking, metadata filters, and re-ranking so context stays relevant and cheap.
- Require **grounded citations**: every answer that claims a fact should point at a source. That single constraint cuts hallucination more than clever wording alone.

**Result in production:** raised RAG answer accuracy from **72% → 94%** on a **300-question** eval set; cut fabricated answers by **~90%**.

### Agents, tools, and actions

- Implement **tool / function calling** so models can fetch data, draft actions, or call internal APIs — with clear schemas and timeouts.
- Separate **“suggest”** from **“do”**: anything that reaches external users or irreversible side effects goes through **guardrails + human approval** when needed.
- Prefer small, composable tools over one mega-agent that is hard to debug.

### Evals, prompts, and cost control

- Maintain **evaluation sets** (golden questions, regression suites) and run them on a cadence — weekly where quality is a product promise.
- Treat prompts as versioned artifacts: change control, A/B where it matters, and fallbacks (“I don’t know”) when confidence is low.
- Optimize **LLM spend**: embedding caches, smaller models for simple tasks, batching, and avoiding retrieval of unused context. Held monthly LLM costs **~60% below** early estimates while improving quality.

### Models & stack

Claude / OpenAI APIs · embeddings · pgvector · Python services that orchestrate retrieval, grounding, streaming, and policy checks.

---

## Backend systems

I build backends that stay boring under pressure: clear contracts, strong data models, and ops that don’t rely on heroics.

### Languages & frameworks

- **Python / FastAPI** for AI orchestration, RAG services, and high-readability API layers.
- **Node.js / Express** and **TypeScript** for marketplace and product APIs that need shared types with the front end.
- Comfortable across **REST** and **GraphQL** depending on client needs and schema ownership.

### Data & consistency

- **PostgreSQL** as the system of record — query design, indexing, and schema evolution that respect production load.
- **Redis** for caching hot paths, rate limits, and session-adjacent state.
- Auth patterns: **OAuth 2.0**, **JWT**, and service-to-service boundaries that don’t leak trust.

### Scale & reliability (examples)

- Scaled marketplace APIs to **1M+ requests/day** at **99.95%** uptime with caching, rate limiting, and horizontal scaling on AWS.
- Cut **p95 API latency ~42%** (e.g. 840ms → 490ms) via query redesign, Redis, and removing redundant service hops.
- Reduced **MTTR ~40%** with Datadog dashboards, structured logging, and on-call runbooks.

### How I design services

1. Define the **user contract** and failure modes first.  
2. Make the happy path fast; make the error path **explicit and observable**.  
3. Prefer idempotent writes and clear ownership of data.  
4. Load-test assumptions before they become incidents.

---

## Frontend — React & Next.js

I ship interfaces that feel product-grade: fast first paint, accessible interaction, and streaming where AI answers need it.

### Core stack

- **React** + **TypeScript** as the default UI layer.
- **Next.js** with **SSR**, **ISR**, **streaming**, and careful code splitting.
- **Tailwind CSS** for consistent, maintainable design systems.
- State with **Zustand / Redux** when client complexity earns it — not by default.

### Performance & UX craft

- Improved Lighthouse from **58 → 92** and cut load time **~45%** through ISR, splitting, and image pipelines.
- Improved page load **~30%** and key-workflow engagement **~9%** through targeted performance work.
- Build **accessible** UIs (keyboard, focus, contrast, semantics) — especially for internal tools used all day.

### AI in the UI

- Stream tokens into the interface so wait time feels productive.
- Show **sources / citations** next to answers so trust is visible, not implied.
- Keep loading, empty, and error states intentional — AI UIs fail differently than CRUD forms.

### Product loop

I’ve run **15+ A/B experiments** with SQL + stats discipline, driving **6–12%** conversion gains on permanent rollouts. Frontend work is not decoration; it’s instrumented product surface.

---

## Cloud, DevOps & observability

Production is part of the feature.

| Layer | Tools & practices |
| --- | --- |
| **Cloud** | AWS — EC2, S3, Lambda, RDS, EKS, CloudFront |
| **Containers** | Docker, Kubernetes |
| **IaC** | Terraform — environments as code, cost-aware sizing |
| **CI/CD** | GitHub Actions, Jenkins — fast, gated deploys |
| **Observability** | Datadog, structured logs, dashboards, alerts, runbooks |

I’ve lowered AWS spend on the order of **~$15K/month** through right-sizing, S3/CloudFront hygiene, and Terraform-backed infra — quality and cost are the same conversation.

---

## Engineering practices I won’t skip

- **System design** before coding paths that will live for years.  
- **Automated tests** (Jest, Pytest, Cypress, Playwright) on the paths that break users.  
- **Code review** as a teaching and safety mechanism, not a rubber stamp.  
- **Agile delivery** with clear ownership and staged rollout.  
- Documentation and mentoring so the system is understandable when I’m not in the room.

---

## Stack at a glance

<p>
  <img alt="TypeScript" src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white" />
  <img alt="Python" src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" />
  <img alt="FastAPI" src="https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white" />
  <img alt="Node.js" src="https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white" />
  <img alt="React" src="https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black" />
  <img alt="Next.js" src="https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white" />
  <img alt="PostgreSQL" src="https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white" />
  <img alt="Redis" src="https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white" />
  <img alt="GraphQL" src="https://img.shields.io/badge/GraphQL-E10098?style=for-the-badge&logo=graphql&logoColor=white" />
  <img alt="AWS" src="https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazonwebservices&logoColor=FF9900" />
  <img alt="Docker" src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" />
  <img alt="Kubernetes" src="https://img.shields.io/badge/Kubernetes-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white" />
  <img alt="Terraform" src="https://img.shields.io/badge/Terraform-7B42BC?style=for-the-badge&logo=terraform&logoColor=white" />
  <img alt="Tailwind CSS" src="https://img.shields.io/badge/Tailwind-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white" />
  <img alt="Datadog" src="https://img.shields.io/badge/Datadog-632CA6?style=for-the-badge&logo=datadog&logoColor=white" />
</p>

---

## In one sentence

I ship **AI products with measurable quality**, **backends that hold up at scale**, and **Next.js front ends** that stay fast, accessible, and honest about what the model knows.

<div align="center">

<br/>

<sub>Pinterest · OpenSea · Facebook · UIUC Statistics & CS</sub>

</div>
