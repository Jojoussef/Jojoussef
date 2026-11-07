# Youssef Benatti

```
Coordinates: 35.76°N, 10.82°E (Monastir, Tunisia)
Role: Systems, Applied AI, and Security Engineer
Portfolio: https://youssef-benatti.me
Email: contact@youssef-benatti.me
GitHub: @Jojoussef
```

I build systems that handle strict data integrity requirements, high-throughput retrieval pipelines, and distributed web applications. My background spans cryptographic audit trails, AI evaluation frameworks, network security assessments, and production SaaS architecture.

---

## ⚡ Verified Open-Source Engineering

Recent patches submitted to core open-source repositories:

| Ecosystem | PR / Subsystem | Technical Description | Impact & Test Scope |
|---|---|---|---|
| **UK Government BEIS** | [`inspect_ai#6078`](https://github.com/UKGovernmentBEIS/inspect_ai/pull/6078) `Merged` | Fixed reader selection in `precomputed_scores()` on HTTP(S) presigned URLs with query parameters. Scoped `urlparse(url).path` to prevent `.json` fallback errors on `.jsonl` files. | 2 unit test suites added. 776 scorer tests passed cleanly. |
| **UK Government BEIS** | [`inspect_ai#5987`](https://github.com/UKGovernmentBEIS/inspect_ai/pull/5987) `Open` | Prevented empty model completions from receiving false `CORRECT` scores in `model_graded_qa` and `choice` scorers. Added `reason="no_response"` tracking. | 125 scorer tests verified. Preserved zero-choice evaluation invariants. |
| **ZizkaDB** | [`ZizkaDB#231`](https://github.com/ZIZKA-AI-SL/ZizkaDB/pull/231) `Landed in #261` | Sealed tamper-evident audit gaps for EU AI Act Article 12 compliance. Extended SHA-256 event preimage across `tenant_id`, `agent_id`, `parent_event_id`, and DB sequence numbers in transactional `INSERT ... RETURNING`. | Added `GET /v1/events/verify`. 16 unit tests covering JSONB round-trip stability and field tamper detection. |
| **Dex Identity Provider** | [`dex#5100`](https://github.com/dexidp/dex/pull/5100) `Open` | Replaced HTTP 500 crashes with typed `UserNotInRequiredGroupsError` returning HTTP 403 Forbidden in `connector/github/github.go`. | 3 unit tests added. Signed off with DCO per CNCF criteria. |
| **HoloViz Panel** | [`panel#8974`](https://github.com/holoviz/panel/pull/8974) `Merged` | Fixed widget state collisions during HTML export in `panel/io/embed.py`. Required widget type and candidate value equality before merging duplicate keys. | 24 tests passed cleanly in `panel/tests/io/test_embed.py`. |
| **HoloViz Panel** | [`panel#9028`](https://github.com/holoviz/panel/pull/9028) `Open` | Fixed inverted batch-update condition in `ReactiveESM._update_model`, enabling bidirectional `jslink` preprocessing on dynamically appended children. | Added Bokeh `CustomJS` callback verification test in `test_custom.py`. |
| **IBM Docling** | [`docling#4993`](https://github.com/docling-project/docling/pull/4993) `Closed` | Preserved nested list structures across empty paragraph nodes in `MsWordDocumentBackend` by snapshotting list hierarchy state. | Markdown export verified with 4-space indent retention. |
| **Raspberry Pi Foundation** | [`blockly#10602`](https://github.com/RaspberryPiFoundation/blockly/pull/10602) `Closed` | Routed variable declaration extraction through `getVariableName()` across JavaScript and Dart generators. | 25 mocha generator tests passed. |

---

## 🛰️ Flagship Production Systems

### 1. [eSIM Price Truth & Spot FX Arbitrage Engine](https://youssef-benatti.me/esim-arbitrage-calculator/)
A production data analysis engine and buying tool covering 94 global travel destinations, 20 fiat currencies, and 136,000+ catalog prices.
- **Core Architecture:** Custom Node static generator with zero npm runtime dependencies. Transforms raw catalog snapshots into programmatic destination pages and interactive calculators.
- **Arbitrage Detection:** Evaluates live European Central Bank exchange rates against vendor-locked pricing tables, identifying 224 currency inversion opportunities for international travelers.
- **Subscription Infrastructure:** Server-side entitlement gate running on Appwrite Functions and Cloudflare Workers. Verifies JWT sessions and validates Stripe webhooks under cryptographic signature checks.

### 2. [AutoGEO Audit & Retrieval Platform](https://github.com/Jojoussef/autogeo-audit-engine)
An automated B2B audit engine that scores company retrievability across generative search systems (Perplexity, SearchGPT, Gemini).
- **Pipeline:** Monorepo orchestrating automated domain crawling, structured data extraction, and semantic citation scoring.
- **Video Diagnostics:** Renders automated 1080p diagnostic video reports using Remotion, Node, and headless Chromium workers.
- **Deployment:** Multi-container production stack managed with Docker Compose, Caddy reverse proxy, and Appwrite backend integrations.

### 3. [Conceptionist Spacetime Observatory](https://youssef-benatti.me)
My personal interactive spatial engineering portfolio.
- **Physics & Optics:** Three.js celestial constellation featuring an active full-screen optical glass lens with 13 stage-specific diopter magnification steps and chromatic dispersion passes.
- **Procedural Audio:** Web Audio API sound engine synthesizing 432 Hz Pythagorean pentatonic harmonics and continuous velocity-modulated drone oscillations directly in code.
- **Interactive Telemetry:** In-browser SHA-256 Merkle audit verification console and live currency conversion test beds.

---

## 📦 Production Applications

### [Seha](https://github.com/Jojoussef/it-impact-app)
AI-assisted healthcare platform designed to process and track CNAM health insurance claims in Tunisia.
- Built with Next.js 15, TypeScript, NextAuth, and shadcn/ui.
- Automates medical paperwork intake through optical character extraction and structured classification pipelines.
- Implements role-based access control for patients and medical providers with complete tracking histories.

### [YuccaInfo GED](https://github.com/Jojoussef/yuccainfo_ged_backend)
Document management and electronic archiving system for enterprise workflows.
- **Backend:** Django REST Framework, PostgreSQL, and asynchronous OCR pipelines running Tesseract and Hugging Face transformer models.
- **Frontend:** Next.js and TypeScript interface providing virtualized document browsing, metadata tagging, and sub-second full-text search.
- **Repositories:** [Backend API](https://github.com/Jojoussef/yuccainfo_ged_backend) · [Frontend UI](https://github.com/Jojoussef/yuccainfo_ged_frontend)

---

## 🛠️ Technical Matrix

```
Languages:            Python, TypeScript, JavaScript, Go, SQL, HTML5, CSS3
Frameworks & Libs:    Next.js 15, React, Django REST, FastAPI, Express, Three.js, Tailwind CSS
Databases & Storage:  PostgreSQL, SQLite, Redis, Cloudflare D1 / KV, Appwrite
Applied AI & Tools:   Inspect AI, PyTorch, Hugging Face, Tesseract OCR, Pydantic V2, Docker
Security & Network:   Burp Suite, Wireshark, OAuth2 / OIDC, JWT / HMAC, Linux (Debian, macOS)
Testing & Quality:    Pytest, Mocha, Ruff, Pre-commit, GitHub Actions CI/CD
```

---

## 📊 Live Activity

<div align="center">
  <img height="150" src="https://github-readme-stats.vercel.app/api?username=Jojoussef&show_icons=true&hide_border=true&theme=tokyonight&rank_icon=github" alt="GitHub Stats" />
  <img height="150" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Jojoussef&layout=compact&hide_border=true&theme=tokyonight" alt="Top Languages" />
</div>

---

<div align="center">
  <sub>Open to systems engineering, applied AI, and security roles. Reach out via email or connect on GitHub.</sub>
</div>
