# AGENTS.md: Rules for the "AI Agents" LLM Wiki

## Purpose
Build a wiki about **AI Agents** for a beginner who knows nothing about the topic.
The wiki is later used as the only knowledge source for a teaching HTML slideshow.

## Golden rule
**Only use information from the sources the user provides.**
- Never add facts from your own knowledge.
- If something is missing or sources disagree, write it under "Open questions / conflicts". Do not fill the gap.
- Do not create or change pages until the user has given a source and asked for an ingest.

## Folder layout
```
raw/      original source text (never edit)
wiki/     wiki pages written by the AI
  sources/  one summary page per source
```

## Page list
| Page | Purpose |
|---|---|
| `index.md` | Entry point: all pages with one-line descriptions |
| `what-is-an-ai-agent.md` | Definition in plain language |
| `agent-vs-workflow.md` | How an agent differs from a fixed pipeline or a plain chatbot |
| `agent-loop.md` | Core cycle: observe → think → act → check result → repeat |
| `tools.md` | How agents use tools (search, code, APIs) |
| `memory-and-planning.md` | How agents remember context and break tasks into steps |
| `examples.md` | Concrete real-world examples |
| `risks-and-limits.md` | Errors, cost, safety, when not to use agents |
| `glossary.md` | Short definitions of terms (LLM, tool call, prompt, etc.) |
| `sources/source-01.md` ... `source-05.md` | One summary page per ingested source |

Create a page only when a source actually supports it. Thin pages may be merged, but ask the user first.

## Page template (every concept page)
```
# Title
**Summary:** 1-2 sentences a beginner can understand.
**Key points:**
- point (Source: source-01)
- point (Source: source-02)
**Related pages:** [[page-a]], [[page-b]]
**Sources:** source-01, source-02
**Open questions / conflicts:** anything sources disagree on or don't cover
```
- Every key point must have an inline `(Source: source-XX)` tag.
- Write in plain language for a beginner.

## Linking rules
- Use `[[page-name]]` links in the "Related pages" line and inline where a term first appears.
- Every concept page links back to `index.md` and to at least two related pages.
- Concept pages cite `sources/` pages, and each source page lists which concept pages it contributed to (two-way links).

## Ingest procedure (one source at a time)
1. Summarize the source's key points to the user first.
2. Create or update the wiki pages, adding the source tag to each point.
3. Create `sources/source-XX.md` listing the concept pages it contributed to.
4. Report which pages were created or changed, and any gaps or conflicts found.

## Later steps
- **Lint:** after all 5 sources, list contradictions, untagged claims, missing links and beginner gaps. List first, fix only after approval.
- **Slides:** use only pages in `wiki/`. List the slide outline and the wiki page behind each slide before writing any HTML. Show the source wiki page at the bottom of every slide.
- **Check:** compare every slide claim against the wiki and flag anything not found there.
