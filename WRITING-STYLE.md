# Writing style

Rules for every Markdown file Claude writes or edits in this vault. The goal: notes that read like a person wrote them, not a chatbot.

Sources: Wikipedia's [Signs of AI writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing) guide (WikiProject AI Cleanup), the [humanizer](https://github.com/blader/humanizer) and [avoid-ai-writing](https://github.com/conorbronsdon/avoid-ai-writing) skills, and a scan of this vault's own notes (September 2026). The examples marked *from the vault* are real sentences that broke these rules.

## 1. Punctuation

- **No em dashes (—) and no en dashes used as dashes (–).** The vault had 473 of them, about 26 per 1,000 words. A human writer uses maybe one. Replace each with a period, comma, colon, or parentheses. Most of the time the right fix is two sentences.
  - *From the vault:* "It reminded me of Sade's Justine — everything bad happens to her precisely because she stays virtuous."
  - *Better:* "It reminded me of Sade's Justine: everything bad happens to her because she stays virtuous."
- En dashes in number ranges (`1849–1859`) and hyphens in compound words (`self-destructive`) are fine.
- In lists, separate a name from its description with a colon: `**Myshkin**: the protagonist...`, `[[the-idiot]]: one line...`.
- Straight quotes. No emojis. No arrows (→) in prose.

## 2. Sentence patterns

**"Isn't X, it's Y" reversals.** The most common tic in the vault after dashes. Knocking down a reading nobody proposed and then giving the "real" one sounds deep but usually adds nothing. State Y directly. Keep the contrast only when X is a reading someone actually held, usually Marco himself ("I first read it as X").
- *From the vault:* "The real turning point isn't the duel, it's the final scene."
- *Better:* "The turning point is the final scene."
- Also watch for: "not just X, but Y", "not only... but also", "that isn't living at all, it's...", "not as X, but as Y".

**Punchy closers and aphorisms.** A short line at the end of a paragraph that restates it with extra drama.
- *From the vault:* "That's the real difference." / "That detail changes the whole scene for me."
- End on the last actual point instead. If the closer holds a real idea, merge it into the previous sentence.

**Fake-deep framing.** "The real question is", "the deeper pattern", "at its core", "what's striking is", "crueler than that", "the whole point". Just say the thing.

**Commentary about the idea instead of the idea.** "An irony worth sitting with:", "a genuine alternative worth holding against this", "importantly,", "interestingly,", "it's worth noting that". Delete the frame and keep the content.

**Announcing a point before making it.** "Here's the thing:", "Let me explain", "The key insight is". Start with the point.

**Forced groups of three.** "intensity, struggle, and growth", "intelligence, irony, and cruelty". Use three items only when there really are three distinct things. Two is fine. One precise word is better.

**Stacked hedges.** "might perhaps suggest", "could arguably be seen as". One qualifier at most, only where the doubt is real.

**"-ing" tails that add fake significance.** "..., highlighting the tension between X and Y", "..., reflecting a broader shift". Cut them, or make them a separate claim that you can support.

**Same rhythm everywhere.** Several sentences in a row with the same opening, the same length, or the same "X, Y, and Z" shape. Vary them. A short sentence is fine.

**Over-long chained sentences.** One sentence carrying four ideas linked by dashes, semicolons, and parentheses. Split it. A sentence over ~35 words probably needs splitting.

## 3. Words

**Intensifiers that inflate.** `genuinely`, `precisely`, `truly`, `deeply`, `incredibly`, `the real` (as in "the real him", "the real difference"). The vault had about 77. Delete them; the sentence almost always survives. Keep `actually` only when it corrects something ("I thought X, but it's actually Y").

**AI-favored vocabulary.** Avoid: delve, tapestry, testament, pivotal, crucial, vital, profound, nuanced, multifaceted, intricate, interplay, resonate, underscore, highlight (verb), showcase, embody, encapsulate, foster, enhance, garner, navigate (figurative), landscape (figurative), realm, journey (figurative), poignant, stark, haunting, visceral, masterful, vibrant, enduring, indelible, rich (figurative), key (adjective), robust, leverage, seamless, additionally (as a sentence opener).

**Avoiding "is" and "has".** `serves as`, `stands as`, `functions as`, `marks`, `boasts`, `features`. Write `is` and `has`.

**Vague connections.** `associated with`, `connected to`, `in connection with`. Name the actual relationship (wrote, influenced, argued against, was arrested with).

## 4. Claude-written reference sections

`# Summary`, `# Main characters`, `# Historical & cultural context`, and `historical-context/` notes.

- **No inflated significance.** Nothing like "a pivotal moment in literary history", "remains strikingly relevant today", "left an indelible mark". Give the fact and let it carry its own weight.
- **No vague attribution.** Not "is widely read as", "critics argue", "scholars have noted" without saying who. Name the source or state it as the book's content. If you can't name anyone, drop the claim.
- **Facts first, interpretation labeled.** Dates, names, what happened. If a sentence is interpretation, it belongs to Marco's `# Notes` or needs a named source.
- **Short.** A summary is a memory aid. Plain sentences, plot in order, the ending included.

## 5. Formatting

- **Bold** only for names in character or figure lists and for a key term the first time it's defined. Never for emphasis inside prose.
- No horizontal rules (`---`) between sections, except frontmatter.
- Headings in sentence case. Don't skip heading levels.
- No end-of-section recap paragraphs.

## 6. Marco's voice (`# Notes`, concept definitions)

- **Removal over addition.** When cleaning his text, cut slop and fix grammar. Don't add ideas, examples, or stakes that weren't in his answers.
- **Keep his wording and his sentence shapes.** Fixing grammar does not mean upgrading his vocabulary or making him sound more literary. Plain beats elegant.
- **Keep his real hedges and corrections.** "I think", "I'm not sure", "I first read it as X, but" are his thinking, not slop.
- **Don't overcorrect.** A single dash-like pause or a list of three that's really three is fine. The problem is the density and the automatic habits, not every single instance.

## 7. Self-check before finishing

Re-read what you wrote. Then search it:

```bash
grep -n -i -E "—|–[^0-9]|isn't [^.]*, it's|it's not [^.]*, it's|not just|genuinely|precisely|truly|the real |the deeper|at its core|worth (sitting|noting|holding)|importantly|widely (read|seen|regarded)|serves as|stands as|testament|pivotal|crucial|profound|nuanced|tapestry|interplay|underscore|resonat|embod" <file>
```

Rewrite every hit that matches a pattern above. Check one paragraph by ear: if it sounds like a book blurb or a lecture, simplify it.
