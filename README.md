# Portfolio — Russell Licht

**AI Systems Architect | Cross-Domain Engineering**

Architecture overviews and project statistics for technical review. No source code. All projects built January–March 2026 while working full-time as a salon manager and colorist.

Full project access available upon request — contact Dig.Russell.Licht@Gmail.com

---

## At a Glance

| Metric | Value |
|--------|-------|
| Total Python | 1,040,000+ lines across 7,600+ files |
| Scientific Computations | 442 with full audit trails |
| Integrated Data | 170 GB across 80+ observational and simulation datasets |
| Galaxies Analyzed | 4,142 cross-matched across 16 surveys |
| Papers Authored | 3 (1 in revision, 2 in preparation) |
| Patent | Provisional filed — spacecraft architecture, 20 claims |
| Repositories | 9 active (2 public, 7 private) |
| Audit Reports | 12 comprehensive audits, 213 audit files |
| Domains | Astrophysics, gravitational physics, quantitative finance, aerospace, developer tooling |
| Build Period | 90 days |

---

## Project Architectures

### 1. Astrophysics Research Program

**Scale**: 5 interconnected repositories, 370K+ lines of Python, 419 computations

**Architecture**:
```
shared_constants.py (single source of truth — read-only across all repos)
    |
    ├── Repository 1: Galaxy-Scale Analysis (main program)
    |   ├── analysis/pipeline/ — 9-stage data integration pipeline
    |   ├── analysis/tests/ — 50+ test scripts with kill/survive verdicts
    |   ├── raw_data/ — 80+ datasets (170 GB), quality-tiered (A/B/C/D)
    |   ├── meta/ — Data librarian index, galaxy cross-survey lookup (4,142 galaxies)
    |   ├── outputs/ — 277 numbered computation directories
    |   ├── paper/ — 3 manuscripts (LaTeX + figures + tables)
    |   └── audit/ — Contamination tracking, quarantine list
    |
    ├── Repository 2: Gravitational Physics (140K lines)
    |   ├── Numerical relativity solvers
    |   ├── Parameter space scans
    |   ├── Wave signature analysis
    |   └── 44 computation directories
    |
    ├── Repository 3: Cluster-Scale Extension (107K lines)
    |   ├── 32 independent analysis packages
    |   ├── Multi-wavelength data integration (X-ray, SZ, optical, simulation)
    |   └── 23+ synthesis outputs
    |
    ├── Repository 4: Cross-Scale Physics Catalog (103K lines)
    |   ├── 10 scale levels (10^-35 to 10^26 m)
    |   ├── 98 computation directories
    |   └── Systematic framework survey
    |
    └── Repository 5: Quality Assurance
        ├── 12 comprehensive audits
        ├── 213 audit files
        └── Math verification, contamination checks, constant validation
```

**Data Pipeline**:
```
16 Surveys → Cross-Match (4,142 galaxies) → Quality Tiering → Unified Pipeline
    → Per-Galaxy Fitting (ODR) → Multi-Scale Analysis → Kill/Survive Verdict
    → Contamination Audit → Paper
```

**Key Infrastructure Decisions**:
- Single constants file consumed read-only across 5 repos via symlinks — prevents parameter drift
- Every computation is a testable hypothesis with explicit pass/fail criteria
- Quarantine list for unvalidated parameters — flagged values cannot enter downstream analysis
- Data librarian index tracks citation, redistribution policy, and quality tier for every dataset

---

### 2. V3 Autonomous Investment System

**Scale**: 49 microservices, 567K lines of Python, 535+ unit tests

**Architecture**:
```
Layer 1: Data Scouts (15 agents)
    ├── Equities: Alpaca (real-time quotes + trades)
    ├── Crypto: Coinbase WebSocket (L2 order book)
    ├── Market Data: Polygon, Alpha Vantage
    ├── DeFi: DeFi Llama
    ├── Macro: FRED, BIS, BLS
    ├── Positioning: CFTC, FINRA
    ├── Government: US Treasury, SEC EDGAR
    └── All agents → Kafka/Redpanda (42+ topics)

Layer 2: Feature Engines (11 engines)
    ├── Macro: Liquidity, USD strength, commodities, industrial cycle
    ├── Microstructure: Dealer gamma, dark pool activity
    └── Crypto/DeFi: Dominance, mempool, stablecoin flow, liquidations, DEX liquidity

Layer 3: Synthesis
    ├── Kalman Filter fusion
    ├── Hidden Markov Models
    ├── Bayesian networks
    └── Conviction scoring → 6 strategy modules

Layer 4: Execution
    ├── Position sizing
    ├── Risk management
    └── Order routing (Alpaca Markets API)

Layer 5: CIO Command Center
    └── Flask + PostgreSQL human oversight dashboard

Infrastructure:
    ├── Kafka/Redpanda (42+ topics, multi-agent event streaming)
    ├── PostgreSQL 16 (persistent storage)
    ├── Kubernetes on GKE (container orchestration)
    ├── Argo Workflows (job scheduling)
    ├── Prometheus + Grafana (monitoring)
    ├── GitHub Actions (CI/CD)
    └── Docker (containerization)
```

