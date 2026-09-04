# BookGraph

Marco's personal knowledge graph of books, built in Obsidian. Plain Markdown files, linked with `[[wikilinks]]`, visualized via Obsidian's graph view.

## Structure

- `books/` — one note per book finished. Template: `templates/book-template.md`.
- `concepts/` — one note per idea/theme that recurs or matters enough to be its own node. Template: `templates/concept-template.md`.
- Books link to concepts, not directly to other books. Two books share an idea by both linking to the same concept note — that's what makes the graph meaningful instead of a pile of isolated book pages.

## The loop

1. **Mid-book**: Marco jots raw one-line notes into that book's `# Raw notes` section (usually from his phone). No linking, no structure — just capture. Don't touch this section unless asked.
2. **On finishing a book**: Marco runs an "exam" ritual elsewhere (separate Claude chat) — comprehension + essay questions, including connections to books already in the vault — and answers them himself. He pastes the questions and his own answers into the `# Exam` section.
3. **Extraction (this is the job done inside the vault)**: given a finished book note with raw notes + exam filled in, create/update concept notes in `concepts/` for the ideas that came up, link them from the book note's `# Concepts extracted` section, and link related concepts to each other. Also check existing concept notes for connections to this book — the whole point is surfacing links to prior reading, not just filing new ones in isolation.

## Rules

- **Never write exam answers for Marco.** The exam is how he tests his own understanding; if Claude fills it in, the graph stops reflecting what he actually knows. Claude's job is structuring and linking what he already wrote, and asking clarifying questions if his notes are ambiguous, not generating the content.
- Concept notes are named for the idea, not the book (`the-ship-of-theseus-problem.md`, not `mortality-in-book-x.md`) — that's what lets multiple books converge on one node.
- Prefer a small number of well-connected concept notes over many thin ones. Before creating a new concept, check `concepts/` for something close enough to reuse or link instead.
- Don't invent connections that aren't in Marco's own notes/answers — flag a possible connection as a question rather than asserting it as a link, unless it's clearly what he meant.
- Keep frontmatter (title/author/date_finished/rating) filled in on book notes; it's used for Obsidian queries later.
