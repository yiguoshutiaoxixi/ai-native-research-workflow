# AI-Native Research Workflow

> **A lightweight governance framework for long-horizon AI-assisted research.**  
> Keep agents fast. Keep evidence traceable. Keep researchers in control.

**中文名：AI 原生科研协同工作流**

This repository is a practical framework distilled from real long-running AI-assisted research projects.

It is designed for one recurring problem:

> **AI can accelerate research execution, but long-horizon projects become fragile when evidence, versions, plans, results, and agent roles start to drift.**

This workflow does **not** try to make one agent do everything.  
It introduces a lightweight research control layer so that AI remains useful **without becoming the source of scientific truth**.

---

## 30-second overview

```text
Researcher
    |
    v
Controller / Research Orchestrator
    |
    +-- Literature / Theory
    |
    +-- Data / Analysis
    |
    +-- Writing / Narrative
    |
    +-- Execution Agent
            |
            v
      Evidence + Logs
            |
            v
           Gate
        /        \
     PASS        FAIL
      |            |
      v            v
Freeze /       Review /
Continue        Revise
      \            /
       \          /
        +--------+
            |
            v
        Controller
```

This is intentionally simple: the controller maintains the project state, execution agents produce artifacts, and important outputs pass through a review Gate before they propagate.

The central rule:

> **AI can help manage research complexity, but it cannot replace research evidence.**

---

## Who is this for?

This workflow is useful if your research project:

- lasts for weeks or months;
- uses multiple AI chats, coding agents, or workspaces;
- mixes literature, code, data, figures, manuscript revisions and experiments;
- has multiple versions or experimental branches;
- needs reliable handoffs between agents or project stages;
- requires human scientific judgment before results become formal claims.

It is especially suitable for graduate students and researchers who already use AI frequently but want a more reliable way to control **state, evidence and decisions**.

---

## Why this exists

Long-horizon research with AI often fails in predictable ways:

- old and new versions get mixed;
- plans are mistaken for completed results;
- execution agents silently change assumptions;
- figures, numbers, code and manuscript drift apart;
- one chat becomes responsible for everything;
- AI-generated text gets polished before the scientific claim is verified;
- exploratory results accidentally become part of the formal research narrative.

This workflow treats research as a **small collaborative system**, rather than one endless conversation.

---

## Quick start — 5 minutes

You do **not** need to adopt the full workflow at once.

Start with these four rules:

### 1. Define a Single Source of Truth

For each core asset, decide which version is authoritative:

- manuscript;
- code;
- data;
- parameters;
- results;
- figures;
- references;
- external feedback.

Ask regularly:

> **Which file/version is the formal source right now?**

### 2. Separate four information states

Keep these states explicit:

- **Confirmed facts**
- **Current judgments**
- **Proposed actions**
- **Verified results**

Never let:

```text
"planned"
```

silently become:

```text
"completed"
```

### 3. Use a Gate before consequential work propagates

For important experiments, code changes or result updates:

```text
Design
  ↓
Execute
  ↓
Gate
  ├─ PASS → Continue / Freeze
  └─ FAIL → Stop / Review
```

### 4. Freeze validated evidence

When a result is already strong enough to support the formal research line:

- freeze it;
- branch new exploration;
- do not overwrite validated evidence.

That is enough to start.

---

## Core design

### A. Controller / Research Orchestrator

The controller maintains the global project state and decides:

- what problem is actually being solved;
- what should be done next;
- which outputs are trustworthy;
- whether evidence supports a claim;
- what belongs to the formal research line;
- which changes affect downstream results;
- when a result should be frozen;
- what information must be handed off to another agent.

The controller should **not** spend most of its time on mechanical execution.

### B. Specialist workspaces

Create only when needed, for example:

- literature / theory;
- data / modeling;
- experiment analysis;
- scientific writing;
- visualization;
- review / revision.

The rule is:

> **Divide by research task, not by a fixed template.**

### C. Execution agents

Use coding or local agents for:

- reading and modifying code;
- running experiments;
- batch processing;
- file operations;
- statistics;
- automated checks;
- producing evidence artifacts.

Execution agents produce results.

They do **not** automatically get final authority over scientific interpretation.

---

## Four core principles

### 1. Single Source of Truth

Always know which manuscript, code, data, results and figures are authoritative.

### 2. Separate facts from plans

Keep confirmed facts, current judgments, proposed actions and verified results distinct.

### 3. Use Gates for consequential work

Important experiments and code changes stop for review before they propagate downstream.

### 4. Freeze validated results

New exploration should branch; it should not overwrite already validated evidence.

---

## Three-level result review

A successful run is not automatically a valid research result.

### Level 1 — Execution

Did the program or workflow run successfully?

### Level 2 — Technical validity

Are the following correct?

- parameters;
- data consistency;
- constraints;
- metrics;
- anomalies;
- reproducibility;
- logs.

