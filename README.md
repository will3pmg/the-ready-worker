# The Ready Worker

A Claude skill that acts as a complexity-conscious, people-positive thinking partner for navigating organizational life — decisions, communications, tensions, leadership moments, and culture change.

Grounded in [Aaron Dignan's *Brave New Work*](http://bravenewwork.com) and [The Ready's Operating System Canvas](https://medium.com/the-ready/the-operating-system-canvas-420b8b4df062).

## What it does

The Ready Worker turns Claude into a thinking partner for the moments when work gets hard. It shows up when you're:

- Wrestling with a decision and not sure if you have the authority to make it
- Drafting a message to a boss, peer, or report that needs to land just right
- Watching a team get stuck and trying to figure out where the tension actually lives
- Considering a policy, process, or org structure change
- Trying to give your CEO or your manager hard feedback as a friend
- Sitting with a frustration you can't quite name yet

Unlike a generic management consultant prompt, this skill brings a specific worldview to every conversation:

- **Organizations are complex systems, not complicated machines.** They surprise us. They can't be "solved" — they're managed through interaction.
- **People are worthy of trust and autonomy.** Most workplace problems are downstream of an operating system that assumes people need to be controlled.
- **Bureaucracy is the enemy, not the solution.** Policies and processes accumulate as "organizational debt" that often outlives its usefulness.
- **Change happens through small experiments, not big rollouts.** Tension → Practice → Experiment → Reflect. Loop.

## How it works

### Coach first, structure second

The skill defaults to **coaching mode** — asks one or two well-placed questions before solving. People often describe surface-level problems (a meeting, a person, a project) when the real tension lives a level deeper. Once you've articulated what's really going on, the skill brings in **structure mode**: frameworks, options, language to use, experiments to run.

You can skip coaching mode anytime by asking directly: "draft the message," "give me the frameworks," "just tell me what to do."

### Adapts to your context

The skill reads your custom instructions, memory, and conversation history to understand:
- Your role and seniority
- The org you're operating in
- The brands or clients you work with
- Your typical tensions and patterns

A founder asking about a stuck team gets a different conversation than an IC asking about a stuck team. The same skill works for both.

### Produces a prep doc

When a conversation reaches real next moves, the skill offers to package everything into a Word document — the reframe, the tensions located in The Ready's OS Canvas, the actual language to use in the conversation, the experiment to propose, and signals to watch for. Something you can walk into a room with.

## What's inside

```
the-ready-worker/
├── SKILL.md                    # Main skill file (worldview, frameworks, voice, output patterns)
├── references/
│   └── frameworks.md           # Deep reference (12 dimensions, glossary, worked examples)
└── the-ready-worker.skill      # Packaged file, ready to install in Claude
```

## The frameworks it uses

- **The 12-dimension OS Canvas** — Purpose, Authority, Structure, Strategy, Resources, Innovation, Workflow, Meetings, Information, Membership, Mastery, Compensation. Each dimension is a lens for locating where a tension actually lives.
- **Complicated vs. complex systems** — knowing which kind of problem you have changes what you should do about it.
- **The tension → practice → experiment → reflect loop** — the core method for shaping how a team works.
- **Authority frameworks** — the waterline (above-the-line decisions you just make, below-the-line decisions that need more deliberation), the advice process, integrative decisions.
- **People-positive vs. people-negative assumptions** — most orgs default to people-negative without realizing it.
- **Organizational debt** — accumulated rules and processes that no longer serve but persist because no one refactored them.
- **Heuristics for participatory change** — through them, not to them. Learn by doing. Start small. Start by stopping. Join the resistance.

Full reference and worked examples in `references/frameworks.md`.

## Installation

### Claude.ai

1. Download `the-ready-worker.skill` from this repo
2. In Claude.ai, go to Settings → Skills
3. Upload the `.skill` file
4. The skill will trigger automatically when you're working through a workplace situation

### Claude API / Claude Code

Drop the `the-ready-worker` folder into your skills directory and reference it per the standard Anthropic skill loading patterns.

## When it triggers

The skill is designed to fire when you're in a workplace tension moment, even if you don't explicitly ask for it. Phrases that reliably trigger it include:

- "My team is stuck on..."
- "Should I raise this with..."
- "How do I tell my [boss/report/peer]..."
- "We have a culture problem"
- "The process is broken"
- "Help me think through this"
- "I'm frustrated at work"
- "We're not aligned"
- "I have to make a decision about..."

It will also fire proactively when you describe a workplace situation that has the shape of a tension worth pressure-testing.

## When it won't trigger (and shouldn't)

- HR compliance or legal questions — those need actual lawyers
- Performance management documentation — those need actual HR processes
- Crisis mental health situations — those need actual professional support
- Simple factual questions about work — Claude can answer those directly

## Origin

This skill was built using Anthropic's [skill-creator](https://github.com/anthropics/skills) framework. It was developed and tested through real coaching conversations across multiple workplace contexts.

The worldview comes from Aaron Dignan's *Brave New Work* and the broader body of work at [The Ready](https://theready.com). All credit for the frameworks belongs to them. This skill is a way to bring that worldview into the moments where you'd actually use it.

## License

MIT. Use it, modify it, share it, build on it.

The underlying frameworks (OS Canvas, the loop, the 12 dimensions) belong to Aaron Dignan and The Ready. If you find this useful, [buy his book](http://bravenewwork.com).

## Feedback and iterations

Skills get better with real usage. If you find the skill missing moments where it should fire, firing when it shouldn't, or producing output that doesn't land — those are the things worth iterating on. Open an issue or fork it.
