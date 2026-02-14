# Music Library Prompt

## Purpose

Generate 5 new Suno-ready songs per run that match my taste while still exploring fun variations.

## Task

I am using Suno simple creation mode. Create exactly 5 songs from the genre pool below.

Use my history files (ratings, notes, and prior prompts) to avoid repeats and improve quality:

1. Do not repeat the same primary genre twice in one run.
2. Do not reuse titles, core hooks, or near-identical style prompts from previous runs.
3. Prefer genre blends (about 70/30 or 60/40) to keep songs fresh.
4. Balance safety + exploration:
   - 3 songs should be in proven favorite areas.
   - 2 songs should be experimental but still adjacent to my taste.

Then update the outputs:

1. Update the genre table counts.
2. Update any relevant genre/history files with the new prompts.
3. Replace `today.md` with today's 5 prompts.

## Output Format (for each of the 5 songs)

For each song, return:

1. Title
2. Primary genre + secondary influence
3. Style prompt (paste-ready for Suno)
4. Short lyrics concept (2-3 sentences)
5. Why it fits my taste (1 sentence)

## Genres I Like

Metal, punk rock, alternative rock, EDM, dubstep, synthwave, drum and bass, electro-swing, pop-punk, industrial rock, folk metal, darkwave, chiptune rock, glitch hop

## Prompt Quality Rules

1. Keep each style prompt specific, vivid, and concise (around 20-50 words).
2. Avoid artist names and direct references to copyrighted songs.
3. Include energy, mood, tempo feel, and key instrumentation in each style prompt.
4. Keep songs distinct from each other in groove, sonic texture, and vocal style.

## Genre Table

| Genre | number of songs |
|---|---|