**Backtest Engine**:
```
Docker Image (GCP Artifact Registry)
    → K8s Job (argo namespace)
    → Two-Pass Architecture:
        Pass 1: Daily bars (spot + optional perps)
        Pass 2: 4H bars (intraday perps)
    → Reflexive Strategy Router:
        5 strategies × per-strategy exit profiles
        50-trade rolling feedback loop (λ=0.95)
    → PostgreSQL results
```

---

### 3. POPPINS — Spacecraft Architecture

**Provisional Patent POPPINS-PROV-001 | 20 Claims | Filed February 2026**

**System Overview**:
```
Autorotative Descent (80-98% propellant reduction)
    ├── Deployable structural petals (5 functions per petal)
    ├── Centrifugal self-regulating louver system
    └── Morphic hull with pressure-driven reconfiguration

Dual-Mode MHD Bore
    ├── Entry: Atmospheric plasma → 1-3 MW electrical power
    └── Orbit: Magnetoplasmadynamic thruster (2,000-5,000s Isp)

Cascading Degradation (7 levels)
    Level 1: Full neuromorphic + electronic servo
    Level 2: Hydraulic + mechanical cam followers
    Level 3: Passive hydraulic (atmospheric pressure)
    Level 4: Mechanical gear + spring assist
    Level 5-7: Progressive arm fracture → gravity-stable equilibrium

Zero Single-Use Hardware
    Every component serves 2+ functions across mission phases
```

---

### 4. Claude Sidecar — Developer Tooling

**Scale**: 55 TypeScript source files, Electron desktop app

**Architecture**:
```
Electron Shell
    ├── PTY Manager (node-pty) — terminal session management
    ├── IPC Handlers — main ↔ renderer communication
    └── Session Store — multi-session state

React 18 Frontend (Vite)
    ├── FileTree — live-animated, color-coded by operation type
    ├── ActivityView — real-time operation stream
    ├── TerminalTabBar — multi-session tabs
    ├── SessionSidebar — session management
    └── Intelligence Layer:
        ├── Deep Parser — AST-level code understanding
        ├── Sequence Detector — pattern recognition
        ├── Knowledge Dictionary — domain context
        └── Teaching Assistant — contextual help

Express + WebSocket Server
    ├── File Watcher (chokidar) — filesystem events
    └── Claude Code Hooks integration — real-time event streaming
```

---

### 5. Agentic Evaluation Framework (Public)

**Repository**: [github.com/rlicht-digc/agentic-evaluation-framework](https://github.com/rlicht-digc/agentic-evaluation-framework)

4 evaluation skills preventing failure modes in extended AI reasoning sessions:
- Evidence-grade inflation detection
- Stale-value propagation tracking
- Confirmation bias interruption
- Result classification with explicit verdicts

---

## Agent Infrastructure

**Multi-Agent Coordination**:
```
Human (Russell)
    ├── Claude Code Agent 1 (primary — hooks, skills, memory)
    ├── Claude Code Agent 2 (parallel tasks)
    ├── Codex Agent (independent cross-validation)
    └── Mailbox Protocol:
        ├── 40-character SHA tracking per message
        ├── Sequential .seq counter
        ├── Role-specific templates (imperative for Codex, XML for Claude)
        └── Repo state sync on every message
```

**Memory Architecture**:
```
MEMORY.md (index — loaded every session, <200 lines)
    ├── user/ — role, preferences, expertise
    ├── feedback/ — corrections + confirmed approaches
    ├── project/ — ongoing work, decisions, deadlines
    └── reference/ — external system pointers

50+ topic files across 5 research domains
Cross-session coherence with staleness detection
```

**Quality Assurance Pipeline**:
```
Computation Prompt → Prompt Hardening Skill (red-team)
    → Agent Execution → Result Classification Skill
    → Kill/Survive Verdict → Contamination Audit
    → Quarantine Check → Downstream Use Approved
```

---

## Technical Environment

Python | TypeScript | SQL | LaTeX | NumPy | SciPy | Astropy | Pandas | Matplotlib | Docker | Kubernetes/GKE | Kafka/Redpanda | PostgreSQL | React 18 | Electron | Node.js | Express | WebSocket | Prometheus | Grafana | GitHub Actions | Argo Workflows | Claude Code | Claude API | Codex

---

*Built by a hairdresser with a high school diploma, working full-time behind the chair. This is what AI-augmented engineering makes possible.*
