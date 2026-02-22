# Changelog

All notable changes to this project are documented here. Format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).

---

## [4.1.1] — 2026-02-22

### Fixed
- Redesigned UI from generic purple-gradient/Inter aesthetic to a distinctive dark editorial theme (Syne + Outfit fonts, amber accent palette)
- Corrected prompt count badge in README from 183 → 198 to match actual data
- Aligned category breakdown table counts in README with real prompt data
- Fixed `animationDelay` overflow (was up to 9.1 s for 183 items; now capped at 0.4 s)
- Added `type="button"` to all `<button>` elements to prevent accidental form submission
- Added `aria-label`, `aria-pressed`, and `aria-expanded` to all interactive controls
- Added visually-hidden `<label>` for the search `<input>` (screen-reader accessibility)
- Fixed `role="status"` and `aria-live="polite"` on toast notification
- Added `<nav>` with `aria-label` around category filter group
- Corrected `stats` useMemo dependency array to include `categories`
- `useEffect` now resets `expandedId` when `search` or `filter` changes (prevents stale expanded state)
- "Reset Filters" button now also clears `expandedId`
- `copyToClipboard` textarea fallback for browsers without `navigator.clipboard`
- `categories` array is now memoized once with `useMemo([], [])` instead of being recomputed on every render
- Fixed missing `<link rel="icon">` tags in `<head>`
- Updated example contribution ID in README from 126 (taken) to 199 (next available)
- Updated favicon.svg from generic blue "A" circle to a distinctive robot/AI icon
- Created this CHANGELOG.md
- Created favicon.png generation reference

### Added
- CSS custom property system (`--color-*`) for consistent theming
- Dot-grid background texture for visual depth
- Amber left-border card hover effect
- Smooth `cubic-bezier` transitions on all interactive elements
- `<article>` semantic element per prompt card

---

## [4.1.0] — 2026-02-24

### Added
- 15 new Gemini 3.1 Pro prompts showcasing advanced reasoning and "Vibe Coding"
- New SVG Animation Series: Pelican, Frog, Giraffe, Ostrich, Turtle, and Dachshund (IDs 184–189)
- Wuthering Heights Portfolio design prompt (ID 190)
- Starling Murmuration 3D simulation (ID 191)
- Hand-Tracking Interaction prompt (ID 192)
- Generative Soundscapes Audio prompt (ID 193)
- ISS Aerospace Dashboard prompt (ID 194)
- Edit-then-Test Agent prompt (ID 195)
- Extended Output Refactor Agent prompt (ID 196)
- ARC-AGI-2 Logic Grid solver (ID 197)
- GPQA Diamond Solver (ID 198)

### Changed
- Total prompt count: 183 → 198
- Version bump: 4.0.0 → 4.1.0

---

## [4.0.0] — 2026-02-22

### Added
- 58 new prompts across 5 new categories and 3 expanded existing ones
- New categories: Writing & Content (10), Education & Learning (8), Audio & Music (7), Data Analysis (9), Personal Productivity (7)
- Expanded categories: Video Generation (1 → 10), Coding (+5), Career (+5)
- Video Generation prompts: First-Person FPV Drone, Temporal Hyperlapse, Macro Liquid Fusion, Character Emote, Product Reveal: Shadow Play, B-Roll: Handheld Gritty, Isometric 3D Animation, Nature: Atmospheric Mist, Sci-Fi: Warp Speed (IDs 165–173)
- Writing & Content prompts (IDs 126–135)
- Education & Learning prompts (IDs 136–143)
- Audio & Music prompts (IDs 144–149)
- Data Analysis prompts (IDs 150–157)
- Personal Productivity prompts (IDs 158–164)
- Additional Coding prompts: Tailwind Component Architect, TypeScript Type Guard Generator, GitHub Action CI/CD Pipeline, Python Web Scraper, Legacy Code Refactorer (IDs 174–178)
- Additional Career prompts: Job Description Optimizer, LinkedIn Thought Leader, Interview Simulation: FAANG, The 'Brag Document' Builder, Freelance Proposal Closer (IDs 179–183)

### Changed
- Total prompt count: 125 → 183
- Category count: 10 → 15

---

## [3.3.0] — 2026-01-15

### Added
- Gemini 3.5 Flash Deep Agent Mode with Think-Act-Observe loops (ID 116–117)
- Google AI Products prompts: NotebookLM, AI Studio, AI Mode Shopping (IDs 118–122)
- Agentic Vision with active image investigation and Python code generation (ID 117)
- Deep Think Mode with modulated reasoning Fast/Thinking/Pro (ID 116)
- Full-Stack Generator (Snowbunny) for one-shot website creation (ID 120)
- Multimodal Live API for real-time streaming agents (ID 123)
- NotebookLM MCP Integration prompt (ID 124)
- Total prompts: 125 across 10 categories

---

## [3.2.0] — 2025-12-01

### Added
- Advanced Agentic AI section with model-specific prompts (IDs 96–115)
- Multi-Agent Coordination System (ID 96)
- Context Engineering Blueprint (ID 97)
- Gemini 2.0 Deep Research Mode (ID 98)
- Agentic Code Reviewer Jules-Style (ID 99)
- Agent-to-Agent Protocol Designer (ID 100)
- Gemini Multimodal Chain-of-Thought (ID 101)
- Claude MCP Context Engineering (ID 102)
- Social Media Agent Platform-Adaptive (ID 103)
- Few-Shot Adaptive Agent (ID 104)
- Negative Prompt Engineering (ID 105)
- OpenAI Swarm Pattern: Handoffs (ID 106)
- Gemini Grounding with Web Search (ID 107)
- Anthropic Prompt Caching Strategy (ID 108)
- Vision Board + Goal Tracking 2026 (ID 109)
- LLM-as-Judge Self-Evaluation (ID 110)
- Conditional Tool Use Routing (ID 111)
- Gemini Long Context 1M Tokens (ID 112)
- Parallel Agent Execution (ID 113)
- Input/Output Guardrails Agent (ID 114)
- Gemini Spatial Reasoning Prompt (ID 115)

---

## [3.1.0] — 2025-10-15

### Added
- Agentic AI section with 15 autonomous workflow prompts (IDs 81–95)
- Multi-Step Research Agent, Code Review Agent, Customer Support Triage Agent
- Data Pipeline Orchestrator, Content Strategy Agent, Meeting Summarization Agent
- Competitive Intelligence Agent, Bug Reproduction Agent, Learning Path Designer
- API Integration Planner, Crisis Communication Agent, Security Audit Agent
- Sales Qualification Agent, Workflow Automation Designer, Prompt Chain Architect

---

## [3.0.0] — 2025-09-01

### Added
- Initial public release
- 80 prompts across 9 categories
- Categories: Infographics, Image Generation, Image Editing, Video Generation, Marketing, Career, Coding, Problem Solving, Design
- Web interface with search, filter, copy-to-clipboard
- React-based SPA with Tailwind CSS
- MIT License

---

*For a full diff of each version, see the [GitHub releases page](https://github.com/darshil0/ai-prompt-collection-2026/releases).*
