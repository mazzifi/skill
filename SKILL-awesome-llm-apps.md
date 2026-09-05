---
name: awesome-llm-apps-index
description: Reference index over "Awesome LLM Apps" (awesome-llm-apps-main.zip) — a large collection of example AI-agent/LLM application projects organized by category (starter agents, advanced agents, always-on agents, multi-agent teams, voice agents, generative UI, game-playing agents, MCP agents, RAG tutorials, memory apps, chat-with-X, optimization, fine-tuning, framework crash courses). Use when the user wants example code/architecture patterns for building an AI agent app, is deciding what kind of agent to build, or wants a working reference implementation to adapt rather than build from scratch.
license: Repo-level license applies per project; check each subfolder before reusing code verbatim in a shipped product.
---

# Awesome LLM Apps — example project index

This is a curated collection of runnable example projects (mostly Python)
demonstrating LLM/agent patterns, not a single tool. Use it as **inspiration
and architecture reference** when the user is building something similar,
then adapt the pattern to their actual stack rather than copying files
wholesale.

## Category → directory map

| Category | Directory |
|---|---|
| 🌱 Starter AI Agents | `starter_ai_agents/` |
| 🚀 Advanced AI Agents | `advanced_ai_agents/` (includes autonomous game-playing agents) |
| 🛰️ Always-on Agents | `always_on_agents/` |
| 🤝 Multi-agent Teams | inside `advanced_ai_agents/` — look for "multi-agent" or "team" in project names |
| 🗣️ Voice AI Agents | `voice_ai_agents/` |
| 🖼️ Generative UI / Agentic Frontends | `generative_ui_agents/` |
| ♾️ MCP AI Agents | `mcp_ai_agents/` |
| 📀 RAG (Retrieval Augmented Generation) | `rag_tutorials/` |
| 💾 LLM Apps with Memory | look for "memory" in `advanced_llm_apps/` and `starter_ai_agents/` |
| 💬 Chat with X | look for "chat_with_" prefixed projects across the tree |
| 🎯 LLM Optimization Tools | `advanced_llm_apps/` |
| 🔧 LLM Fine-tuning | `advanced_llm_apps/` (fine-tuning subprojects) |
| 🧑‍🏫 Agent Framework Crash Courses | `ai_agent_framework_crash_course/` |
| 🧩 Agent Skills | `agent_skills/` |

Each project directory typically has its own `README.md` (setup/usage) and a
`requirements.txt`. There is no single entry point for the whole repo —
navigate to the specific project directory the user's use case matches.

## How to use this

1. Ask (or infer) what kind of app the user wants: a one-shot agent, a
   long-running/background agent, a multi-agent team, voice interface, a
   RAG/chat-with-docs tool, or a framework tutorial.
2. Find candidate project names in the matching category directory:
   ```bash
   unzip -l awesome-llm-apps-main.zip | grep "^.*rag_tutorials/[^/]*/$"
   ```
3. Pull the specific project's README and main script to see the actual
   pattern (framework used — often LangChain, CrewAI, LlamaIndex, OpenAI
   Agents SDK, or raw API calls — plus how it wires up tools/memory/RAG).
4. Explain the pattern and adapt it to the user's requirements, model
   choice, and constraints — don't assume their target model/provider
   matches what the example hardcodes.
5. If the user wants "an example of X", search directory names for X first;
   the repo is broad (agents, RAG, voice, MCP, fine-tuning) so there's often
   a directly relevant starting point rather than something to build from
   zero.

## Caveats
- Examples reflect whatever LLM providers/SDKs were current when written —
  package/API surfaces (OpenAI Agents SDK, CrewAI, LangChain, MCP libraries)
  move fast; verify against current docs before treating example code as
  correct today.
- These are demos/tutorials, not production-hardened apps — no assumption of
  auth, rate-limiting, or error handling beyond what's shown.