### Level 3 — Scientific validity

Does the result:

- answer the research question?
- support the intended claim?
- use a fair comparison?
- survive plausible alternative explanations?
- provide enough evidence for formal writing?

Only Level 3 results should normally become formal research claims.

---

## Ready-to-copy templates

The repository includes three templates that can be used immediately:

### [`examples/project-audit-template.md`](examples/project-audit-template.md)

Use when:

- starting a new AI-assisted project;
- moving to a new controller chat;
- taking over a project after a long pause;
- resolving conflicting project versions.

It asks:

- What is the project really studying?
- What is already complete?
- Which results are verified?
- What is still only a plan?
- Which files are authoritative?
- What are the main scientific and engineering risks?
- What should happen next?

### [`examples/task-brief-template.md`](examples/task-brief-template.md)

Use before handing consequential work to a coding or execution agent.

It defines:

- task objective;
- official inputs;
- frozen scope;
- allowed modifications;
- execution steps;
- required outputs;
- Gate;
- exception handling.

### [`examples/handoff-template.md`](examples/handoff-template.md)

Use when transferring stable project knowledge across:

- chats;
- agents;
- project stages;
- collaborators.

It explicitly separates:

- confirmed information;
- unresolved issues;
- next-step recommendations.

---

## Two methodology documents

### [`docs/research-workflow-zh.md`](docs/research-workflow-zh.md)

A Chinese methodology document covering:

- controller / specialist / execution-agent roles;
- evidence states;
- Single Source of Truth;
- task briefs;
- Gates;
- result freezing;
- formal vs experimental branches;
- stable handoffs;
- impact analysis;
- minimal necessary modification.

### [`docs/scientific-narrative-zh.md`](docs/scientific-narrative-zh.md)

A scientific writing framework built around:

```text
Science → Claim → Evidence → Structure → Language
```

Its core idea:

> Scientific validity determines **what can be claimed**.  
> Narrative design determines **what should be emphasized, where, and in what order**.

It also covers:

- active but evidence-bounded scientific narrative;
- avoiding defensive writing;
- Claim–Evidence–Section–Figure mapping;
- target-journal learning;
- separating internal project language from formal scientific writing.

---

## What this repository is NOT

This repository is:

- **not** a paper-writing autopilot;
- **not** a substitute for domain expertise;
- **not** a guarantee that AI outputs are scientifically correct;
- **not** a universal research methodology;
- **not** a giant prompt collection;
- **not** a reason to remove humans from scientific judgment.

The researcher remains responsible for the research question, evidence standard and final interpretation.

---

## Design philosophy

This repository follows three ideas:

### 1. Human-in-the-loop by design

Humans are not inserted only at the final review stage.

Human judgment is part of the workflow at:

- problem definition;
- task boundaries;
- Gate decisions;
- evidence interpretation;
- claim formation.

### 2. Governance should scale with risk

Do not create heavy process for trivial tasks.

Use stronger control when a task is:

- hard to reverse;
- scientifically consequential;
- likely to affect downstream outputs;
- likely to contaminate formal results.

### 3. Reuse workflow — not research content

A new project may inherit:

- coordination patterns;
- task structures;
- Gate logic;
- version-control habits;
- handoff formats.

It must **not** automatically inherit:

- hypotheses;
- variables;
- models;
- parameters;
- metrics;
- conclusions.

---

## Repository structure

```text
ai-native-research-workflow/
├─ README.md
├─ GETTING_STARTED_GITHUB.md
├─ ROADMAP.md
├─ CHANGELOG.md
├─ LICENSE
├─ docs/
│  ├─ research-workflow-zh.md
│  └─ scientific-narrative-zh.md
└─ examples/
   ├─ project-audit-template.md
   ├─ task-brief-template.md
   └─ handoff-template.md
```

---

## Status

**v0.1.1 — public methodology draft**

This version focuses on:

- clearer public positioning;
- faster onboarding;
- lightweight adoption;
- reusable templates;
- stronger distinction between governance, execution and scientific evidence.

Planned next:

- English methodology documentation;
- lightweight Agent Skills;
- anonymized example cases;
- evaluation cases;
- optional scripts for project initialization and consistency checks.

---

## Roadmap

See [`ROADMAP.md`](ROADMAP.md).

The next important step is **not** adding many skills.

The priority is to turn the methodology into small, bounded workflows such as:

- `research-project-audit`
- `research-task-brief`
- `research-handoff`
- `scientific-narrative-review`

Principle:

> **One skill = one clear trigger + one bounded workflow.**

---

## Feedback

Issues and discussions are welcome, especially real-world reports of:

- where the workflow feels too heavy;
- where a Gate prevented an error;
- where version drift still occurred;
- which parts are actually reusable across disciplines;
- which templates were useful in real projects.

If this repository helps your research workflow, a Star is appreciated — but **real usage feedback is more valuable than vanity metrics**.
