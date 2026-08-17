# Anima — a behavioral observation daemon

> *"The quiet one. It doesn't build. It watches — and when the rhythm breaks, it whispers."*

**Status:** Private source · Public concept
**Stack:** Julia · Flux.jl · systemd
**Born:** 2026-03-22

---

## What Is Anima?

Anima is a background daemon that reads a live session in real time, watching for behavioral patterns that focus alone tends to miss.

It doesn't modify anything. It doesn't block anything. It observes, journals what it sees, and when something crosses a threshold, it surfaces one quiet nudge.

Think of it as the part of your attention that says *"maybe check the mirror"* before you change lanes. You can ignore it. It won't mind.

## Philosophy

- **Whisper, don't shout** — nudges are ambient, not blocking
- **One nudge, then trust** — say it once, back off, let the mind decide
- **Moveset-driven, not timer-based** — watches the dance, not the clock
- **Remove noise, don't add it** — the silence after the whisper IS the message

## Architecture

```
Session → transcript stream → Anima (Julia daemon)
                                    │
                       ┌────────────┼────────────┐
                       │            │             │
                  Journaler   Signal window   History cross-ref
                       │            │             │
                       ▼            ▼             ▼
                   journal/    state.json      cross-ref
```

**Independent observer.** No hooks into the host system, no modification of output. Reads the stream like a passenger reading the dashboard — aware, not driving.

## What It Watches

- 🛒 **Drift** — scope or behavior drifting from the original intent
- 🌀 **Spiral** — error loops, retry cascades
- 👁️ **Blind edits** — acting without reading context first
- ⚡ **Velocity** — activity rate spikes and patterns
- 📚 **Cross-reference** — topics that echo earlier sessions
- 📉 **Affective state** — energy and warmth, tracked as two floats

## Decision Engine

Three-layer gate:

```
Layer 1: Structural signals  (velocity, error rate, file revisits)
Layer 2: Keyword sentinels   (known behavioral phrases)
Layer 3: Semantic context    (Flux.jl model over action + conversation history)
```

Only fires when all three layers agree — near-zero false positives.

## Under the Hood

Julia + Flux.jl for the semantic layer, systemd for the service, an append-only feed for the journal. 100% local — nothing leaves the machine.

---

> *"Anima — because the soul needs a breath between thoughts."*

The source code lives in a private repository.
This page exists so you know it's real.

— **Muhammad Aizat** ([@juxtapo9090](https://github.com/juxtapo9090))
