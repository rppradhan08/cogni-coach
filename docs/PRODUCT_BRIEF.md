## Product Brief: CogniCoach MVP

### 1) Project overview / description
CogniCoach is an AI-powered assistant that helps job seekers improve their resumes for ATS compatibility and practice interviews through realistic, text-based sessions with actionable feedback. The MVP focuses on two core modules: a Resume Optimizer and a Text-Based Mock Interviewer, prioritizing fast time-to-value using established NLP/LLM capabilities.

### 2) Target audience
- Early-career candidates and recent graduates
- Career switchers and professionals re-entering the workforce
- Job seekers applying broadly who need faster iteration and higher interview conversion

### 3) Primary benefits / features
- Resume Optimizer
  - Upload or paste resume text; input target job description
  - ATS readability checks (layout, fonts, parse-ability, consistency)
  - Keyword matching with relevance score and missing keyword suggestions
  - Clarity and impact improvements (e.g., stronger verbs, scannable bullets)
  - Basic grammar/typo corrections
  - Actionable report and option to download an ATS-optimized version
- Text-Based Mock Interviewer
  - Select scenarios (behavioral/technical) or tailor via job description
  - Q&A interface with immediate, structured feedback after answers or session
  - Feedback dimensions: relevance, conciseness/clarity, tone, filler phrase detection, keyword integration
  - Automated session summary highlighting strengths and prioritized improvements
- Foundational
  - Clear AI usage disclosure and basic data privacy statement
  - Lightweight feedback mechanism for continuous improvement

### 4) High-level tech/architecture used
- Frontend: React + TypeScript (Vite), Tailwind CSS, shadcn/ui
- Auth: Clerk (session-based auth, protected routes)
- Backend/API: Node.js with Hono (REST endpoints for analysis and reports)
- Database: Supabase (Postgres) for user data, sessions, interview logs, reports
- Storage: Supabase storage (optional) for uploaded documents if needed
- AI/NLP: External LLM API for text analysis, keyword extraction, and feedback generation
- Payments (future-ready): Stripe integration for tiers/premium features
- Package manager/tooling: pnpm; environment variables via platform secrets

Architecture sketch (MVP):
- Client handles resume upload/text input and interview UI
- Backend exposes endpoints: resume analyze, interview session, feedback report
- Backend calls LLM API for analysis; persists artifacts in Postgres
- Auth guards read/write operations; rate limits to protect API budgets


