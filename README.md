<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&height=200&color=0:0f172a,50:1e293b,100:0f172a&text=Chirag%20Sahani&fontSize=42&fontColor=e2e8f0&animation=fadeIn&fontAlignY=40&desc=AI%20Software%20Engineer%20-%20Backend%20and%20Systems%20Architecture&descAlignY=62&descSize=18"/>

<a href="https://www.linkedin.com/in/chiragsahani"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white"/></a>
<a href="https://chiragsahani.netlify.app"><img src="https://img.shields.io/badge/Portfolio-0f172a?style=flat-square&logo=vercel&logoColor=white"/></a>
<a href="https://github.com/chiragSahani"><img src="https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white"/></a>

</div>

<br/>

## Overview

```yaml
role:            AI Software Engineer, Trao Technologies (remote)
focus:           Backend systems, multi-tenant architecture, AI/RAG platforms
education:       B.Tech CSE, Chandigarh Group of Colleges — Gold Medalist, GPA 8.7
current_build:   Melior — AI proposal automation platform
problem_solving: 1,300+ DSA problems, multiple top-100 national rankings
location:        Haldwani, Uttarakhand, India
```

I design and ship backend systems for multi-tenant SaaS products — API layers, authorization models, and data pipelines that need to hold up under real traffic, not just demo well. Most of my recent work sits at the intersection of conventional backend engineering (REST APIs, RBAC, queues, indexing) and applied AI (RAG pipelines, document ingestion, LLM-backed automation).

---

## System Design

Representative request path for the multi-tenant platforms I build:

```mermaid
flowchart LR
    Client[Client — React / Next.js] --> Gateway[API Gateway]
    Gateway --> Auth[Auth Layer — JWT + RBAC]
    Gateway --> Rate[Rate Limiting / Validation]
    Auth --> Service[Service Layer]
    Service --> DB[(MongoDB / PostgreSQL)]
    Service --> Cache[(Redis)]
    Service --> Queue[BullMQ Workers]
    Service --> AI[RAG / LLM Pipeline]
    AI --> Vector[(Vector Store)]
    Queue --> Notify[Notification Service]
```

**Patterns applied consistently across projects**

| Concern | Approach |
|---|---|
| Layering | Controller → Service → Repository, no business logic in route handlers |
| Tenancy | Organization-scoped data access enforced at the service layer, not just the query |
| AuthZ | JWT sessions + role-based middleware, permission checks colocated with the resource |
| Performance | Compound/indexed queries, aggregation pipelines over in-memory filtering |
| Async work | Redis-backed BullMQ queues for anything that shouldn't block the request cycle |
| API surface | Versioned REST endpoints, consistent error envelope, centralized error handling |
| AI integration | Document ingestion → chunking → vector storage → retrieval-augmented generation |

---

## Selected Work

**Melior — AI Proposal Automation** · *Trao Technologies*
Platform that automates proposal generation for client-facing teams — document ingestion, AI-assisted drafting, and pricing/portal access workflows, with the internal onboarding and comms tooling built around it.

**Enterprise LMS Platform**
Multi-tenant learning management system with organization-level data isolation, invitation-based onboarding, course/enrollment engines, session lifecycle management, and an aggregation-driven analytics dashboard on MongoDB.

**Nexus**
Modular full-stack platform built around versioned REST APIs and indexing strategy tuned for read-heavy access patterns.

**JobbyApp**
SaaS platform with protected routing and session-based authentication control.

**CareConnect**
Healthcare analytics dashboard, optimized for rendering large result sets without blocking the UI thread.

**InsydNotification**
Reusable, typed notification component system built for reuse across multiple frontends.

---

## Stack

