# AI-Native Research Workflow

> A practical workflow for long-horizon research with AI agents: keep evidence, versions, decisions, and handoffs under control.

**中文名：AI 原生科研协同工作流**

This repository is a practical, research-first framework distilled from long-running AI-assisted research projects.  
It is not a “one prompt writes a paper” recipe. Its goal is to make AI collaboration **traceable, reviewable, and evidence-aware**.

## Why this exists

Long-horizon research with AI often fails in predictable ways:

- old and new versions get mixed;
- plans are mistaken for completed results;
- execution agents silently change assumptions;
- figures, numbers, code and manuscript drift apart;
- one chat becomes responsible for everything;
- AI-generated text gets polished before the scientific claim is verified.

This workflow treats research as a small collaborative system rather than a single endless chat.

## Core model

```text
Researcher
    │
    ▼
Controller / Research Orchestrator
    │
    ├── Literature / Theory
    ├── Data / Analysis
    ├── Writing / Narrative
    └── Execution Agent (code, files, batch runs)
             │
             ▼
        Evidence + Logs
             │
             ▼
            Gate
             │
             ▼
      Freeze / Continue / Revise
```

The central rule is simple:

> **AI can help manage research complexity, but it cannot replace research evidence.**

## Four principles

1. **Single Source of Truth**  
   Always know which manuscript, code, data, results and figures are authoritative.

2. **Separate facts from plans**  
   Keep confirmed facts, current judgments, proposed actions and verified results distinct.

3. **Use Gates for consequential work**  
   Important experiments and code changes stop for review before they propagate downstream.

4. **Freeze validated results**  
   New exploration should branch; it should not overwrite already validated evidence.

## What is in v0.1

```text
ai-native-research-workflow/
├─ README.md
├─ GETTING_STARTED_GITHUB.md
├─ ROADMAP.md
├─ LICENSE
├─ docs/
│  ├─ research-workflow-zh.md
│  └─ scientific-narrative-zh.md
└─ examples/
   ├─ project-audit-template.md
   ├─ task-brief-template.md
   └─ handoff-template.md
```

### `docs/research-workflow-zh.md`
A practical governance model for long-running AI-assisted research projects:
roles, evidence states, Single Source of Truth, task briefs, Gates, freezing, branching, and stable handoffs.

### `docs/scientific-narrative-zh.md`
A scientific writing framework built around:

```text
Science → Claim → Evidence → Structure → Language
```

It separates scientific validity from narrative design and discourages both defensive writing and unsupported promotion.

### `examples/`
Ready-to-copy templates for:
- project cognition audit;
- high-impact task briefs;
- cross-agent / cross-chat handoffs.

## What this repository is NOT

- not a paper-writing autopilot;
- not a substitute for domain expertise;
- not a promise that AI outputs are scientifically correct;
- not a universal research methodology;
- not a collection of giant prompts.

The researcher remains responsible for scientific judgment.

## Intended users

Researchers and graduate students who use multiple AI systems, coding agents or long-running workspaces and need a lightweight way to control:

- project state;
- evidence provenance;
- task boundaries;
- version drift;
- handoffs;
- scientific claims.

## Status

**v0.1 — public methodology draft**

This first version intentionally prioritizes clear methodology and reusable templates over automation.

Planned later:
- English documentation;
- lightweight Agent Skills;
- example cases;
- evaluation cases;
- optional scripts for project initialization and consistency checks.

## Feedback

Issues and discussions are welcome, especially real-world reports of:

- where the workflow is too heavy;
- where a Gate prevented an error;
- where version drift still occurred;
- which parts are actually reusable across disciplines.

---

If this repository helps your research workflow, a Star is appreciated — but real usage feedback is even more valuable.
