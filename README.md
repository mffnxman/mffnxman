# Rafael Garcia

I run facilities operations by day and build local-first AI infrastructure the rest of the time. Everything here runs on one consumer laptop (8 GB VRAM, 32 GB RAM) and is written to survive that constraint: measured resource promises, governors, regression suites, and memory that persists across sessions.

## Projects

| Repo | What it is | Stack |
|---|---|---|
| [dart2](https://github.com/mffnxman/dart2) | d'Artagnan 2.0: a locked local-LLM daemon with thin clients, tier routing (daily / deep / failover) with measured VRAM and RAM promises, a resource governor with co-tenant eviction, and a RAM cockpit GUI. | Python, llama.cpp, FastAPI, pywebview |
| [memory-spine](https://github.com/mffnxman/memory-spine) | A file-based long-term memory engine for Claude Code. Hooks for boot, prefetch, and session end; hybrid TF-IDF + vector + rerank retrieval; knowledge graph with personalized PageRank; bitemporal facts; a consolidation sleep cycle; continuity regression tests. | Python, SQLite, fastembed |
| [dartagnan](https://github.com/mffnxman/dartagnan) | d'Artagnan v1: a local agent built as a substrate for studying small-model confabulation. Five layered interventions and an adversarial regression methodology. Superseded by dart2, kept as the research artifact. | Python, Ollama, Qwen3 |
| [duck-pet-claude](https://github.com/mffnxman/duck-pet-claude) | A pixel-art desktop duck with a built-in Claude Code terminal, plus Duck Sentinel: a local-first co-pilot loop where a free observation layer runs 24/7 and Claude only wakes up when something matters. | Python, tkinter, CDP |
| [injection-scan](https://github.com/mffnxman/injection-scan) | A prompt-injection scanner for agent tool output. Catches text that mimics system messages, overrides instructions, or hijacks the next action. Ships as a Claude Code skill and a standalone CLI. | Python |
| [mcp-erp-bridge](https://github.com/mffnxman/mcp-erp-bridge) | Reference implementation: wrap a cookie-authenticated internal web app as an MCP server so non-technical operators can drive it from Claude. Deterministic core, probabilistic edge. | Python, FastMCP, httpx |

## How I work

- Build, measure, then keep the number. Every tier in dart2 has a benchmarked promise and a regression that fails when it drifts.
- Local first. If it can run on the laptop without a cloud round-trip, it does.
- Memory is infrastructure. The memory engine is what lets an assistant pick up where the last session left off instead of starting cold.
- Tests before claims. Each repo carries its own suite; the READMEs only quote numbers that exist in the tree.

## Currently

Shipping the sanitized public versions of the tools above and looking for forward-deployed and applied-AI engineering work where this kind of hands-on systems building is the job.
