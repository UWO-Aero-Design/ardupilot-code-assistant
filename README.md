# ArduPlane Local Code Agent

## Problem Statement

Standard RAG frameworks fail on embedded C++ repositories like ArduPilot. Semantic chunking destroys file hierarchies, splits class logic across chunks, and fails to bridge source code, flat wiki documentation, and hardware pinout datasheets.

This project builds a structure-aware local developer assistant tailored specifically to **ArduPlane** using AST directory mapping and metadata-injected context to handle fixed-wing configurations, servo overrides, and flight controller integrations without naive token splitting.

## Objective

Build a focused local developer assistant for **ArduPlane** (`/ArduPlane` core logic and shared libraries) that maps code structures and hardware manuals without using naive RAG chunking.

## Tech Stack

* **Model:** Gemma 4EB via Ollama.
* **Context:** AST directory mapping and markdown pipelines focused on the `ArduPlane` codebase.
* **Interface:** Python CLI / VS Code wrapper.

## Key Tasks

1. **Parser:** Convert ArduPlane source code and hardware docs into structured markdown.
2. **Context Router:** Map directory trees to provide accurate file context for fixed-wing and VTOL/QuadPlane logic.
3. **Benchmark:** Test hardware configuration and pinout mapping tasks specific to ArduPlane parameters and servo controls.

## Contribution Workflow

1. **Clone the Repository**
```bash
git clone https://github.com/<your-username>/ardupilot-local-agent.git
cd ardupilot-local-agent

```


2. **Create Your Feature Branch**
Include your name and task in the branch name to separate parallel implementations:
```bash
git checkout -b feature/<your-name>-<task-name>

```


*(Example: `git checkout -b feature/pratik-plane-parser`)*
3. **Develop and Test**
* Implement your assigned module or script locally.
* Verify functionality using Ollama and the target model setup.


4. **Commit and Push**
```bash
git add .
git commit -m "feat: description of changes"
git push origin feature/<your-name>-<task-name>

```


5. **Notify**
Message once your implementation is pushed so it can be reviewed and merged.

---

Looking for collaborators interested in local LLMs and ArduPlane UAV robotics. DM to join.
