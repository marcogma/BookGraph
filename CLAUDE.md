# BookGraph

Marco's personal knowledge graph of books, built in Obsidian. Plain Markdown files, linked with `[[wikilinks]]`, visualized via Obsidian's graph view.

## Structure

- `books/` — one note per book finished. Template: `templates/book-template.md`.
- `concepts/` — one note per idea/theme that recurs or matters enough to be its own node. Template: `templates/concept-template.md`.
- Books link to concepts, not directly to other books. Two books share an idea by both linking to the same concept note — that's what makes the graph meaningful instead of a pile of isolated book pages.

## The loop

1. **Mid-book**: Marco jots raw one-line notes into that book's `# Raw notes` section (usually from his phone). No linking, no structure — just capture. Don't touch this section unless asked.
2. **On finishing a book**: either Marco runs an "exam" ritual elsewhere and pastes the transcript in for extraction, or — going forward — the `literary-book-exam` skill (`~/.claude/skills/literary-book-exam/`) runs the exam live in a Claude Code session and writes the note directly. Both paths produce the same shape of note.
3. **Extraction/writing**: rewrite Marco's answers into the book note's `# Notes` section as **first-person reflective prose in his own voice — not a Q&A/dialogue transcript.** Keep his own words and ideas, fixing only grammar, and fold in the understanding he arrived at during the exam (corrections he accepted, connections he made, ideas that clicked) as his own synthesized notes — never attributed as "Claude said" or presented as dialogue. Then create/update concept notes in `concepts/` for the ideas that came up, link them from `# Concepts extracted`, and link related concepts to each other. Check existing concept notes for connections to this book — the whole point is surfacing links to prior reading, not just filing new ones in isolation.

## Rules

- **Never write exam answers for Marco in `# Notes`.** The exam is how he tests his own understanding; if Claude invents the substance, the graph stops reflecting what he actually knows. Claude's job is rephrasing/structuring what he already thought and said — correcting grammar, smoothing it into notes — never adding ideas he didn't have.
- **`# Notes` reads like Marco's own journal, not a transcript.** No "Q:", no "Claude:", no back-and-forth. When a correction or idea came from the exam dialogue, absorb it into his voice (e.g. "I initially read it as X, but realized Y") rather than narrating who said what.
- **`# Historical & cultural context`, `# Summary`, and `# Main characters` are the deliberate exceptions** to the rule above — reference material Claude writes directly and factually (author biography, historical/literary context, plot/argument summary, who's who), not Marco's interpretation. `# Summary` and `# Main characters` exist specifically so Marco can re-orient himself in a book he read a while ago and has started forgetting the details of — write them for that purpose: `# Summary` can and should include the ending (it's a memory aid, not a spoiler-free teaser), and `# Main characters` should be enough to place a name instantly (**Name** — one line on who they are and their role), adapted to "key figures/terms" or omitted for a non-narrative work like a philosophical treatise. Keep all three out of `# Notes` and don't blur them — the whole value of the split is that a reader can trust `# Notes` is really his.
- Concept notes are named for the idea, not the book (`the-ship-of-theseus-problem.md`, not `mortality-in-book-x.md`) — that's what lets multiple books converge on one node.
- Prefer a small number of well-connected concept notes over many thin ones, but don't over-correct into flattening every new idea into the existing hubs — a batch extraction once did this (nearly everything got tagged `need-to-be-witnessed` / `freedom-as-capacity-to-refuse` instead of minting new concepts), and it made the graph feel repetitive rather than genuinely connected. Before creating a new concept, check `concepts/` for something that's actually the same idea, not just loosely adjacent.
- Don't invent connections that aren't in Marco's own notes/answers — flag a possible connection as a question rather than asserting it as a link, unless it's clearly what he meant. (This restriction is about *his* interpretive connections — it doesn't apply to `# Historical & cultural context`, which is expected to bring in outside information.)
- Keep frontmatter (title/author/date_finished/rating) filled in on book notes; it's used for Obsidian queries later.
