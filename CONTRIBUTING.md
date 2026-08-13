# Contributing

Thanks for helping grow this. The goal is that this repo stays navigable at 10x its current size, so a few rules keep things consistent, please read before opening a PR.

## Adding a single resource (the common case)

1. **Find the right section.** Read the section's README header (prerequisites/scope) to confirm the fit. When in doubt, favor the more foundational section and cross-link.
2. **Add one line in the matching resource-type table/list**, using the standard format:
   ```
   - [Resource Title](https://link) - Level - one-line note
   ```
   For Courses/Videos, add a table row instead (see any existing section for the columns).
3. **Tag a level:** Beginner / Intermediate / Advanced. Base this on what the resource assumes, not how "important" it is.
4. **Write a real note.** "Great resource" is not a note. Say what it covers, what makes it worth including, or a caveat (e.g., "paywalled after chapter 3", "assumes PyTorch").
5. **Keep alphabetical or recency order** within a list unless the section says otherwise.

## Adding a PDF or notebook

- **PDFs:** only commit the file to `assets/pdfs/<section>/` if you have clear redistribution rights (your own notes, CC-licensed, author-permitted). Otherwise, link to the source instead of hosting a copy. Mirror the path in the section's "PDFs in this repo" list.
- **Notebooks:** same mirroring pattern under `notebooks/<section>/`. Note in the notebook's one-line description whether it runs on free-tier Colab, needs a GPU, or needs an API key.
- **Papers:** add to both the section's Papers list *and* `papers/README.md`'s running log.

## Proposing a new top-level section

New sections should be rare, most growth should happen inside existing folders. Open an issue first if you think a topic doesn't fit anywhere. A new section is justified when:

- The topic doesn't reasonably fit as a subsection of any existing folder, **and**
- You can already list at least ~8–10 real resources for it (enough to be worth a dedicated README), **and**
- It's distinct enough in prerequisites/audience to need its own difficulty framing.

If approved, copy [`templates/SECTION_README_TEMPLATE.md`](templates/SECTION_README_TEMPLATE.md) into the new folder as `README.md`, fill in every section (don't leave template placeholder text), and add the folder to the tree and the "Where do I start?" table in the root `README.md`.

## PR checklist

- [ ] Resource is in the correct section (check prerequisites, not just keyword match)
- [ ] Line follows the standard format with a real one-line note
- [ ] Difficulty level is tagged
- [ ] Link works and doesn't require a login/paywall you haven't disclosed
- [ ] If hosting a file: redistribution rights are clear
- [ ] If adding a new section: template fully filled in, root README tree + table updated

## Reporting broken links

Open an issue with the section name and the broken link, or just submit a PR removing/replacing it, small fixes don't need discussion first.
