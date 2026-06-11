# Orange Line Illustration · 橙线插画

[中文](README.md) | **English**

> One idea, one accent, lots of silence.
> 一个想法，一抹橙色，大量留白。

A complete style system (packaged as an AI agent **skill**) for generating
New Yorker-style minimalist editorial illustrations: thin black ink lines
on pure white, vast negative space, and a single warm-orange accent
(`#F97316`) placed exactly where the meaning lives.

Born from a real workflow — illustrating *Six Principles for Building
Products with AI* (《与 AI 一起做产品的六条原则》).

![cover example](examples/cover-walking-through-the-draft.png)

## What's inside

- **The style spec** — line, background, accent, figures, mood. The rules
  that make a whole set of images feel like one voice.
- **Metaphor design method** — how to find the visual tension, why action
  scenes beat abstract symbols (field-tested, with failure cases).
- **Prompt template** — a battle-tested skeleton for any image model that
  accepts text prompts.
- **Caption & title system** — the quiet bottom-left signature for interior
  images, the title-anchored layout for covers.
- **The gacha workflow** — generation is cheap, AI self-inspection is
  expensive; batch candidates, let the human pick.

## Examples

| | |
|---|---|
| ![](examples/01-amplifier.png) | ![](examples/02-subtraction.png) |

Note the scale: the person is always **tiny**, the object monumental.
That disproportion is the signature drama of the style.

## Install

Works with any AI agent that supports the SKILL.md convention
(Cola, Claude Code, Codex, etc.). Drop the directory into your agent's
skill folder, e.g.:

```
~/.cola/skills/orange-line-illustration/
```

Then just ask your agent for illustrations — "three orange-line style
illustrations for this article" — and it will follow the spec.

## License

**Dual license**: free for open-source & personal use; commercial license
required for closed-source / proprietary use. See [LICENSE.md](LICENSE.md).
