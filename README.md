<h1 align="center">Hi, I'm Guru Charan Gupta 👋</h1>

<p align="center">
  <b>Senior Full-Stack / AI Engineer</b> · web platforms · LLM &amp; media-model products · agent safety tooling · Cloudflare edge · blockchain infrastructure
</p>

<p align="center">
  <a href="https://anchorage.proofoftech.org">⚓ Anchorage demo</a> &nbsp;·&nbsp;
  <a href="https://kdf-wasm.lordofthechains.com">🧪 KDF WASM Playground</a> &nbsp;·&nbsp;
  <a href="https://linkedin.com/in/gcharang">💼 LinkedIn</a> &nbsp;·&nbsp;
  <a href="mailto:mrgcharang@gmail.com">📧 Email</a>
</p>

<p align="center">
  <img src="https://readme-typing-svg.demolab.com/?font=Fira+Code&size=20&duration=3200&pause=800&center=true&vCenter=true&width=620&color=2F81F7&lines=8%2B+years+shipping+production+systems+end+to+end;Apps+%2B+developer+tooling+%2B+content+infrastructure;LLM+%26+media-model+products+on+the+Cloudflare+edge;Open-source+safety+tooling+for+AI+agent+workflows;Multi-agent+AI+workflows+with+Claude+Code" alt="what I do" />
</p>

---

I'm a software engineer with **8+ years building production systems end to end**: user-facing apps, developer tooling, content infrastructure, and the CI/CD and edge infra beneath them.

For close to eight years (2018-2025) I grew through **five roles** at **Komodo**, an open-source blockchain platform *(core technology acquired by Gleec, 2025)*: documentation, support, QA/DevOps, frontend, and platform engineering. The product was a non-custodial multi-chain wallet and a cross-chain atomic-swap DEX: people held their own keys and traded directly across blockchains, with no exchange in the middle. I was the technical point of contact for the **20+ centralized exchanges** integrating Komodo and its Smart Chains, bridging product, QA, docs, and support across releases. Now I build AI products.

