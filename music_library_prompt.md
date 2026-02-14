# Music Library Prompt

## Purpose

Generate 5 new Suno songs per run that match my taste while still exploring variety.

## Task

Before writing songs, do a quick prompt-quality pass and keep it lightweight:

1. If web access is available, quickly check one Suno prompting reference and apply the best practices.
2. If web access is unavailable, proceed without blocking and use known best practices.
3. Study `output.md` and exactly two genre history files in `genre-lists`: use the two highest-count genres from `output.md` `### Total Counts` (tie-break alphabetically).

Create exactly 5 songs from the genre pool below and use history to avoid repeats:

1. Do not repeat the same primary genre twice in one run.
2. Do not reuse titles or near-identical prompts from previous runs. Treat near-identical as >= 70% overlap of meaningful words.
3. Keep each song distinct in mood, energy, instrumentation, and arrangement.
4. Assign exactly one primary genre per song from `## Genres to Generate`.

## Prompt Rules

Each song must include:

1. One style prompt for Suno (200 characters or less).
2. One lyrics-generation prompt (200 characters or less), unless instrumental.
3. If instrumental, set lyrics prompt to `Instrumental`.
4. Character limits apply to prompt text only (not the `Prompt:` / `Lyrics Prompt:` labels).
5. Lyrics prompt must reflect the style prompt using at least two concrete style anchors (examples: mood, energy, setting, vocal delivery, rhythmic feel, era/scene tone).
6. For non-instrumentals, start lyrics prompts as: `Write lyrics for <Song Title> (<Primary Genre>): ...`

## Canonical Output Files

1. `output.md` is the report file and replaces `today.md`.
2. `genre-lists/*.md` files are the genre history files.

## Required File Updates (Strict)

### 1) Update `output.md`

Do both actions:

1. Update `## History` -> `### Total Counts` table at the top.
2. Replace the entire `## Today` section with exactly 5 new songs.

`### Total Counts` rules:

1. `## Genres to Generate` is the source of truth for the active generation pool.
2. Keep existing rows in `### Total Counts` for historical continuity, even if a genre is no longer in `## Genres to Generate`.
3. Ensure every genre in `## Genres to Generate` exists in the table (add missing ones with count `0`).
4. After updating counts, sort the entire table by `Count` (descending), then by `Genre` (alphabetically ascending).

Use this exact `## Today` entry style:

```md
### <index>. <Song Title>

Prompt: <style prompt, <= 200 chars>

Lyrics Prompt: <Write lyrics for <Song Title> (<Primary Genre>): ... <= 200 chars OR Instrumental>

Why chosen: <2-3 sentences on fit + uniqueness>
```

### 2) Append to genre history files in `genre-lists`

For each song, append to the appropriate genre file using this exact style:

```md
## <Song Title>

### Style

<style prompt>

### Lyrics

<lyrics prompt OR Instrumental>
```

If a genre file does not exist, create it with a lowercase dash-case filename (example: `drum-and-bass.md`) and this title format:

```md
# <Genre Name in Title Case>
```

Then append entries in the same style above.

## Genres to Generate

Metal, punk rock, alternative rock, EDM, dubstep, synthwave, drum and bass, electro-swing, pop-punk, industrial rock, folk metal, darkwave, chiptune rock, glitch hop, trip hop, post-punk, shoegaze

## Prompt Quality Rules

1. Keep prompts concrete and audible: mood, tempo feel, instrumentation, vocal style (or instrumental), production texture, and structure cues.
2. Avoid artist names and direct references to copyrighted songs.
3. Use a few clear constraints when useful.
4. Prioritize specificity with enough flexibility for creative variation.
5. Keep style and lyrics aligned: if the style is aggressive/minimal/dance/atmospheric, the lyrics brief should call for matching diction, pacing, and emotional intensity.
