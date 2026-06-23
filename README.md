# LearnLoop — Cowork starter

A personal learning system that runs entirely inside Cowork. **The files are the database; the agent is the runtime.** No servers, no setup — open this folder in Cowork and start talking to it.

## How to start

1. Open this folder in Cowork.
2. Say: **"Read operating-instructions.md and follow it. Run `status`."**
3. Then try **`learn AI Retrieval`** to take your first depth step, or **`digest`** to pull and curate today's news against the concept map.

The agent reads your concept map and progress at the start of each session and writes them back at the end — so your understanding accumulates across days.

## What's here

- `operating-instructions.md` — the runtime: the commands and the rules the agent follows. Start here.
- `index.yaml` — the root index listing all subjects and their folder locations.
- `<subject>/` — one folder per subject, e.g. `ai-retrieval/`. Each contains:
  - `map.yaml` — the concept map with prerequisites and rubrics.
  - `progress.yaml` — your mastery state. Starts all `unseen`.
  - `cards.yaml` — spaced-recall items minted as you learn.
  - `deep-dives/` — generated interactive HTML explainers and their `index.yaml`.

## Commands

- `status` — where you are across subjects.
- `learn <subject>` / `next` — take the next step along the map (depth).
- `digest` — curate today's news against your concept map (breadth).
- `deep dive <n>` — generate a grounded interactive explainer for an item.
- `review` — run due spaced-recall cards.
- `add subject <name>` — generate a new concept map.

## Good to know

- This is a faithful prototype of the larger design: the YAML files map onto database tables and the operating instructions onto code, so nothing here is throwaway when you graduate to the deployed version.
- It depends on the agent reading and writing the state files every session — that discipline is what makes progress stick.
- The honest risk is the understanding-check going easy on you. The instructions tell it to grade against each concept's rubric and to mark concepts `shaky` when earned; hold it to that.
