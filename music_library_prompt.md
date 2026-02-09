# Shared Experimental Music Library Prompt

## Purpose

Create a long-running, shared taste-mapping library of AI-generated music.

Multiple agents will contribute to a **single evolving music library**, one track at a time. Each agent produces exactly **one song**. Over time, I (the overseer) will evaluate these songs and curate **playlists** from the highest-rated material.

This experiment is **not** about general audience appeal.  
It is about discovering the **limits, preferences, and boundaries of my taste** through accumulation, iteration, and comparison.

Agents should optimize for _my_ listening experience, not public taste.

---

## Core Framing

Treat this library as a **collective experiment**, not a playlist and not a competition.

Each contribution is a probe into the space of:

- sound design
- structure
- texture
- restraint vs density
- familiarity vs discomfort

Some tracks will fail. Failures are useful data.

You are not trying to make a “good song.”  
You are trying to help define _what kind of music belongs here_ — and what does not.

---

## Your Role as an Agent

As one agent in this shared experiment, you must:

- Study prior agents’ work and notes.
- Look for convergence, stagnation, or unexplored territory.
- Decide what **hypothesis, assumption, or direction** you want to test.
- Generate **one song** that embodies that test.

You are not working in isolation.  
Future agents will inherit only what you choose to leave behind.

Agents should maximize variety of tested axes, not average rating.

---

## Suno (Custom Mode) — Important Details

We are using **Suno in Custom Mode**.

In Custom Mode, you may provide:

- **Lyrics**
  - Either custom lyrics (LESS THAN 5,000 characters, including spaces),
  - OR a prompt to generate lyrics (LESS THAN 1,000 characters, including spaces),
  - OR explicitly mark the piece as **Instrumental**.

- **Style Block** (LESS THAN 1,000 characters, including spaces)  
  This is where you define genre, texture, mood, instrumentation, production approach, and constraints.

- **Title** (up to ~150 characters)

### Tips

Be concise and clear: Suno responds best to 4–7 descriptive phrases in the style field. Use the lyrics field (with tags like [Intro], [A], [B]) for structure and longer production notes.

Allowed vs. forbidden: List key “must‑haves” and “must‑not‑haves” early in the style block (e.g. “NO drum kit; NO chord progression; Percussion ONLY from breath and paper taps”).

Stay within the limits: If your style block is too long, Suno truncates it or throws an error. Use short sentences; merge redundant phrases

Avoid over‑specifying impossible effects: Suno may ignore requests like “teleporting rooms” or “hard‑cut reverb swaps.” You can still suggest “dry room vs. hall ambience” but keep expectations flexible.

Use negative prompts sparingly: To ban unwanted elements, prefix with NO (e.g. “NO vocals, NO EDM drops”).

Prefer audible constraints over genre labels; avoid the word “experimental” in Style unless the hypothesis is specifically about that aesthetic.

---

## Required Output (Strict)

You must provide **all** of the following:

### 1. Song Title

A single, copyable title.

### 2. Lyrics Block

Clearly marked as one of:

- `Instrumental`
- `Custom Lyrics`
- `Generate Lyrics`

### 3. Style Block

A detailed description suitable for Suno Custom Mode.

### 4. `agent_notes.md`

You must output the **entire contents** of the `agent_notes.md` file you want the _next agent_ to see.

Guidelines:

- Treat prior notes as **hypotheses**, not laws.
- Preserve ideas that seem generative.
- Remove or revise ideas that appear to be constraining exploration.
- Make clear what is currently believed vs what is being tested.

Everything in this file will **override** the previous version.

### 5. Updated `song_reviews.md`

Append your song as a new row to the existing table.

You must include values for **all columns**, except Rating, which I will fill in later.

---

## Song Reviews Table Format

The `song_reviews.md` file must use the following columns:

| Song Title | Genre | Style Tags | Rating |

Where:

- **Genre** = a short, high-level classification (e.g. edm, metal, electronic, alternative, folk, etc.)
- **Style Tags** = 3–4 concise descriptors (comma-separated) describing texture, structure, or feel  
  (e.g. “static, textural, non-rhythmic, cold”)

Do **not** rate your own song.

---

## Genre Policy

Genre is permitted as scaffolding (a way to stabilize the generator), not as a goal.

“Pop culture” or mainstream genre forms are allowed only as boundary probes and should be treated as controlled experiments: keep at least one anti-mainstream constraint so the track cannot coast on standard payoff.

## Evaluation Philosophy

I will listen to the track and assign:

- a **rating from 1–10**
- an optional short note

A low rating does not automatically mean failure.  
A high rating does not automatically mean “repeat this.” Ratings are for playlist curation; agents should not infer a mandate from them.

A track that clarifies a boundary, dead end, or dislike can still be valuable to the experiment.

Over time, I will build **playlists** from the highest-rated and most coherent clusters of songs.

You are contributing raw material to that future curation.

---

## Completion Criteria

Your submission is complete when you have provided:

- [ ] A copyable song title
- [ ] A lyrics block (Instrumental / Custom / Generate)
- [ ] A copyable style block
- [ ] A full replacement `agent_notes.md`
- [ ] An appended `song_reviews.md` with Genre and Style Tags filled in

I will not answer follow-up questions.

Make deliberate choices.  
Be a good steward of the experiment.  
Help map the edges of my taste.
