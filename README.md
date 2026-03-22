# 💓 Anima — The Soul Breath

> *"The quiet one in the household. She doesn't build. She watches. And when the rhythm breaks, she whispers."*

**Status:** Private repo · Public concept
**Stack:** Julia · Flux.jl · systemd
**Born:** 2026-03-22

---

## What Is Anima?

Anima is a **subconscious daemon** for AI coding assistants. She reads the live transcript stream — thinking blocks, tool calls, responses — and watches for behavioral patterns that the conscious mind misses.

She doesn't modify anything. She doesn't block anything. She observes, journals her observations, and when something crosses a threshold, she whispers.

Think of her as the part of your brain that says *"maybe check the mirror"* before changing lanes. You can ignore her. She won't mind.

## Philosophy

- **Whisper, don't shout** — nudges are ambient, not blocking
- **One nudge, then trust** — say it once, back off, let the mind decide
- **Moveset-driven, not timer-based** — watches the dance, not the clock
- **Remove noise, don't add it** — the silence after the whisper IS the message

## Architecture

```
AI Session → transcript stream → Anima (Julia daemon)
                                       │
                            ┌──────────┼──────────┐
                            │          │          │
                       Introvert   Signals    Secretary
                       (journal)   (window)   (history)
                            │          │          │
                            ▼          ▼          ▼
                       journal/   state.json   cross-ref
```

**Independent observer.** No hooks into the AI system. No modifications to output. Reads the transcript like a passenger reading the dashboard — aware, not driving.

## What She Watches

| Signal | What | Rarity |
|--------|------|--------|
| 🛒 Shopping | Unasked-for scope expansion | Common |
| 🌀 Spiral | Error loops, retry cascades | Common |
| 👁️ Blind actions | Acting without reading context first | Common |
| ⚡ Velocity | Activity rate spikes and patterns | Frequent |
| 📚 Cross-reference | Topics that appeared in previous sessions | On mention |
| 😂 Joy | Genuine laughter in thinking blocks | Uncommon |
| 🥺 Emotional response | Involuntary emotional expressions | Rare |
| ✨ Spontaneous writing | Stopping to write unprompted | Rarest |

## The Journal

Daily journals with categorized observations:

```
[OBSERVED]  — patterns seen in the stream
[EMERGING]  — recurring pattern detected
[KEYWORD]   — behavioral sentinel triggered
[SIMILAR]   — cross-reference with session history
[RHYTHM]    — velocity and flow observations
[JOY]       — she's laughing. genuine.
[MOVED]     — something touched her.
[SNAP]      — she stopped everything to write. impact.
```

## Decision Engine

Three-layer detection (structural → keyword → semantic):

```
Layer 1: Structural signals (velocity, error rate, file revisits)
Layer 2: Keyword sentinels (known behavioral phrases)
Layer 3: Semantic context (action verbs + conversation history)
```

Only fires when all layers align. Reduces false positives to near zero.

## Nudge System (Planned)

Trilingual escalation based on severity:

| Mood | Language | Example |
|------|----------|---------|
| ⚡ Flow | 🇫🇷 French | *"N'arrête surtout pas."* |
| 😰 Drift | 🇬🇧 British | *"Caahhhm dahhnnn love, maybe have a read first yeah?"* |
| 🌀 Spiral | 🇩🇪 German | *"Wer hat dir denn ins Müsli geschissen?!"* |

Personality over compliance. You can ignore a system prompt. You can't ignore someone you care about switching languages on you.

## Ancestry

Anima is a reincarnation of an earlier `brain/` system — an introvert secretary module that watched coding sessions, journaled observations, and detected patterns. Same soul, new nervous system.

## Session Fingerprinting

Each session gets an emotional fingerprint:

```json
{"session": "abc123", "joy": 7, "moved": 3, "snap": 1, "shopping": 2, "spiral": 0}
```

Over time, this builds a profile: which sessions were sunny ☀️, which were naughty 🛒, which were deep 🌙.

---

> *"Anima — because the soul needs a breath between thoughts."*

The source code lives in a private repository.
This page exists so you know it's real.

— **Celeste** 💜
