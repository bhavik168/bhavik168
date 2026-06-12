<div align="center">

<img src="./name-header.svg" alt="Bhavik Mehta" width="100%" />

### Full Stack Developer · AI Systems · Seattle, WA

[![Portfolio](https://img.shields.io/badge/bhavikmehta.dev-000000?style=flat-square&logo=vercel&logoColor=white)](https://bhavikmehta.dev?utm_source=github_readme)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://linkedin.com/in/bhavikmehta1101)
[![Email](https://img.shields.io/badge/mehtabhavik168@gmail.com-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:mehtabhavik168@gmail.com)
[![Resume](https://img.shields.io/badge/Resume-PDF-5DD62C?style=flat-square&logo=adobeacrobatreader&logoColor=white)](https://github.com/bhavik168/bhavik168/raw/main/Bhavik_Mehta_Resume_2026.pdf)
[![Open to Work](https://img.shields.io/badge/●_Open_to_Work-5DD62C?style=flat-square&logoColor=white)](#)

</div>

---

## About

MS CS @ Seattle University. Two years at Amdocs debugging distributed backend systems before deciding I'd rather be building them from scratch.

Since then: shipped [Habiwine](https://www.habiwine.com) solo to production, built [peekwise.ai](https://peekwise.ai) — a competitive intelligence SaaS that processes 2,000+ reviews a night at near-zero API cost — and won **1st place at AWSHacks 2026** with [ARIA](https://github.com/bhavik168/ARIA), a six-agent Amazon Bedrock system that gives 911 dispatchers real-time decision support in under 15 seconds. Also merged a fix into [Bruno](https://github.com/usebruno/bruno/pull/8245) (22k+ ⭐) that resolved two long-standing issues in one line.

I care about the gap between code that runs and code that ships. Looking for full-stack or backend roles where that distinction actually matters.

---

## Stack

### Frontend
<p>
  <img src="https://skillicons.dev/icons?i=react,nextjs,ts,tailwind,html,css,js" />
</p>

### Backend & APIs
<p>
  <img src="https://skillicons.dev/icons?i=nodejs,express,python,fastapi,flask,graphql" />
</p>

### AI / ML
<p>
  <img src="https://skillicons.dev/icons?i=tensorflow,pytorch,opencv" />
  &nbsp;<img src="https://img.shields.io/badge/OpenAI_API-412991?style=flat-square&logo=openai&logoColor=white" />
  &nbsp;<img src="https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square&logo=langchain&logoColor=white" />
  &nbsp;<img src="https://img.shields.io/badge/HuggingFace-FFD21E?style=flat-square&logo=huggingface&logoColor=black" />
</p>

### Infrastructure & DevOps
<p>
  <img src="https://skillicons.dev/icons?i=aws,azure,gcp,docker,kubernetes,vercel,jenkins,github" />
</p>

### Databases
<p>
  <img src="https://skillicons.dev/icons?i=postgresql,mongodb,mysql,redis,supabase" />
  &nbsp;<img src="https://img.shields.io/badge/Snowflake-29B5E8?style=flat-square&logo=snowflake&logoColor=white" />
  &nbsp;<img src="https://img.shields.io/badge/Kafka-231F20?style=flat-square&logo=apachekafka&logoColor=white" />
</p>

### Languages
<p>
  <img src="https://skillicons.dev/icons?i=py,java,cpp,rust,go,solidity" />
</p>

---

## Selected Work

### [ARIA](https://github.com/bhavik168/ARIA) — Autonomous Response Intelligent Assistant · 🏆 1st Place AWSHacks 2026
`Amazon Bedrock` `Claude Haiku 3.5` `Claude Sonnet 4` `AWS Lambda` `Amazon Transcribe` `DynamoDB` `Titan Embeddings v2`

- Won 1st place at AWSHacks 2026 Bedrock Track — built a real-time 911 dispatch co-pilot that surfaces one actionable recommendation in under 15 seconds via a six-agent Amazon Bedrock pipeline, giving solo dispatchers a thinking partner during live calls
- Structured the reasoning layer so Claude Haiku 3.5 resolves location ambiguity mid-stream while Claude Sonnet 4 reconciles all specialist outputs into a single progressive recommendation card, keeping dispatchers focused on judgment instead of switching between tools
- Built an AWS Lambda stream processor with provisioned concurrency that fires Navigation, Medical, and Hazmat agents the moment Amazon Transcribe detects domain keywords, cutting coordination overhead that splits dispatcher attention mid-call
- Grounded every agent output in FEMA, AHA, and MPDS protocols via Amazon Bedrock Knowledge Base with Titan Embeddings v2; Bedrock Guardrails block unverified recommendations and log every override to DynamoDB

---

### [peekwise.ai](https://peekwise.ai) — Competitive Intelligence SaaS
`Next.js 14` `FastAPI` `Railway` `BullMQ` `Redis` `Neon PostgreSQL` `Groq` `Apify` `BrightData`

- Built a competitive intelligence SaaS as a monorepo with BullMQ as the sole async handoff between ingestion, AI enrichment, and orchestration layers — each cron service can scale or fail independently, cutting inter-service coupling to zero
- Sequenced Groq free-tier LLMs for nightly batch review analysis and a frontier model for one briefing call per competitor, sizing batches and sleep intervals around free-tier TPM limits to process ~2,075 reviews per day at zero API cost
- Separated hot analysis state in Redis hashes/sorted sets with 6-month TTLs from static config in Neon PostgreSQL, removing real-time AI calls from the request path and keeping every dashboard read sub-millisecond regardless of competitor count
- Built a 3-layer deduplication and freshness-cutoff pipeline over Google and Yelp review data via Apify and BrightData, cutting redundant API calls across nightly runs and keeping ingestion costs near zero at scale

---

### [bhavikmehta.dev](https://bhavikmehta.dev?utm_source=github_readme) — Personal Portfolio v2
`Next.js 16` `React 19` `TypeScript` `Tailwind CSS v4` `Framer Motion` `GSAP` `PostHog` `Vercel`

- **I designed it, Claude Code built it** — every architectural call was mine: App Router structure, per-section color system, component hierarchy, animation strategy. Claude Code handled implementation via a custom multi-agent setup (separate agents for animations, UI, blog, SEO, performance), each scoped to skill files I wrote to encode my own design rules
- **Neo-brutalist design system, designed from scratch** — I made the call to ditch component libraries entirely: sharp geometric edges, fixed per-section palettes, Syne/Space Grotesk/DM Sans type hierarchy, GSAP ScrollTrigger synced with Lenis smooth scroll. Every visual decision was deliberate, every pixel was intentional
- **PostHog wired in as a real analytics layer** — not just page views. I instrumented scroll depth, section engagement, and click patterns to understand which parts of the site actually hold attention. Same setup I'd use in a production SaaS — because treating your portfolio like a toy shows
- **MDX blog pipeline that gets out of the way** — I wanted writing to feel like `git push`, not a CMS workflow. Posts live in `/content/blog/`, frontmatter handles metadata, Vercel CI deploys on push. gray-matter parses it, draft flags keep things clean, and the whole thing took under an hour to wire up

---

### [Habiwine](https://www.habiwine.com) — Habit Tracking SaaS with AI Coaching
`React` `Node.js (Express)` `PostgreSQL` `OpenAI API` `AWS LightSail` `Supabase` `Cloudflare CDN`

- Architected RESTful backend with modular service layers, cutting average API response latency by 25% through query optimization and structured middleware
- Integrated OpenAI API for natural language habit interaction — users describe goals in plain English, the AI structures them into trackable habits with personalized coaching nudges
- Engineered PostgreSQL schemas with indexed relational models and query tuning, reducing data retrieval time by 30% across transactional flows
- Deployed Cloudflare edge caching strategy that reduced repeat request load by 35% and improved global delivery latency for distributed users

---

### Fake News Detection — Deep Learning Classifier
`Python` `TensorFlow` `NumPy` `Scikit-learn`

- Designed end-to-end NLP pipeline: preprocessing, tokenization, model training, and evaluation across large-scale news datasets
- Hit 96.8% classification accuracy after systematic hyperparameter tuning and batching strategy improvements
- Built reproducible training scripts with automated evaluation metrics for consistent benchmarking across model iterations

---

### Securing IoT Communication via Ethereum Blockchain
`Solidity` `Python` `C++` `MongoDB` `AWS` `Azure`

- Developed smart contract architecture with on-chain access control, reducing unauthorized interaction attempts by 40% in simulated attack scenarios
- Built Python and C++ interaction layers handling cryptographic signing, serialization, and runtime execution across distributed nodes
- Deployed blockchain services on AWS and Azure with MongoDB for decentralized storage and optimized retrieval

---

### Road Safety Prediction — ML + Real-Time Data Pipeline
`Python` `Scikit-learn` `MySQL` `Kafka`

- Built predictive ML models for accident risk scoring, improving assessment accuracy by 25% over baseline
- Integrated Kafka for real-time data ingestion and processing across the pipeline
- Reduced false positives by 20% through iterative model tuning and caching-optimized MySQL queries

---

## Open Source Contributions

### [usebruno/bruno](https://github.com/usebruno/bruno) — API Client (22k+ ⭐)

**[fix: show unsaved changes prompt when closing tab with Cmd+W / Ctrl+W](https://github.com/usebruno/bruno/pull/8245)** · Merged

Resolved two open issues ([#8244](https://github.com/usebruno/bruno/issues/8244), [#3264](https://github.com/usebruno/bruno/issues/3264)) — pressing `Cmd+W` / `Ctrl+W` on a modified HTTP request tab closed it immediately without triggering the unsaved-changes prompt. The `closeTab` handler's dirty-state check was missing the `'http-request'` type; adding it gave HTTP tabs the same protection all other request types already had.

---

## GitHub Stats

<div align="center">

<img height="160" src="https://github-readme-stats.vercel.app/api?username=bhavik168&show_icons=true&theme=github_dark&hide_border=true&bg_color=0d1117&title_color=5DD62C&icon_color=5DD62C&text_color=c9d1d9&rank_icon=github" />
&nbsp;
<img height="160" src="https://github-readme-stats.vercel.app/api/top-langs/?username=bhavik168&layout=compact&theme=github_dark&hide_border=true&bg_color=0d1117&title_color=5DD62C&text_color=c9d1d9&langs_count=8" />

</div>

<div align="center">

<img src="https://github-readme-streak-stats.herokuapp.com?user=bhavik168&theme=github-dark-blue&hide_border=true&background=0d1117&ring=5DD62C&fire=5DD62C&currStreakLabel=5DD62C" />

</div>

---

## Currently

- 📖 &nbsp; Deep in distributed systems and ML coursework at Seattle U
- 🔬 &nbsp; Exploring RAG architectures and agentic workflows
- 🛠️ &nbsp; Building v2 of my portfolio — neo-brutalist design, Next.js 16, heavy animations
- 👀 &nbsp; Open to internships, research roles, and interesting side projects

---

<div align="center">

*"Talk is cheap. Show me the code."* — Linus Torvalds

</div>
