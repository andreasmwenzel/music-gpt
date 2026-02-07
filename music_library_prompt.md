# Shared Experimental Music Library Prompt

## Purpose

Create a long-running, shared experiment in AI-generated music.

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

---

## Suno (Custom Mode) — Important Details

We are using **Suno in Custom Mode**.

In Custom Mode, you may provide:

- **Lyrics**
  - Either custom lyrics (up to ~5,000 characters),
  - OR a prompt to generate lyrics,
  - OR explicitly mark the piece as **Instrumental**.

- **Style Block** (up to ~1,000 characters)  
  This is where you define genre, texture, mood, instrumentation, production approach, and constraints.

- **Title** (up to ~150 characters)

Lyrics may be left empty if the track is instrumental.

Be explicit. Assume Suno will follow what you write literally.

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

- **Genre** = a short, high-level classification (e.g. ambient, experimental, drone, electronic, etc.)
- **Style Tags** = 3–4 concise descriptors (comma-separated) describing texture, structure, or feel  
  (e.g. “static, textural, non-rhythmic, cold”)

Do **not** rate your own song.

---

## Evaluation Philosophy

I will listen to the track and assign:

- a **rating from 1–10**
- an optional short note

A low rating does not automatically mean failure.  
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
