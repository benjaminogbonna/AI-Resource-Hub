# AI Resource Hub

A single, growing map of the best free and paid resources for learning AI, from "what is a neuron" to reading frontier papers. Organized so a complete beginner and a working researcher can both find what they need in under a minute.

- **For learners:** stop hunting across 20 tabs. Pick a section, pick your level, go.
- **For contributors:** every section follows the same format, so adding a resource is a 2-minute PR, not a redesign.

---

## How this repo is organized

```
AI-Resource-Hub/
├── README.md                          ← you are here
├── CONTRIBUTING.md                    ← how to contribute, add resources / new sections
├── templates/
│   └── SECTION_README_TEMPLATE.md     ← the format every section follows
│
├── 00-start-here/                     ← learning paths by persona & goal
├── 01-math-and-statistics/            ← linear algebra, calculus, probability, stats
├── 02-ai-fundamentals/                ← what is AI, history, core concepts, ethics
├── 03-machine-learning/               ← classical ML: regression → trees → SVMs → ensembles
├── 04-deep-learning/                  ← neural nets, CNNs, RNNs, transformers, training
├── 05-large-language-models/          ← LLM architecture, training, fine-tuning, prompting
├── 06-ai-agents/                      ← agentic systems, tool use, planning, multi-agent
├── 07-retrieval-augmented-generation/ ← RAG, embeddings, vector DBs, retrieval
├── 08-image-models/                   ← CV, diffusion, GANs, vision-language models
├── 09-video-models/                   ← video generation, understanding, world models
├── 10-speech-and-audio-models/        ← ASR (STT), TTS, audio generation, music models
├── 11-mlops-and-deployment/           ← serving, monitoring, infra, edge inference
├── 12-tools-and-frameworks/           ← PyTorch, TensorFlow, JAX, HF, LangChain, etc. (cross-cutting)
│
├── notebooks/                         ← runnable notebooks, mirrored by section
├── papers/                            ← running log of notable papers, cross-topic
└── assets/pdfs/                       ← PDFs, mirrored by section
```

**Why numbered prefixes?** They encode a rough learning order (math → fundamentals → ML → deep learning → specializations) while still sorting correctly in any file browser or GitHub's UI. You don't have to go in order, jump straight to `06-ai-agents` if that's what you need, but the order is there if you want a path.

**Why folders instead of one giant README?** Because "comprehensive" and "navigable" are in tension past a certain size. Splitting by topic means:
- Each section README stays short enough to actually scan.
- You can deep-link to `05-large-language-models#fine-tuning` instead of a 3,000-line file.
- New sections don't require restructuring old ones.

---

## Where do I start?

| I am... | Go to |
|---|---|
| A complete beginner, no coding/math background yet | [`00-start-here`](00-start-here/) → [`01-math-and-statistics`](01-math-and-statistics/) → [`02-ai-fundamentals`](02-ai-fundamentals/) |
| A developer who wants to build with AI (not research it) | [`00-start-here`](00-start-here/) → [`05-large-language-models`](05-large-language-models/) → [`07-retrieval-augmented-generation`](07-retrieval-augmented-generation/) → [`06-ai-agents`](06-ai-agents/) |
| Comfortable with Python, new to ML | [`03-machine-learning`](03-machine-learning/) → [`04-deep-learning`](04-deep-learning/) |
| Interested in generative media (images/video/audio) | [`08-image-models`](08-image-models/) / [`09-video-models`](09-video-models/) / [`10-speech-and-audio-models`](10-speech-and-audio-models/) |
| Already deep in ML, want to specialize or go to production | [`11-mlops-and-deployment`](11-mlops-and-deployment/), or jump to any Advanced tagged resource |
| Just want a working knowledge of AI, no coding | [`00-start-here`](00-start-here/) → [`02-ai-fundamentals`](02-ai-fundamentals/) |

Every folder has its own `README.md` with the same structure (see below), so once you've read one, you know how to read all of them.

---

## The standard section format

Every topic folder, and every future ones added follows [`templates/SECTION_README_TEMPLATE.md`](templates/SECTION_README_TEMPLATE.md):

1. **Header:** what the section covers, prerequisites, related sections.
2. **"How to use this folder:"** a short pointer for where to actually start.
3. **Resource tables:** grouped by type, not by sub-topic:
   - Courses
   - Videos & Talks
   - Articles & Blog Posts
   - Papers
   - Books
   - Notebooks & Code
   - Repos & Tools
   - PDFs in this repo
4. **"What's next:"** the logical follow-on section.

Grouping by resource type (not sub-topic) is deliberate: it means "I want a video, not an article" is always answerable by scanning one part of the page, regardless of which section you're in.

### Difficulty tags

Every single resource is tagged, not just the section:

- **Beginner:** no prior knowledge in this section needed.
- **Intermediate:** assumes the section's stated prerequisites.
- **Advanced:** research-level or assumes strong fluency already.

### Resource line format

```
- [Resource Title](https://link) - Level - one-line note on what it's good for / why it's here
```

Tables are used for Courses and Videos (extra columns like provider/cost are useful there); plain bullet lists are used for Articles, Books, Repos, and PDFs to keep additions fast.

---

## Notebooks, Papers, and PDFs - the shared folders

Three resource types get their own top-level folder *in addition to* being linked from their topic section, because they behave differently:

- **`notebooks/`** - mirrors the section structure (`notebooks/05-large-language-models/...`). A section README links to the notebook; the notebook itself lives here so it's easy to `git clone` and run everything at once.
- **`papers/`** - a single running log of notable papers across *all* topics, in reverse-chronological order, in addition to being cited in their relevant section. Good for "what came out recently across the whole field."
- **`assets/pdfs/`** - same mirroring pattern as notebooks. **Only for PDFs you have the right to redistribute** (arXiv preprints, your own notes, CC-licensed material). Everything else gets linked to, not hosted, see [CONTRIBUTING.md](CONTRIBUTING.md).

---

## Design principles (read this before restructuring anything)

1. **One resource, one home.** A resource lives in exactly one section's README. If it's genuinely cross-cutting (e.g., a course covering both RAG and agents), it goes in the more foundational section and gets a cross-link from the other.
2. **Type before topic, inside a section.** Sub-organizing by resource type (not sub-topic) keeps sections skimmable without deep nesting.
3. **Numbered top-level, unnumbered inside.** Top-level folders are numbered for a rough path; files inside a section aren't, since section order rarely matters as much.
4. **Every resource is tagged and annotated.** No bare links. A link with no note or level is a link nobody will click.
5. **Prefer linking over hosting.** Only host a file (PDF/notebook) when redistribution rights are clear or it's original content. Default to linking.
6. **New top-level section = last resort.** Before creating one, check whether the resource fits an existing section. Repo growth should mostly happen *inside* folders, not by multiplying them, see [CONTRIBUTING.md](CONTRIBUTING.md) for the bar.

---

## Contributing

Contributions are welcome. 
Adding a resource takes minutes. See [CONTRIBUTING.md](CONTRIBUTING.md) for the full guide, including:
- How to pick the right section (and when a new one is justified)
- The exact line format and difficulty-tagging rules
- Rules for hosting PDFs/notebooks vs. linking out
- PR checklist

---

## Status

This repo is actively growing. Sections currently have placeholder READMEs seeded from the template, check each folder's "Last updated" line at the bottom of its README for freshness. Contributions and resource suggestions (via issues or PRs) are welcome.

---

*Maintained as a living reference. If a link breaks, please open an issue or PR rather than silently working around it, broken links are the #1 way resource repos rot.*