> ⚓ **[Anchorage](https://anchorage.proofoftech.org)** · [source](https://github.com/ProofOfTechOrg/anchorage) · [API reference](https://proofoftechorg.github.io/anchorage/)
>
> Open-source enterprise safety layer for AI agent workflows, built on Mastra, so an agent's outward actions wait for human approval and leave an audit trail. RBAC, per-action audit, egress and write-permission policy, and Cloudflare-native durable execution: a run suspends at an approval step, survives a server restart, and resumes from its snapshot, and CI proves that on the real Workers runtime. Apache-2.0; three libraries on npm, all published with provenance.

> 🧪 **[KDF WASM Playground](https://kdf-wasm.lordofthechains.com)** · [source](https://github.com/gcharang/react-komodefi-wasm)
>
> Komodo's atomic-swap engine, running in a browser tab. A **30+ MB** WebAssembly build behind a service-worker compress/fetch/decompress pipeline: **1.1 s** cold, **231 ms** on return. Integrators, QA, and docs readers fire real RPC calls against it with no local build.

## 🚀 What I'm working on

- 📝 **Writing and running a technical site**, built solo on Astro + Cloudflare Workers: "Ask the Field Notes", a live hybrid-RAG search over the essays (BM25 + Vectorize + Reciprocal Rank Fusion, streamed cited answers), a citation-gated multi-agent content pipeline behind **154 authored posts drawing on 537 arXiv papers**, and a Lighthouse-CI (CWV) performance budget enforced in CI.
- 🧰 Open-sourcing the layers underneath the agents. **[understudy](https://github.com/ProofOfTechOrg/understudy)** is a model-free browser-execution substrate: it drives an already-logged-in Chromium tab over `chrome.debugger`/CDP behind approval gates, with credentials resolved service-side so they never reach a model's context. **[vectorless-rag](https://github.com/ProofOfTechOrg/vectorless-rag)** answers grounded questions over a local PDF corpus without embeddings or a vector database, routing each request through a LangGraph agent and expanding a document tree so every citation resolves to a page. Both MIT, both sole-authored; understudy's protocol and connector ship on npm.
- 🧱 Then building products on those libraries rather than around them. **An agent and capability cloud** gives a hosted agent a priced, metered, governed way to call outside services: a control plane owning definitions and deployments, my own flowsafe Durable Object runner as the only thing that executes a run, a budget-authorizer Durable Object counting in-flight reservations against caps behind a kill switch, and a remote MCP server on the gateway itself. A separate **shadow-mode AML alert-triage platform** takes privacy-masked monitoring and sanctions alerts and returns evidence-cited disposition recommendations while taking no regulated action: a deterministic rules engine runs the mandatory hard stops before any model call, so a model can never recommend closure over a triggered stop, and a human analyst makes every binding decision.
- 💳 Built a complete **stablecoin payment gateway** and operated it end to end on a live public testnet, for a regulated fiat-backed stablecoin on an EVM ZK-rollup L2. Hosted checkout, a merchant SDK and a WooCommerce plugin, signed webhooks, an event-sourced invoice machine over a hash-chained double-entry ledger, custody with maker-checker payouts, KYB/KYT and sanctions screening, and the Solidity contracts underneath, tested in Foundry with a gas-drift gate in CI. My own load test against a single instance held 2,500 concurrent checkout sessions at p95 280 ms.
- 🎙️ Built a **hands-free voice agent** on Cloudflare Workers: one click opens a continuous browser call, speech recognition through Workers AI decides when a turn ends so nobody presses a button, and talking over the reply aborts the model and speech calls mid-turn, dropping audio already in flight so it stops rather than speaking over the person.
- ⚡ **Building AI products at an early-stage venture** as lead frontend engineer &amp; core backend engineer: a real-time, multimodal generative-AI web app (streaming chat + image / video / voice over self-hosted open-source models), with SSE streaming UIs, a Radix design system, and hardened FastAPI backends (BFF cookie auth, CSRF/SSRF hardening, S3-backed media pipelines).
- 🤖 Leaning on **multi-agent AI workflows** (Claude Code: skills, hooks, subagents) to move fast without dropping the quality bar.

## ✨ Selected highlights

- 🌐 Shipped Komodo's public web estate across **5+ launches and rebrands**: **10+ properties, 120k+ monthly visits, 1M+ monthly Google Search impressions**.
- 🛡️ Led the user-facing response to the **2019 Agama supply-chain attack** and coordinated fund recovery for **thousands of users** after a **~$13M** white-hat sweep.
- 📈 Built a DeFi markets dashboard charting **1000+ trading pairs**; also a docs platform with MDX source and a Next.js build-and-deploy system that lints all the docs, adds attribution based on git commit history, and more.
- 🔗 Ran a **multi-region dPoW notary-node stack** helping protect **15+ Smart Chains** against 51% attacks.

## 🧩 More from Komodo (2018-2025)

Across those five roles I also:

- 🛂 wrote a geographic-compliance Cloudflare Worker (TypeScript/Hono) screening **2M+ requests/month** against a **34-jurisdiction** policy, with fail-closed defaults;
- 💬 built the in-app feedback Worker (parallel Trello/Matrix/Backblaze fan-out) that cut response times by **more than 50%**;
- 🔄 was users' go-to when a cross-chain atomic swap stalled: diagnosed the failure, recovered stuck funds, and wrote the guides that prevented the next one;
- 🗳️ won **5+ community elections** to keep operating that dPoW stack, a consensus-critical seat, and built the on-chain governance and vote-tally dashboards the elections used;
- 🧑‍🏫 taught junior engineers blockchain fundamentals throughout the KDF WASM Playground build;
- 🧰 sole-authored the [KDF WASM RPC bridge](https://github.com/GLEECBTC/komodo-defi-wasm-rpc) (Node.js/Puppeteer) so browser-only builds run under existing JSON-RPC tooling like a native daemon, and wrote **7 technical articles** on the [official blog](https://komodoplatform.com/en/blog/author/gcharang/).

## 🛠️ Tech I reach for

**Languages**
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Dart](https://img.shields.io/badge/Dart-0175C2?style=flat-square&logo=dart&logoColor=white)
![Bash](https://img.shields.io/badge/Bash-4EAA25?style=flat-square&logo=gnubash&logoColor=white)

**Frontend**
![React](https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white)
![Astro](https://img.shields.io/badge/Astro-BC52EE?style=flat-square&logo=astro&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=flat-square&logo=vite&logoColor=white)
![WebAssembly](https://img.shields.io/badge/WebAssembly-654FF0?style=flat-square&logo=webassembly&logoColor=white)

**Backend &amp; Data**
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)

**Infra &amp; Cloud**
![Cloudflare](https://img.shields.io/badge/Cloudflare-F38020?style=flat-square&logo=cloudflare&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Nginx](https://img.shields.io/badge/Nginx-009639?style=flat-square&logo=nginx&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonwebservices&logoColor=white)
![GCP](https://img.shields.io/badge/GCP-4285F4?style=flat-square&logo=googlecloud&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)

**AI &amp; Automation**
![Claude Code](https://img.shields.io/badge/Claude%20Code-D97757?style=flat-square&logo=anthropic&logoColor=white)
![Mastra](https://img.shields.io/badge/Mastra-1B1B1F?style=flat-square&logoColor=white)
![LangGraph](https://img.shields.io/badge/LangGraph-1C3C3C?style=flat-square&logo=langchain&logoColor=white)
![Hybrid RAG](https://img.shields.io/badge/Hybrid%20RAG-1C3C3C?style=flat-square&logoColor=white)
![Workers AI](https://img.shields.io/badge/Workers%20AI-F38020?style=flat-square&logo=cloudflare&logoColor=white)
![Vectorize](https://img.shields.io/badge/Vectorize-F38020?style=flat-square&logo=cloudflare&logoColor=white)

## 📌 Featured projects

| Project | What it is | Stack |
|---|---|---|
| **[anchorage](https://github.com/ProofOfTechOrg/anchorage)** · [live ↗](https://anchorage.proofoftech.org) · [API docs ↗](https://proofoftechorg.github.io/anchorage/) | The guardrails an agent runs behind: connector permission manifests, a React approval dashboard, an in-browser control room replaying attack scenarios against the real evaluators, an audit stream exported to a SIEM | TypeScript · Mastra · Durable Objects |
| **[understudy](https://github.com/ProofOfTechOrg/understudy)** · [npm ↗](https://www.npmjs.com/package/@understudy/protocol) | Executes what an agent decides: an encrypted credential vault, a dry run that never dispatches the real write, refs that fail closed against a replaced tab, per-tenant isolation where a cross-tenant request returns 404 | TypeScript · MV3 · CDP |
| **[vectorless-rag](https://github.com/ProofOfTechOrg/vectorless-rag)** | The parts that keep a research app honest: model-written SQL validated before it reaches Postgres, content-addressed artifacts with audited activation, a worst-case cost reserved before any paid model call | Python · FastAPI · LangGraph |
| **[react-komodefi-wasm](https://github.com/gcharang/react-komodefi-wasm)** · [live ↗](https://kdf-wasm.lordofthechains.com) | Zero-install sandbox for the Komodo DeFi RPC API: hot-swappable engine versions, request save/load, log download, seed-phrase import | TypeScript · Next.js · WASM |
| **[claude-config](https://github.com/gcharang/claude-config)** | Plan-then-execute, multi-agent Claude Code workflow: deterministic scaffolding + quality-gate loops so smaller models ship large features | Python · Claude Code |
| **[create-smartchain](https://github.com/gcharang/create-smartchain)** | One-command Komodo Smart Chain test networks: auto-generated configs, idempotent lifecycle | Shell |
| **[komodo-install-explorer](https://github.com/gcharang/komodo-install-explorer)** | Automated Komodo Smart Chain block-explorer install | Shell |
| **[komodo-docs-mdx](https://github.com/GLEECBTC/komodo-docs-mdx)** | MDX→Next.js docs platform powering [komodoplatform.com/en/docs](https://komodoplatform.com/en/docs): custom remark/rehype, generated API samples, in-browser fuzzy search | TypeScript · MDX |
| **[node-komodo-rpc](https://github.com/gcharang/node-komodo-rpc)** · [npm ↗](https://www.npmjs.com/package/node-komodo-rpc) | Promise-based, multi-instance Komodo daemon RPC client | JavaScript |

## 🌍 Open source

**Published by me on npm:**
[@proofoftech/breakwater](https://www.npmjs.com/package/@proofoftech/breakwater) ·
[@proofoftech/flowsafe](https://www.npmjs.com/package/@proofoftech/flowsafe) ·
[@proofoftech/fleet-control](https://www.npmjs.com/package/@proofoftech/fleet-control) ·
[@understudy/protocol](https://www.npmjs.com/package/@understudy/protocol) ·
[@understudy/connector](https://www.npmjs.com/package/@understudy/connector) ·
[node-komodo-rpc](https://www.npmjs.com/package/node-komodo-rpc)

**Komodo ecosystem** (KomodoPlatform / GLEECBTC), merged contributions:
[komodo-defi-framework](https://github.com/GLEECBTC/komodo-defi-framework) ·
[dPoW](https://github.com/KomodoPlatform/dPoW) ·
[NotaryNodes](https://github.com/KomodoPlatform/NotaryNodes) ·
[coins](https://github.com/GLEECBTC/coins) ·
[komodo-docs-mdx](https://github.com/GLEECBTC/komodo-docs-mdx) ·
[hw-kmd-wallet](https://github.com/GLEECBTC/hw-kmd-wallet)

**Beyond Komodo**:
[TokelPlatform/documentation](https://github.com/TokelPlatform/documentation)

## 📫 Connect

<p align="left">
  <a href="https://linkedin.com/in/gcharang"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
  <a href="mailto:mrgcharang@gmail.com"><img src="https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" /></a>
</p>
