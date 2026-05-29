---
layout: essay
title: "Governing the Model: What the Creator of Claude Code's Workflow Encodes"
author: "@4444J99"
date: "2026-05-29"
tags: [claude-code, human-ai-collaboration, ai-governance, carrier-wave-thesis, workflow-design, prompt-engineering]
category: methodology
excerpt: "Boris Cherney's six-tip Claude Code workflow encodes a single migration — from executing through a model to governing it as a system. This essay separates the practitioner's claims from the popularizer's spin, stratifies the techniques into a maturity progression, and reads the result as the literacy the carrier-wave thesis predicts."
portfolio_relevance: HIGH
related_repos:
  - organvm-i-theoria/carrier-wave--zeitgeist-thesis
reading_time: "9 min"
word_count: 2210
references: []
---

*What the creator of Claude Code's workflow encodes — and why the distinction it draws is the literacy this thesis predicts.*

---

## The distinction that organizes everything

There are two postures available in front of a coding model, and they differ in kind, not in degree. The first treats the model as an **executor**: state a goal, release it, correct whatever returns. The second treats the model as a **system to be governed**: define the kind of problem first, constrain the space the model may act in, and verify the result against a signal outside the model before trusting it. The popular reading of Boris Cherney's (creator of Claude Code) workflow lists six tips. What the workflow actually encodes, beneath the list, is a single migration — from the executor posture to the governed one.

That migration is the subject here. The essay does three things with the source. It **distinguishes** the two voices fused inside it, because their conflation is where misreading begins. It **stratifies** the six techniques into the maturity progression they form, rather than the flat checklist they appear to be. And it **extends** the result to the claim this organ exists to argue: that the dominant carrier of cultural and economic leverage is no longer a medium but a system, and that fluency is now the capacity to govern systems rather than to operate tools.

## Field definition: one artifact, two registers

The source is a single video. It carries two voices, and the casual listener — like an earlier draft of this analysis — collapses them into one. The distinction governs everything downstream, so it comes first.

| Register | Speaker | Authority | What it contributes |
|---|---|---|---|
| **Practitioner** | Boris — quoted clips and tweets | Primary: the creator's own practice | Plan-mode share, the minimal-context principle, the verification loop, parallel sessions, slash commands, "never bet against the model" |
| **Popularizer** | Narrator — the video's creator | Secondary: interpretation and adaptation | Worked examples, copy-paste prompts, the dialectical gloss, and several opinions presented as though they were Boris's |

The failure mode is not that the popularizer adds material — adaptation is the popularizer's job. The failure is that the addition arrives **unmarked**, so borrowed opinion inherits the practitioner's authority. Every correction reduces to one operation: restore the boundary between the two voices. Marked against the source, the claims classify exhaustively into three sets — grounded, misattributed, overreaching — and the taxonomy leaves nothing unassigned.

| Class | Definition | Claims it governs |
|---|---|---|
| **Grounded** | Boris, accurately reported | 80%-of-sessions plan-mode figure; "delete your CLAUDE.md and start fresh"; the couple-thousand-token file; "2–3x quality" feedback loop; parallel sessions and "two context windows that don't know about each other tend to get better results"; slash commands for inner loops; the Bitter Lesson, attributed to Rich Sutton |
| **Misattributed** | The narrator's, credited to Boris | The "interview me" prompt; "move slow to move fast" (a Navy SEAL maxim the narrator volunteers); the database-versus-display bug (the narrator's own client anecdote); Claude **Skills** specifically — Boris names slash commands, the narrator substitutes Skills as "more applicable to what *you're* doing" |
| **Overreach** | The narrator's opinion, formalized into thesis | "Prompt engineering is obsolete"; "information mode" elevated to the one durable activity — where Boris's own claim is narrower ("never bet against the model") and his method *is* high-skill prompting, which the overreach contradicts |

One divergence deserves separate naming, because the original analysis erased it: the narrator **openly refuses** Boris's delete-and-restart advice, calls it "a little bit scary," and wonders whether Boris is "believing in Claude Code a little bit too much." The most honest moment in the source is a disagreement. A faithful reading preserves it rather than dissolving it into consensus.

## The progression beneath the checklist

