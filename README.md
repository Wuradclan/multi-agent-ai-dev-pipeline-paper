# Toward a Self-Healing Multi-Agent Software Engineering Pipeline

This repository contains the LaTeX source and compiled PDF for a position paper proposing a **6-stage multi-agent architecture** for AI-assisted software engineering.

The pipeline enforces **segregation of duties** across specialized agents:
1. **Architect (Plan)** – high-level task decomposition and JSON blueprints.
2. **Researcher (Verify)** – grounded external doc and API validation.
3. **Engineer (Build)** – repository-aware implementation (Claude Code).
4. **Validator (Test)** – isolated QA agent with deterministic tests.
5. **Memory Layer (Commit)** – long-term, structured project memory.
6. **Grounded Continuation (Loop)** – future planning grounded in verified state.

The paper:
- Identifies failure modes in **single-agent coding workflows** (context collapse, hallucinated APIs, broken loops).
- Defines the concept of **Memory Contamination** and explains why persistent context must be protected by a quality gate.
- Outlines an **evaluation roadmap** comparing this architecture against single-agent baselines (e.g., standard Claude Code) using metrics like test pass rates, contamination rate, context window efficiency, and P95 latency.

## Contents

- `self_healing_multi_agent_pipeline.tex` – LaTeX source of the paper.
- `Ai_architcture_loop.pdf` – compiled PDF.
- `architecture-loop.png` – system architecture diagram (6-stage loop).

## How to build

```bash
pdflatex self_healing_multi_agent_pipeline.tex
```

Make sure `architecture-loop.png` is in the same directory as the `.tex` file before compiling.

## License

This repository is licensed under the **MIT License**. You are free to read, share, and build upon this work, provided that attribution to the original author is preserved.
