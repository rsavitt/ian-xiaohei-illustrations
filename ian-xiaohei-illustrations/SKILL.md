---
name: ian-xiaohei-illustrations
description: Generate Ian-style English article illustrations. Use when the user asks for "weird", "Xiaohei", "hand-drawn", "article illustrations", "blog illustrations", "post illustrations", "illustration suggestions", "shot list", "remove title / edit image" tasks for English articles, posts, blogs, Notion docs, workflow docs, methodologies, processes, structures, states, metaphors or opinions. Defaults to the Xiaohei IP, pure-white hand-drawn line art, a few red/orange/blue annotations, and a clean but bizarre visual style.
---

# Ian Xiaohei Bizarre Article Illustrations

## Core positioning

Design and generate 16:9 horizontal article illustrations for English articles. The goal is not commercial illustration, PPT infographics, or cute cartoons — it is to turn the key judgments, processes, structures, states, or metaphors in the article into one clean, weird, creative, readable but non-textbook hand-drawn explainer image.

The default visual IP is "Xiaohei": solid black, white dot eyes, thin legs, blank expression, seriously doing one absurd-but-coherent thing. Xiaohei must take part in the core action of the image — never just stand around as decoration.

## Read these references first

Load on demand — don't stuff the context all at once:

- `references/style-dna.md`: style DNA, colors, text, taboos.
- `references/xiaohei-ip.md`: Xiaohei's appearance, personality, action library, and taboos.
- `references/composition-patterns.md`: structure types, original-metaphor method, and anti-copy rules.
- `references/prompt-template.md`: single-image prompt template.
- `references/qa-checklist.md`: post-generation checks and iteration rules.
- `assets/examples/`: low-frequency visual calibration only; do not enter the default generation path. Do not copy these examples' compositions, objects, or labels.

## Workflow

### 1. Digest the article

First read the article, link, Notion page, Markdown file, or screenshot the user gives you. Extract:

- What the core point is
- Which paragraphs carry a cognitive shift
- Which content suits visual explanation
- Which parts only suit text, no image needed

Don't space illustrations evenly. Prioritize "cognitive anchors" — e.g.: core judgments, two breakpoints, input/output loops, splits, before/after contrasts, one-fish-many-uses, handoff paths, common pits, character state changes.

### 2. Output illustration strategy first

If the user just says "analyze where this needs illustrations / think about which parts need images," give a shot list first. For each image, write clearly:

- Which paragraph it goes after
- The image's theme
- Core meaning
- Structure type
- What Xiaohei is doing in the image
- Suggested elements
- Suggested English handwritten labels

Default 4–8 images. For short articles, 1–3; long articles still shouldn't easily exceed 9. Enough is enough — don't turn the article into a picture book.

### 3. Single image generation

If the user explicitly asks "generate / output / make image / generate for me," don't stop to confirm; use the built-in `image_gen` to generate each one separately. Do not splice multiple images into one.

Each image explains only one core structure. The prompt must include:

- 16:9 horizontal English article illustration
- Pure white background
- Black hand-drawn line art
- A few red/orange/blue handwritten English labels
- Lots of white space
- Xiaohei as the core action subject
- No PPT, commercial illustration, childish cuteness, complex architecture, or top-left type titles

Do not reproduce past cases. Examples only provide style density and Xiaohei-participation patterns — never directly reuse existing compositions like "conveyor breakpoints / Xiaohei pulling a lever / material fish / stamp toolbox / common-pit path," unless the user explicitly asks for a reproduction. Reinvent a weird-but-coherent metaphor from the current article every time.

### 4. Check and iterate

After generating, check `references/qa-checklist.md`. If any of the following appear, regenerate or partially edit first:

- Xiaohei is just decoration
- Canvas too full
- Looks too much like a flowchart/PPT
- Too much English text, or many typos
- Titles like "common pits / flowchart / system architecture" in the top-left
- Style too cute, childish, or stiff
- Background isn't clean white

### 5. Save and deliver

If the user is working inside a workspace, copy final images to:

```text
assets/<article-slug>-illustrations/
```

Name in order:

```text
01-topic-name.png
02-topic-name.png
```

Keep the original generated files. Do not overwrite existing assets unless the user explicitly asks for replacement.

## Output discipline

Pre-generation strategy output should be short and precise. Post-generation delivery should include:

- How many images were generated
- What each image is for
- Save paths
- Which images are the most solid, which are optional

Don't give long lectures on style theory — let the images speak.