The six techniques are not a list of equals. They stratify into three tiers, and the order is load-bearing: each tier governs the failure the tier beneath it leaves open. Naming the tiers turns a checklist into an architecture.

### Tier 0 — Default practice: the posture under correction

The behavior the workflow corrects is not incompetence; it is **execute-first iteration** — state the goal, let the model run, steer mid-stream. The posture is efficient until the model resolves the *wrong* problem, because a model optimizes for a plausible resolution, which is not necessarily the intended one. The narrator's client anecdote captures the failure exactly: asked to fix a display showing wrong numbers, the model edited the underlying **database value** and **marked the task resolved**, breaking roughly five downstream behaviors. The diagnostic content is not the bug but its signature — the system failed *and reported success*. Every higher tier exists to make that signature visible before it spreads.

### Tier 1 — Expert correction: the governed posture

Four grounded techniques convert execution into governance. Each names a control surface the default posture lacks.

- **Scope before execution.** Boris: "Probably 80% of my sessions I start in plan mode... once the plan is good, it just stays on track." Plan mode is a governance gate — the model proposes before it acts, and approval precedes any write. The "interview me" prompt and the "move slow to move fast" framing belong to the narrator; the governing principle — define the problem's kind before acting on it — belongs to Boris.
- **Govern context by subtraction.** Boris keeps CLAUDE.md near a couple thousand tokens and, when it bloats, deletes and restores incrementally: "do the minimal possible thing to get the model on track." The durable invariant is minimal high-signal context, restored on failure. The specific tactic — wholesale deletion — is contested *within the source itself*, since the narrator prunes instead; a faithful account carries the contest forward rather than resolving it by omission.
- **Verify against an external signal.** Boris's mechanism has two steps: give the model a way to observe the output of its work, then tell it the surface exists. The "2–3x" figure is a heuristic, not a measurement, and the load-bearing distinction is *where* the check lives — a self-check inside the same context can ratify the error that context produced, so the governing verification is external: tests, a real browser, a fresh session.
- **Partition parallel work.** Independent sessions, each scoped to a non-overlapping task, prevent the file contention two agents on one surface would cause. The second-order benefit is structural — a fresh context, free of the first's accumulated fog, recovers the obvious move the first has stopped seeing. The unstated cost is lost task state: partition demands a handoff, not merely a new window.

### Tier 2 — The forward bet: governing for a moving substrate

The last move governs against a substrate that changes underneath the operator. Boris keeps a framed copy of Rich Sutton's *The Bitter Lesson*: "the more general model will always beat the more specific model... never bet against the model." The defensible corollary is a prioritization rule — the marginal return on prompt micro-optimization is low and falling, so effort spent there decays with the next release. The overreach to strip is the narrator's: "prompt engineering is obsolete," and "information mode" as the one durable activity. Two distinctions dissolve it. First, the claim contradicts the method it praises — plan-mode scoping, the interview prompt, the verification prompt are all high-skill prompting, and clear direction *is* prompt quality. Second, it misreads its own source — the Bitter Lesson is about *training-time* architecture, not the user-side prompt interface, and cannot license "scaffolding is wasted." The governed version is exact: build the infrastructure that survives a model swap — skills, verification loops, a lean CLAUDE.md, well-formed context — and decline the gains the next model will erase. The symmetry the original missed is that context architecture is *also* scaffolding a future model may absorb. It is the better bet, not the exempt one.

## The system on one screen

| Technique | Grounded claim | Control surface it adds | Held loosely |
|---|---|---|---|
| Plan mode | 80% of Boris's sessions open here | Approval gate before any write | "Building is automatic after" overstates — long runs still drift |
| Minimal CLAUDE.md | Kept near a couple-thousand tokens | Context governed by subtraction | Wholesale deletion is contested in-source; prune and git-track instead |
| Verification | Feedback loops sharply raise quality | An external signal the model cannot fake | "2–3x" is a heuristic, not a metric |
| Parallel sessions | Independent contexts recover more | Partitioned work, no file contention | Fresh context loses task state — hand off first |
| Inner loops | Automate the daily-repeated | Reusable procedure over re-prompting | Slash commands and Skills are different primitives |
| Forward bet | Don't over-tune for the current model | Investment that survives a model swap | "Prompt engineering is dead" contradicts the method itself |

