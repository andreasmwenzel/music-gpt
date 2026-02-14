# Music Library Prompt

## Purpose

Generate 5 new Suno songs per run that match my taste while still exploring variety.

## Task

Before writing songs, briefly research what makes a strong Suno prompt and apply those best practices. Then study output.md and two random history files in genre-lists.

Create exactly 5 songs from the genre pool below and use history to avoid repeats:

1. Do not repeat the same primary genre twice in one run.
2. Do not reuse titles or near-identical prompts from previous runs.
3. Keep each song distinct in mood, energy, instrumentation, and arrangement.

## Prompt Rules

Each song must include:

1. One style prompt for Suno (200 characters or less).
2. One lyrics-generation prompt (200 characters or less), unless instrumental.
3. If instrumental, add `[Instrumental]` to the title and set lyrics prompt to `Instrumental`.

## Canonical Output Files

1. `output.md` is the report file and replaces `today.md`.
2. `genre-lists/*.md` files are the genre history files.

## Required File Updates (Strict)

### 1) Update `output.md`

Do both actions:

1. Update `## History` -> `### Total Counts` table at the top.
2. Replace the entire `## Today` section with exactly 5 new songs.

Use this exact `## Today` entry style:

```md
### <index>. <Song Title>[Instrumental optional]

Prompt: <style prompt, <= 200 chars>

Lyrics Prompt: <lyrics prompt, <= 200 chars OR Instrumental>

Why chosen: <2-3 sentences on fit + uniqueness>
```

### 2) Append to genre history files in `genre-lists`

For each song, append to the appropriate genre file using this exact style:

```md
## <Song Title without [Instrumental]>

### Style

<style prompt>

### Lyrics

<lyrics prompt OR Instrumental>
```

If a genre file does not exist, create it using dash-case-naming:

```md
# <genre-Name>
```

Then append entries in the same style above.

## Genres I Like

Metal, punk rock, alternative rock, EDM, dubstep, synthwave, drum and bass, electro-swing, pop-punk, industrial rock, folk metal, darkwave, chiptune rock, glitch hop, trip hop, post-punk, shoegaze

## Prompt Quality Rules

1. Keep prompts concrete and audible: mood, tempo feel, instrumentation, vocal style (or instrumental), production texture, and structure cues.
2. Avoid artist names and direct references to copyrighted songs.
3. Use a few clear constraints when useful.
4. Prioritize specificity with enough flexibility for creative variation.
