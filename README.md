<div align="center">

<img src="https://raw.githubusercontent.com/Trilokia/Trilokia/master/gradient.gif" width="100%" height="4" alt="" />

<br/>

<img src="https://github.com/grantli0727.png" width="120" height="120" alt="Grant Li" />

# Grant Li

### Senior Software Engineer  
**AI / LLM · Backend · React / Next.js**

[![Portfolio](https://img.shields.io/badge/Portfolio-grant--li.vercel.app-E91D25?style=for-the-badge&logo=vercel&logoColor=white)](https://grant-li.vercel.app/)
[![GitHub](https://img.shields.io/badge/GitHub-grantli0727-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/grantli0727)
[![Email](https://img.shields.io/badge/Email-grantli0727%40gmail.com-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:grantli0727@gmail.com)

<br/>

<img src="https://readme-typing-svg.demolab.com?font=Poppins&weight=600&size=26&duration=3200&pause=900&color=E91D25&center=true&vCenter=true&width=780&lines=Shipping+AI+products+people+trust;RAG+%7C+Agents+%7C+Evals+%7C+Guardrails;Python+%2F+FastAPI+%7C+Node+%7C+TypeScript;React+%2F+Next.js+at+production+scale" alt="Typing headline" />

<br/>

<img src="https://skillicons.dev/icons?i=typescript,python,nodejs,react,nextjs,fastapi,postgres,redis,aws,docker,kubernetes,terraform,graphql,tailwind,git,githubactions&theme=dark&perline=8" alt="Core skills" />

</div>

---

## <img src="https://raw.githubusercontent.com/Tarikul-Islam-Anik/Animated-Fluent-Emojis/master/Emojis/Objects/Gear.png" width="28" height="28" /> Technical introduction

I am a **Senior Software Engineer** with **7+ years** shipping production software. My work sits at the intersection of **large language model applications**, **reliable backend services**, and **high-quality React / Next.js interfaces**.

I care less about demos that look clever in a slide deck and more about systems that survive real traffic: grounded answers, predictable latency, controlled cost, observable failure modes, and UIs that stay fast under load. I think in measurements first — eval sets, p95s, conversion lifts, and error budgets.

Below is how I work technically, end to end.

<div align="center">

| 🚀 Focus | 🎯 Outcome |
| :---: | :---: |
| **AI systems people trust** | Grounded RAG · agents · guardrails |
| **Backends that hold** | Scale · latency · uptime |
| **Front ends that feel sharp** | SSR · streaming · accessibility |

</div>

---

## <img src="https://raw.githubusercontent.com/Tarikul-Islam-Anik/Animated-Fluent-Emojis/master/Emojis/Smilies/Robot.png" width="28" height="28" /> AI & LLM engineering

I design and ship **end-to-end LLM features** — not just prompt experiments.

<div align="center">
<img src="https://skillicons.dev/icons?i=python,fastapi,postgres,aws,docker&theme=dark" alt="AI stack icons" />
</div>

<br/>

### Retrieval-augmented generation (RAG)

- Build retrieval pipelines that mix **structured routing** (exact SQL / deterministic paths for known question shapes) with **vector search** for open-ended queries.
- Use **pgvector** (and similar embedding stores) for semantic retrieval, with careful chunking, metadata filters, and re-ranking so context stays relevant and cheap.
- Require **grounded citations**: every answer that claims a fact should point at a source.

**In production:** raised RAG answer accuracy from **72% → 94%** on a **300-question** eval set; cut fabricated answers by **~90%**.

### Agents, tools, and actions

- Implement **tool / function calling** so models can fetch data, draft actions, or call internal APIs — with clear schemas and timeouts.
- Separate **“suggest”** from **“do”**: anything that reaches external users or irreversible side effects goes through **guardrails + human approval** when needed.
- Prefer small, composable tools over one mega-agent that is hard to debug.

### Evals, prompts, and cost control

- Maintain **evaluation sets** (golden questions, regression suites) and run them on a cadence.
- Treat prompts as versioned artifacts: change control, A/B where it matters, and fallbacks (“I don’t know”) when confidence is low.
- Optimize **LLM spend**: embedding caches, smaller models for simple tasks, batching, and avoiding unused context — held monthly LLM costs **~60% below** early estimates while improving quality.

### Models & orchestration

Claude / OpenAI APIs · embeddings · pgvector · Python services that orchestrate retrieval, grounding, streaming, and policy checks.

---

## <img src="https://raw.githubusercontent.com/Tarikul-Islam-Anik/Animated-Fluent-Emojis/master/Emojis/Objects/Desktop%20Computer.png" width="28" height="28" /> Backend systems

I build backends that stay boring under pressure: clear contracts, strong data models, and ops that don’t rely on heroics.

<div align="center">
<img src="https://skillicons.dev/icons?i=nodejs,typescript,express,python,fastapi,postgres,redis,graphql&theme=dark" alt="Backend stack icons" />
</div>

<br/>

### Languages & frameworks

- **Python / FastAPI** for AI orchestration, RAG services, and high-readability API layers.
- **Node.js / Express** and **TypeScript** for product APIs that share types with the front end.
- Comfortable across **REST** and **GraphQL** depending on client needs and schema ownership.

### Data & consistency

- **PostgreSQL** as the system of record — indexing, query design, and schema evolution under load.
- **Redis** for caching hot paths, rate limits, and session-adjacent state.
- Auth: **OAuth 2.0**, **JWT**, and service-to-service boundaries that don’t leak trust.

### Scale & reliability

- Scaled APIs to **1M+ requests/day** at **99.95%** uptime with caching, rate limiting, and horizontal scaling.
- Cut **p95 API latency ~42%** via query redesign, Redis, and removing redundant service hops.
- Reduced **MTTR ~40%** with dashboards, structured logging, and on-call runbooks.

### How I design services

1. Define the **user contract** and failure modes first.  
2. Make the happy path fast; make the error path **explicit and observable**.  
3. Prefer idempotent writes and clear ownership of data.  
4. Load-test assumptions before they become incidents.

---

## <img src="https://raw.githubusercontent.com/Tarikul-Islam-Anik/Animated-Fluent-Emojis/master/Emojis/Objects/Artist%20Palette.png" width="28" height="28" /> Frontend — React & Next.js

I ship interfaces that feel product-grade: fast first paint, accessible interaction, and streaming where AI answers need it.

<div align="center">
<img src="https://skillicons.dev/icons?i=react,nextjs,typescript,tailwind,js,html,css,vercel&theme=dark" alt="Frontend stack icons" />
</div>

<br/>

### Core stack

- **React** + **TypeScript** as the default UI layer.
- **Next.js** with **SSR**, **ISR**, **streaming**, and careful code splitting.
- **Tailwind CSS** for consistent, maintainable design systems.
- State with **Zustand / Redux** when client complexity earns it — not by default.

### Performance & UX craft

- Improved Lighthouse from **58 → 92** and cut load time **~45%** through ISR, splitting, and image pipelines.
- Improved page load **~30%** and key-workflow engagement **~9%** through targeted performance work.
- Build **accessible** UIs (keyboard, focus, contrast, semantics).

### AI in the UI

- Stream tokens into the interface so wait time feels productive.
- Show **sources / citations** next to answers so trust is visible.
- Keep loading, empty, and error states intentional — AI UIs fail differently than CRUD forms.

### Product loop

I’ve run **15+ A/B experiments** with SQL + stats discipline, driving **6–12%** conversion gains on permanent rollouts. Frontend work is instrumented product surface — not decoration.

---

## <img src="https://raw.githubusercontent.com/Tarikul-Islam-Anik/Animated-Fluent-Emojis/master/Emojis/Travel%20and%20places/Cloud.png" width="28" height="28" /> Cloud, DevOps & observability

Production is part of the feature.

<div align="center">
<img src="https://skillicons.dev/icons?i=aws,docker,kubernetes,terraform,githubactions,linux,nginx&theme=dark" alt="Cloud stack icons" />
</div>

<br/>

| Layer | Tools & practices |
| --- | --- |
| **Cloud** | AWS — EC2, S3, Lambda, RDS, EKS, CloudFront |
| **Containers** | Docker, Kubernetes |
| **IaC** | Terraform — environments as code, cost-aware sizing |
| **CI/CD** | GitHub Actions, Jenkins — fast, gated deploys |
| **Observability** | Datadog, structured logs, dashboards, alerts, runbooks |

Lowered cloud spend on the order of **~$15K/month** through right-sizing, CDN/storage hygiene, and Terraform-backed infra — quality and cost are the same conversation.

---

## <img src="https://raw.githubusercontent.com/Tarikul-Islam-Anik/Animated-Fluent-Emojis/master/Emojis/Objects/Hammer%20and%20Wrench.png" width="28" height="28" /> Engineering practices

- **System design** before coding paths that will live for years  
- **Automated tests** — Jest, Pytest, Cypress, Playwright  
- **Code review** as safety and teaching, not a rubber stamp  
- **Agile delivery** with clear ownership and staged rollout  
- Documentation and mentoring so systems stay understandable

---

## <img src="https://raw.githubusercontent.com/Tarikul-Islam-Anik/Animated-Fluent-Emojis/master/Emojis/Objects/Toolbox.png" width="28" height="28" /> Skills & tools

### Languages

<p>
  <img alt="TypeScript" src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white" />
  <img alt="JavaScript" src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" />
  <img alt="Python" src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" />
  <img alt="SQL" src="https://img.shields.io/badge/SQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white" />
  <img alt="HTML5" src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white" />
  <img alt="CSS3" src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white" />
</p>

### AI & LLM

<p>
  <img alt="OpenAI" src="https://img.shields.io/badge/OpenAI-412991?style=for-the-badge&logo=openai&logoColor=white" />
  <img alt="Claude" src="https://img.shields.io/badge/Claude-D97757?style=for-the-badge&logo=anthropic&logoColor=white" />
  <img alt="RAG" src="https://img.shields.io/badge/RAG-E91D25?style=for-the-badge" />
  <img alt="Agents" src="https://img.shields.io/badge/Agents%20%26%20Tools-111827?style=for-the-badge" />
  <img alt="pgvector" src="https://img.shields.io/badge/pgvector-4169E1?style=for-the-badge&logo=postgresql&logoColor=white" />
  <img alt="Prompt Eng" src="https://img.shields.io/badge/Prompt%20Engineering-6D28D9?style=for-the-badge" />
  <img alt="Evals" src="https://img.shields.io/badge/Eval%20Sets-0F766E?style=for-the-badge" />
  <img alt="Guardrails" src="https://img.shields.io/badge/Guardrails-BE123C?style=for-the-badge" />
</p>

### Backend

<p>
  <img alt="FastAPI" src="https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white" />
  <img alt="Node.js" src="https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white" />
  <img alt="Express" src="https://img.shields.io/badge/Express-000000?style=for-the-badge&logo=express&logoColor=white" />
  <img alt="REST" src="https://img.shields.io/badge/REST-02569B?style=for-the-badge" />
  <img alt="GraphQL" src="https://img.shields.io/badge/GraphQL-E10098?style=for-the-badge&logo=graphql&logoColor=white" />
  <img alt="WebSockets" src="https://img.shields.io/badge/WebSockets-4353FF?style=for-the-badge" />
  <img alt="OAuth" src="https://img.shields.io/badge/OAuth%202.0-EB5424?style=for-the-badge" />
  <img alt="JWT" src="https://img.shields.io/badge/JWT-000000?style=for-the-badge&logo=jsonwebtokens&logoColor=white" />
</p>

### Frontend

<p>
  <img alt="React" src="https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black" />
  <img alt="Next.js" src="https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white" />
  <img alt="SSR" src="https://img.shields.io/badge/SSR%20%2F%20ISR-111827?style=for-the-badge&logo=nextdotjs&logoColor=white" />
  <img alt="Tailwind" src="https://img.shields.io/badge/Tailwind-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white" />
  <img alt="Zustand" src="https://img.shields.io/badge/Zustand-443E38?style=for-the-badge" />
  <img alt="Redux" src="https://img.shields.io/badge/Redux-764ABC?style=for-the-badge&logo=redux&logoColor=white" />
  <img alt="Framer Motion" src="https://img.shields.io/badge/Framer%20Motion-0055FF?style=for-the-badge&logo=framer&logoColor=white" />
  <img alt="A11y" src="https://img.shields.io/badge/Accessible%20UI-2E7D32?style=for-the-badge" />
</p>

### Data

<p>
  <img alt="PostgreSQL" src="https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white" />
  <img alt="MySQL" src="https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white" />
  <img alt="MongoDB" src="https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white" />
  <img alt="Redis" src="https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white" />
</p>

### Cloud & DevOps

<p>
  <img alt="AWS" src="https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazonwebservices&logoColor=FF9900" />
  <img alt="Docker" src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" />
  <img alt="Kubernetes" src="https://img.shields.io/badge/Kubernetes-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white" />
  <img alt="Terraform" src="https://img.shields.io/badge/Terraform-7B42BC?style=for-the-badge&logo=terraform&logoColor=white" />
  <img alt="GitHub Actions" src="https://img.shields.io/badge/GitHub%20Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white" />
  <img alt="Jenkins" src="https://img.shields.io/badge/Jenkins-D24939?style=for-the-badge&logo=jenkins&logoColor=white" />
  <img alt="Datadog" src="https://img.shields.io/badge/Datadog-632CA6?style=for-the-badge&logo=datadog&logoColor=white" />
  <img alt="Linux" src="https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black" />
</p>

### Testing & quality

<p>
  <img alt="Jest" src="https://img.shields.io/badge/Jest-C21325?style=for-the-badge&logo=jest&logoColor=white" />
  <img alt="Pytest" src="https://img.shields.io/badge/Pytest-0A9EDC?style=for-the-badge&logo=pytest&logoColor=white" />
  <img alt="Cypress" src="https://img.shields.io/badge/Cypress-17202C?style=for-the-badge&logo=cypress&logoColor=white" />
  <img alt="Playwright" src="https://img.shields.io/badge/Playwright-2EAD33?style=for-the-badge&logo=playwright&logoColor=white" />
</p>

---

## <img src="https://raw.githubusercontent.com/Tarikul-Islam-Anik/Animated-Fluent-Emojis/master/Emojis/Symbols/Sparkles.png" width="28" height="28" /> In one sentence

I ship **AI products with measurable quality**, **backends that hold up at scale**, and **Next.js front ends** that stay fast, accessible, and honest about what the model knows.

---

<div align="center">

<img src="https://raw.githubusercontent.com/Trilokia/Trilokia/master/gradient.gif" width="100%" height="4" alt="" />

<br/>

[![Portfolio](https://img.shields.io/badge/🌐_Live_Portfolio-E91D25?style=for-the-badge)](https://grant-li.vercel.app/)
[![GitHub](https://img.shields.io/badge/💻_GitHub-181717?style=for-the-badge&logo=github)](https://github.com/grantli0727)
[![Email](https://img.shields.io/badge/✉️_Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:grantli0727@gmail.com)

<br/>

<sub>Built with care · brand <code>#e91d25</code></sub>

</div>
