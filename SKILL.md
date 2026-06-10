---
name: orange-line-illustration
description: >
  Generate New Yorker-style minimalist editorial illustrations — thin black
  ink lines on white, vast negative space, a single orange accent (#F97316) —
  for articles, principles, covers, and concept visuals. Use when the user
  asks for 配图, 插图, 封面图, editorial illustrations, concept/metaphor
  illustrations, article covers, 公众号配图, principle/maxim illustrations,
  or mentions "橙线风格" / "orange line style" / "纽约客风格插图". Works with
  any image generation tool that accepts text prompts.
metadata:
  category: creative
  author: 橘子 (Orange) & Cola
license: See LICENSE.md — free for open-source & personal use; commercial
  license required for closed-source commercial use.
---

# Orange Line Illustration · 橙线插画

A complete style system for generating elegant, conceptual editorial
illustrations. Born from a real workflow: illustrating "六条与 AI 一起做产品
的原则" (Six Principles for Building Products with AI). The style's soul:
**one idea, one accent, lots of silence.**

## The Style (non-negotiable core)

Every image follows these rules. They are what make a set of images feel
like one voice — consistency is the whole point.

- **Line**: thin black ink lines, hand-drawn editorial feel (think New
  Yorker single-panel cartoons). No shading, no gradients, no fills except
  the accent.
- **Background**: pure white. Generous negative space — emptiness is part
  of the composition, not wasted space.
- **Accent**: exactly ONE color — warm orange `#F97316`. Use it on the
  single most meaningful element (the thing the viewer should understand).
  If everything is orange, nothing is.
- **Figures**: small, simple, hand-drawn humans/robots. Never photorealistic.
- **Mood**: witty, restrained, intelligent. The image should make the
  viewer think for one second, then smile.

## Designing the Metaphor (do this before any generation)

The metaphor is the product; the rendering is just execution. Spend the
thinking here.

1. **Extract the tension.** Good concept illustrations express a pair of
   opposites: many vs. one, hollow vs. warm, generated vs. judged. Find the
   tension in the content first.
2. **Prefer action scenes over abstract symbols.** A person handing a cup
   of warm tea beats floating speech bubbles. A figure tripping on one
   inconsistent stair beats a row of doors with one odd handle. Field-tested:
   abstract juxtapositions confuse readers; small human actions land
   instantly. If the metaphor needs explaining, it failed.
3. **One idea per image.** If the sketch needs two sentences to describe
   its point, cut one.
4. **Place the orange deliberately.** The orange element answers: "what is
   this image about?" — the kept button, the warm steam, the inconsistent
   step, the refined line.

## Prompt Template

Compose prompts from this skeleton (adjust the scene, keep everything else):

```
New Yorker magazine style editorial illustration, single-panel conceptual
metaphor. Minimalist thin black ink line drawing on pure white background,
generous negative space, no shading, no gradients, only one accent color:
warm orange #F97316. Scene: [YOUR SCENE — describe the action, the
characters, what is orange and why]. Witty, restrained, intelligent.
[CAPTION BLOCK — see below]. No other text anywhere.
```

Scene-writing tips learned the hard way:

- Describe **who does what to whom** with spatial directions (left/right/
  middle). Vague spatial relations produce split, disconnected scenes.
- Add explicit negative constraints when geometry matters: "plain side
  view, NOT Escher-like, no impossible geometry" — image models love to
  get creative with stairs and architecture.
- For continuous lines: "one single CONTINUOUS unbroken smooth line, never
  breaking" — otherwise lines fracture.

## Caption & Title System

**Interior images (3:2 landscape)** carry a quiet signature in the
bottom-left corner:

```
In the bottom-left corner: a short horizontal orange line, and below it
one small light-gray Chinese caption in a clean sans-serif font:
"[THE PRINCIPLE / KEY SENTENCE]" — small, quiet, unobtrusive, perfectly
legible.
```

Same corner, same style, every image — the signature position itself
demonstrates consistency.

**Covers (21:9 ultra-wide)** make the title the anchor:

```
The Chinese title "[TITLE]" in clean dark-gray sans-serif typography,
placed in the [upper-left / centered upper] area, medium size, elegant,
perfectly legible.
```

Keep the illustration in the lower portion, breathing room around the
title.

## Workflow: 抽卡, not 检查 (gacha, not QA)

Generation is cheap; AI self-inspection is expensive and adds little.
The human's taste is the quality gate.

1. Design metaphor candidates — for covers, prepare ~5 distinct directions
   in one batch.
2. Generate all candidates in parallel. One generation per metaphor.
3. Present everything to the human. Let them pick. Do not pre-filter with
   image analysis unless the human explicitly asks.
4. When the human says "this metaphor but not quite" — regenerate with a
   sharpened prompt (add the missing spatial/negative constraints), don't
   abandon the metaphor.
5. Rename outputs descriptively (e.g. `01-放大器.png`, `封面E-走过草稿.png`)
   so the set stays navigable.

## Reference: a field-tested set

The style was proven on six principle illustrations + one cover. The
chosen cover metaphor ("walking through the draft": a figure walks along
a line — ahead of them messy black scribble, behind them the same line
refined into clean orange) captures the spirit of the whole style: human
judgment walking through AI's rough output, leaving refinement behind.

Metaphors that worked: erasing a wall of buttons down to one; a conveyor
of identical bottles with one hand-painted; completing the last arc of a
nearly-finished circle; handing warm tea beside a robot's hollow bouquet;
tripping on the one inconsistent stair.

Metaphors that failed (and why): ornate empty speech bubbles (too
abstract), a row of doors with one odd handle (no action, no consequence),
Escher staircases (model over-creativity — constrain geometry explicitly).