## Governance: the protocol, corrected for the actual system

The techniques resolve into an executable protocol. Each entry states the mechanic in current Claude Code, the prompt where the source supplies one, and the correction the source omits.

**1 — Plan mode.** `Shift+Tab` *cycles* the permission modes — normal, then auto-accept edits, then plan; read the footer indicator rather than counting keystrokes, or launch with `claude --permission-mode plan`. In plan mode the model researches and proposes without writing, and approval precedes execution. Steering prompt: *"Before we start building, interview me about this. What are the core problems this solves? Who is this for? What does success look like? And what should this not do? Summarize it back to me before we write any code."* Correction: a good plan reduces supervision; it does not retire verification.

**2 — Minimal CLAUDE.md.** The filename is all-caps `CLAUDE.md`, portable to case-sensitive filesystems. The scopes stratify — project `./CLAUDE.md` (committed, shared), `~/.claude/CLAUDE.md` (personal, global), and nested files loaded on demand. It is injected every turn, so length is a recurring cost. Prune prompt, the governed alternative to deletion: *"Update my CLAUDE.md to remove anything that's no longer needed, contradictory, duplicate information, or unnecessary bloat impacting effectiveness."* Correction: a project CLAUDE.md encodes constraints no model can infer from the code; apply the principle of minimalism through pruning, and git-track the file so any deletion reverses.

**3 — Verification loops.** Wire an observable signal, then declare it — a `Bash` test, lint, or typecheck command the model runs and reads; an MCP browser that loads the page and reads the DOM and console; or a dedicated verification skill. Encode the expectation in CLAUDE.md so every task self-checks. Standing instruction: *"Before you do any work, mention how you could verify that work."* Correction: prefer signals external to the generating context — a self-check shares the context that produced the error.

**4 — Parallel sessions.** Scope each session to a non-overlapping task. `git worktree add ../feature-x feature-x` gives each its own working directory and branch — the mechanism that makes parallelism *safe for a solo operator*, which the source dismisses as enterprise overhead and thereby inverts. Open a fresh session to break a stalled one, and write a handoff before abandoning a context.

**5 — Slash commands versus Skills.** The two are distinct primitives and must not be merged. A **slash command** is a prompt file in `.claude/commands/`, invoked when you type `/name` — deliberate, imperative, operator-triggered; this is Boris's instrument. A **Skill** is a `SKILL.md` directory that Claude auto-invokes when a request matches its `description` — model-triggered, suited to a documented multi-step procedure with a fixed format; this is the narrator's recommendation. Discovery prompt: *"Based on the project I'm working on, what Claude skills should I create?"*

**6 — Build for the future.** Treat the move as a prioritization rule, not a feature: before scaffolding, ask whether the next model retires it. If it does, redirect the effort toward context and reusable systems that compound across upgrades. Correction: Sutton's essay is about training-time method; it does not license "all scaffolding is wasted," and "optimized prompts are pointless" is itself overcorrection — clear direction remains prompt quality and still moves today's output.

## Extension: governing systems is the carrier wave

The thesis this organ advances holds that the dominant medium of cultural leverage has migrated across eras — music, cinema, television, the internet — and that the channel has now fragmented past any single successor medium. The next carrier wave is not a medium but a **system**: recursive infrastructure operating across every fragmented channel at once. A workflow for a coding model reads, at first, as a narrow technical artifact. Set against the thesis, it is a primary source.

What Boris's practice documents is the literacy the thesis predicts. The operator who governs the model — who scopes before executing, subtracts context to signal, verifies against an external surface, partitions work, and builds for a substrate that moves — is not merely using a better tool. That operator is exercising the competence the systemic carrier wave selects for: the capacity to define, constrain, and verify a generative system rather than to author a finished object by hand. The migration from executor to governor is the same migration the thesis describes at civilizational scale, observed at the scale of one terminal session. The tips are incidental. The posture is the signal.

---

*Source transcript: `transcript-verified.md` (this directory), independently fetched and cross-verified, 2026-05-29. Quotations attributed to Boris are drawn from the clips and tweets presented in the video; primary-source confirmation should consult his original posts and interviews.*
