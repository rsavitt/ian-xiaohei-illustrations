# Ian Xiaohei Illustrations (English Edition)

> Turn the judgments, processes, states, and metaphors in your English article into white-paper, hand-drawn, weird-but-clean inline illustrations.
>
> 16:9 horizontal | Xiaohei IP | pure-white hand-drawn | sparse red/orange/blue handwritten English labels | Codex Skill

> This is an English fork of [helloianneo/ian-xiaohei-illustrations](https://github.com/helloianneo/ian-xiaohei-illustrations). All prompts, references, and labels target English-language articles.

---

## What this repo is

Ian Xiaohei Illustrations is a Codex Skill that guides an AI agent to generate inline illustrations for articles, posts, blogs, Notion docs, and methodology content.

It is not a general illustration prompt and not a PPT infographic template. The core goal: first understand the cognitive anchors in the article, then turn one judgment, process, structure, state, or metaphor into a memorable 16:9 hand-drawn explainer image.

The default visual IP is "Xiaohei": a small, solid-black, white-dot-eyed, thin-legged, blank-expression creature. Xiaohei is not a mascot, not a sticker, not corner decoration — Xiaohei is an absurd worker seriously taking part in how the system runs.

In one line: **stop "adding an image" and start drawing one key cognitive action from the article.**

---

## Who this is for

A good fit if you:

- Write English articles and need inline illustrations
- Make knowledge-style content, methodology content, or AI-workflow content
- Want to turn abstract judgments into concrete metaphors
- Want something lighter, weirder, and more personally identifiable than a PPT infographic
- Use Codex for content production and want a reusable visual language

Not a fit if you want:

- Commercial illustration, brand key visuals, or polished flat illustration
- Traditional PPT infographics, complex architecture diagrams, or formal flowcharts
- Children's cartoon, cute IP, or sticker-pack style
- A single image stuffed with whole paragraphs of text or entire course pages
- Strictly editable vector source files

---

## What it produces

By default:

- 16:9 horizontal article illustrations
- A 4–8 image shot list for one article
- Per-image theme, core meaning, structure type, Xiaohei action, and suggested English labels
- Final PNGs saved to `assets/<article-slug>-illustrations/` in your workspace

Not by default:

- PPTX / PDF / Keynote
- SVG / HTML / Canvas editable artwork
- Commercial posters or cover key visuals
- Heavy-text infographics

---

## Visual style

The skill defaults to the "Xiaohei weird article illustration" style:

- Pure white background — no paper grain, beige, shadows, or gradients
- Black hand-drawn line art, thin lines, slight wobble
- Lots of white space — the main subject is only ~40%–60% of the canvas
- A few red, orange, and blue handwritten English labels
- One image expresses one core action, structure, state, or metaphor
- Xiaohei must take part in the core action — never just decoration
- Weird, creative, clean — never childish or saccharine

---

## Example outputs

These were the original Chinese-labeled examples and remain useful for style calibration (line density, white space, color restraint, Xiaohei's vibe). The labels in your new generations will be in English.

### Two breakpoints

![Two breakpoints](examples/images/01-two-breakpoints.png)

### Sort by purpose

![Sort by purpose](examples/images/02-sort-by-purpose.png)

### One fish, many uses

![One fish, many uses](examples/images/03-one-fish-many-uses.png)

### Handoff path

![Handoff path](examples/images/04-handoff-path.png)

### Information well

![Information well](examples/images/05-information-well.png)

### Idea press

![Idea press](examples/images/06-idea-press.png)

### Content fermentation

![Content fermentation](examples/images/07-content-fermentation.png)

### Trust bridge

![Trust bridge](examples/images/08-trust-bridge.png)

These are style calibration samples, not composition templates. Always reinvent the metaphor from the current article — do not copy the objects or compositions from old examples.

---

## Install

Clone the repo:

```bash
git clone https://github.com/rsavitt/ian-xiaohei-illustrations.git
cd ian-xiaohei-illustrations
```

Copy the skill into the Codex skills directory:

```bash
mkdir -p "${CODEX_HOME:-$HOME/.codex}/skills"
cp -R ./ian-xiaohei-illustrations "${CODEX_HOME:-$HOME/.codex}/skills/"
```

Then in Codex:

```text
Use $ian-xiaohei-illustrations Design and generate 5 Xiaohei-style article illustrations for this article.
```

---

## Usage

### Planning only

```text
Use $ian-xiaohei-illustrations Don't generate images yet.
Analyze the article below and produce a shot list of ~5 illustrations.
For each: which paragraph it goes after, theme, core meaning, structure type, what Xiaohei is doing, suggested English labels.

<paste article>
```

### Generate inline illustrations directly

```text
Use $ian-xiaohei-illustrations Generate 4 Xiaohei-style article illustrations for the article below.
16:9 horizontal, pure white background, black hand-drawn line art, a few red/orange/blue handwritten English labels.

<paste article>
```

### Single-concept image

```text
Use $ian-xiaohei-illustrations Generate one inline illustration for "Trust isn't something you shout — it's laid down one piece of evidence at a time."
The image should be weird but clean. Xiaohei must carry the core action.
```

### Edit out a title or typo

```text
Use $ian-xiaohei-illustrations Edit this image. Remove the "Flowchart" title in the top-left. Leave everything else unchanged.
```

More in [examples/prompts.md](examples/prompts.md).

---

## Pipeline

1. Read the article, Markdown, Notion content, screenshot, or user-supplied theme
2. Extract core points, cognitive shifts, process structure, and paragraphs that suit visualization
3. Output a shot list — one cognitive anchor per image
4. Pick a structure type per image: Workflow, System slice, Before/after, Character state, Concept metaphor, Method layering, Map route, or Mini-comic frames
5. Reinvent a low-tech, weird-but-coherent physical metaphor
6. Make Xiaohei carry the core action
7. Generate each image independently with the image model
8. Run the QA checklist — white background, white space, Xiaohei's action, English labels, non-PPT feel, non-copy of old examples
9. Save final PNGs and report usage and paths

---

## Directory structure

```text
.
├── README.md
├── LICENSE
├── NOTICE.md
├── assets/
│   └── ian-wechat-qr.jpg
├── examples/
│   ├── images/
│   │   ├── 01-two-breakpoints.png
│   │   ├── 02-sort-by-purpose.png
│   │   └── ...
│   └── prompts.md
└── ian-xiaohei-illustrations/
    ├── SKILL.md
    ├── agents/
    │   └── openai.yaml
    ├── assets/
    │   └── examples/
    └── references/
        ├── style-dna.md
        ├── xiaohei-ip.md
        ├── composition-patterns.md
        ├── prompt-template.md
        └── qa-checklist.md
```

The subdirectory installed into Codex is:

```text
ian-xiaohei-illustrations/
```

The root README, LICENSE, NOTICE, and examples are GitHub-facing docs.

---

## Notes

- Shorter labels are more stable than long ones.
- One image expresses one core structure — don't turn the article into a manual.
- Xiaohei must carry the core action; if removing Xiaohei leaves the image intact, Xiaohei was decoration.
- The example images are for calibrating line density, white space, color restraint, and Xiaohei's participation — never for copying composition.
- AI image models can drop typos, hallucinated labels, style drift, or stray titles — check every output.
- If there are many typos, regenerate with fewer labels.

---

## About the original author

This is an English fork. The original Chinese skill is by:

**Ian** — product designer / one-person company / AI builder

- GitHub: [helloianneo](https://github.com/helloianneo)
- X/Twitter: [@ianneo_ai](https://x.com/ianneo_ai)
- Site: [www.ianneo.xyz](https://www.ianneo.xyz)

---

## License

MIT License. See [LICENSE](LICENSE).