<p>
<img src="https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white"/>
<img src="https://img.shields.io/badge/Express-000000?style=flat-square&logo=express&logoColor=white"/>
<img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white"/>
<img src="https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black"/>
<img src="https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white"/>
<img src="https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white"/>
<img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white"/>
<img src="https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white"/>
<img src="https://img.shields.io/badge/BullMQ-CC0000?style=flat-square"/>
<img src="https://img.shields.io/badge/NGINX-009639?style=flat-square&logo=nginx&logoColor=white"/>
<img src="https://img.shields.io/badge/PM2-2B037A?style=flat-square"/>
<img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white"/>
<img src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white"/>
<img src="https://img.shields.io/badge/DigitalOcean-0080FF?style=flat-square&logo=digitalocean&logoColor=white"/>
<img src="https://img.shields.io/badge/Vercel-000000?style=flat-square&logo=vercel&logoColor=white"/>
<img src="https://img.shields.io/badge/OpenAI_API-412991?style=flat-square&logo=openai&logoColor=white"/>
<img src="https://img.shields.io/badge/RAG_Pipelines-1e293b?style=flat-square"/>
<img src="https://img.shields.io/badge/Vector_Storage-1e293b?style=flat-square"/>
</p>

| Layer | Tools |
|---|---|
| Backend | Node.js, Express, REST API design, middleware pipelines |
| Data | MongoDB (schema design, aggregation pipelines), PostgreSQL, Redis |
| Async / Jobs | BullMQ, Redis-backed queues |
| Auth | JWT, RBAC, session management |
| AI / ML | OpenAI-compatible LLM APIs, RAG pipelines, document ingestion, vector storage, NLP workflows |
| Infra | Docker, NGINX, PM2, CI/CD, DigitalOcean, Vercel |
| Frontend | React, Next.js, TypeScript |

---

## Metrics

<div align="center">

<img src="https://github-stats-extended.vercel.app/api?username=chiragSahani&show_icons=true&theme=github_dark&hide_border=true&count_private=true&include_all_commits=true" height="165"/>
<img src="https://github-stats-extended.vercel.app/api/top-langs/?username=chiragSahani&layout=compact&theme=github_dark&hide_border=true" height="165"/>

<img src="https://streak-stats.demolab.com/?user=chiragSahani&theme=github-dark-blue&hide_border=true" height="165"/>

<img src="https://github-readme-activity-graph.vercel.app/graph?username=chiragSahani&theme=github-compact&hide_border=true&bg_color=0d1117" width="97%"/>

</div>

> Stats run on **GitHub Stats Extended** (`github-stats-extended.vercel.app`), the actively maintained successor to the original `github-readme-stats` project (which has been paused), plus `streak-stats.demolab.com`, the maintainer's own stable hosted domain rather than a generic Vercel deploy. This avoids the token/rate-limit failures a self-hosted fork hits. If a card is briefly unreachable, it's almost always a transient GitHub API rate limit on the shared instance, not a config error on your end.

---

## Strengths

<table>
<tr>
<td valign="top" width="33%">

**Backend**
- REST API design
- Multi-tenant architecture
- RBAC & session-based auth
- Aggregation & analytics queries
- Middleware pipelines
- Database indexing strategy

</td>
<td valign="top" width="33%">

**AI Systems**
- LLM API integration
- RAG pipeline design
- Document ingestion & chunking
- Vector storage
- NLP-driven automation

</td>
<td valign="top" width="33%">

**Infra / DevOps**
- Docker
- CI/CD pipelines
- NGINX, PM2 process management
- Cloud deployment (DigitalOcean, Vercel)

</td>
</tr>
</table>

---

## Recognition

- Gold Medalist, B.Tech Computer Science Engineering — GPA 8.7
- State-Level Silver Medal, Skill India
- 1,300+ algorithmic problems solved across competitive programming platforms
- Multiple top-100 national rankings

---

<div align="center">

<a href="https://www.linkedin.com/in/chiragsahani"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white"/></a>
<a href="https://github.com/chiragSahani"><img src="https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white"/></a>
<a href="https://chiragsahani.netlify.app"><img src="https://img.shields.io/badge/Portfolio-0f172a?style=flat-square&logo=vercel&logoColor=white"/></a>

<sub>Clean architecture. Measurable performance. Systems that scale predictably.</sub>

<img src="https://capsule-render.vercel.app/api?type=waving&height=100&color=0:0f172a,50:1e293b,100:0f172a&section=footer"/>

</div>
