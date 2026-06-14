# PPT Workflow · 橙线 PPT

Turn any article or talk outline into a polished HTML slide deck, each slide
illustrated with an orange-line story scene.

The key difference from standalone illustrations: PPT illustrations depict
**the actual scenes described in the source text** (a person at a computer,
a team around a table, a broken spaceship), not abstract metaphors. The
story is the illustration.

## Workflow

### Step 0 — Define the character style for this deck

Before generating any illustration, establish the human figure style that
will be used consistently throughout this deck.

**Default: 小橙.** Unless the user requests a different style, use 小橙 as
the recurring character. 小橙's prompt block:

```
Character design: 小橙, a tiny minimalist line-drawn figure. Circle head
(outline only, not filled), two small black dot eyes, no mouth. Narrow
rectangular body made of a few straight black lines (outline only, no
fill). Thin wobbly stick arms and stick legs. One small solid orange dot
(#F97316) on the chest like a badge — this is the ONLY color on the
character. Geometric, clean, hand-drawn. Not cute, not cartoon.
```

When using 小橙, skip the candidate generation step and use this block
verbatim in every illustration prompt.

**Custom character:** If the user wants a different figure style, generate
a single image with **4 candidate figures** side by side — each with a
distinct style (e.g. rounder head, angular torso, different arm/hand
treatment, varying expressiveness). Label them A / B / C / D with a short
descriptor below each.

Present to the user and ask them to pick one — or describe tweaks. Once
confirmed, write out a precise character prompt block (20–40 words) that
will be copy-pasted verbatim in every subsequent illustration prompt.

Do not skip this step. A deck where figures look different on every slide
feels amateurish — one confirmation pass here prevents many regeneration
passes later.

### Step 1 — Read the source

Read the article or outline carefully. Identify:
- The main narrative arc (what's the talk about, what's the conclusion)
- The individual **story moments** — specific events, people, conversations,
  numbers, comparisons. These become slides.
- The total speaking time (target: 1.5–2 min per slide)

### Step 2 — Write the outline, confirm before drawing

Produce a slide-by-slide outline in a table:

| # | Left-top title (big text) | What this slide says | Illustration scene |
|---|---|---|---|

Each illustration scene should describe a **concrete, observable moment**:
who is doing what, where, with what objects. No abstract symbols.

**Stop here and confirm with the user before generating any images.**
One round of outline feedback saves many rounds of image regeneration.

### Step 3 — Rename images immediately after generation

This is the most important operational rule.

After every image generation call, immediately rename the output file to a
descriptive name:

```
slide-01-cover.png
slide-02-forum-workarounds.png
slide-08-mrr-launch.png
```

Do this before writing any HTML. Cryptic generated filenames make it
impossible to track which image belongs to which slide.

### Step 4 — Generate illustrations in parallel

Generate all slides in one parallel batch. For each slide, generate 2
candidates (prompt A and prompt B with slightly different scene framing).

Follow the style rules:
- Thin black ink lines on pure white, generous negative space
- Single orange accent `#F97316` on the most meaningful element
- TINY human figures dwarfed by the scene
- Direct story scene, not a metaphor

**After each batch completes, rename all files immediately** (see Step 3).

Prompt template per slide:

```
New Yorker magazine style editorial illustration, single-panel.
Minimalist thin black ink line drawing on pure white background,
generous negative space, no shading, no gradients, only one accent
color: warm orange #F97316.
Scene: [CONCRETE SCENE — who does what, what is orange and why,
spatial layout, scale contrast].
Witty, restrained, intelligent.
In the bottom-left corner: a short horizontal orange line, and below it
one small light-gray Chinese caption: "[KEY LINE]" — small, quiet,
perfectly legible. No other text anywhere.
```

Use 16:9 ratio for all slides.

### Step 5 — Let the user pick

Present each pair as:

**场景N — [title]**

**NA**
![NA](slide-N-xxx-A.png)

**NB**
![NB](slide-N-xxx-B.png)

Show all pairs at once. The user picks A or B for each scene. Do not
pre-select for the user.

### Step 6 — Build the HTML

After the user confirms their picks, build a single self-contained HTML file.

**Layout per slide:**
- Pure white background
- Top-left: large serif title (`Songti SC` / `STSong` / `SimSun` fallback),
  bold, ~3.8vw, padding ~3.5% top / 5% left
- Center area: illustration image, `object-fit: contain`, fills remaining space
- Cover slide: full-bleed image only (no separate title bar). Add an author
  credit in small orange serif text, bottom-center, absolutely positioned:
  `color: #F97316`, `font-size: ~1.4vw`, `letter-spacing: 0.12em`.
- Thank You slide: centered serif text + orange underline, no image needed

**Navigation (bottom-right corner):**
- Pixel-style `◀` / `▶` triangles, `Courier New` monospace
- Orange `#F97316`, no transparency, no circles or borders
- Counter format: `01/17`
- Keyboard: ← → ↑ ↓ arrow keys
- Mouse: click left half = back, click right half = forward
- Scroll wheel with 400ms debounce
- Touch swipe (horizontal and vertical)

**Progress bar:** 3px orange line at very bottom, width = progress %

**Animation:** subtle `translateX` fade on slide change (28ms, direction-aware)

Save the HTML alongside the images so relative `src` paths work directly.

### Step 7 — Clean up

After the user confirms the final HTML, trash all unused candidate images.
Keep only the images actually referenced in the HTML.

## Slide structure recommendation

For a 25-minute talk (≈14 content slides):

1. Cover — article title, full-bleed image
2–N. One slide per story moment or key point
Last. "Thank You" — white, large serif text, orange line below

Aim for 1.5–2 min per slide. If the source has many sections, group minor
points onto one slide rather than making 30 slides.

## Common mistakes to avoid

- **Skipping the character style step** — inconsistent figures across slides.
- **Generating images before confirming the outline** — expensive rework.
- **Skipping the rename step** — causes slide/image mismatches.
- **Metaphor illustrations** — PPT shows the story, not symbols.
- **Showing images one pair at a time** — show all pairs at once.
- **Pre-selecting images for the user** — the user has taste; let them choose.
