# Personas: Subconscious

Status: Draft

Companion to [PRD.md](./PRD.md). Six personas, ordered by how well Milestone 1 serves them.

## Marcus — 27, 4th-year PhD student (cognitive science)

**Beachhead.**

**Setup:** Zotero with 1,400 PDFs, Obsidian vault with ~900 notes, an old ThinkPad running Linux plus a desktop with a 3090 in it. Runs local models already, mostly for fun. Broke—will not pay $20/mo, will absolutely spend a weekend configuring something free.

**Day:** reads 3–5 papers, writes badly, procrastinates, teaches undergrads. Thesis is 18 months from done and the lit review is a monster he can no longer hold in his head.

**Pain:** he's read everything and remembers nothing. The connection between the paper he read in year 2 and the experiment he's designing now exists—he just can't retrieve it.

**Wants:** overnight synthesis across his reading corpus, with citations he can verify. "These three papers disagree about X." The reference archive is the killer feature—his corpus is what he *read*, not what he wrote.

**Quits if:** a dream cites something that isn't in the source. One hallucinated citation and he's out—academic reflex.

**Why he's first:** existing vault, Linux comfort, local GPU, high tolerance for filesystem-as-UI, and an actual corpus for Milestone 1 to dream over. Also the most likely to file good issues.

## Priya — 34, senior product manager at a mid-size SaaS company

**Setup:** MacBook Pro (work-managed), personal iPhone. Notion for work docs, Apple Notes for everything real, ~600 unorganized ChatGPT threads. Tried Obsidian for six weeks in 2023 and bounced. Pays for ChatGPT Plus out of pocket.

**Day:** 6–8 hours of meetings, Slack, and docs. Thinks in the 20 minutes before bed and on Sunday mornings. Runs the same three questions constantly: *is this the right bet, what did we already learn about this, what am I not seeing.*

**Pain:** re-derives the same conclusion every quarter because the reasoning lives in a Slack thread from March. Her best strategic thinking happens in ChatGPT and evaporates when the thread scrolls away.

**Wants:** a morning brief before standup. "You concluded the opposite of this in April—here's the note." Lens re-runs on standing questions.

**Quits if:** setup takes more than 10 minutes, or review is a terminal/vim thing. Needs mobile. Milestone 2, not Milestone 1.

## Maya — 38, illustrator and printmaker

**Setup:** iPad Pro for drawing, an aging MacBook Air used mostly for invoices and print files, iPhone always in hand. A paper notebook for morning pages. A camera roll with 400 screenshots, fabric swatches, and half-legible poems. Squarespace shop, Instagram, part-time teaching at an art college. Freelance editorial work pays the rent unevenly.

**Day:** morning pages first thing—three pages longhand, six years on and off. Studio in the afternoon if teaching allows. Ideas arrive on walks and in the shower and are lost within the hour.

**Pain:** the pages are a dumping ground she never rereads, by design—Cameron's rule. So the obsessions inside them are invisible to her. She knows there are four years of recurring images in that stack of notebooks and no way to see them without violating the practice that produced them. Meanwhile every new series starts from anxiety and a blank wall.

**Wants:** capture in under 15 seconds—dictate the pages while making coffee, or photograph them. Then, later, *provocations* rather than summaries: "you've drawn the same doorway four times this month," "these two notes from different years want to be the same piece." Oblique Strategies generated from her own subconscious. Prompts for the next body of work.

**Quits if:** the output sounds like a manager or a therapist. Also if it *summarizes*—paraphrase kills the material. The value is in the collision of her own fragments, not a tidy account of them.

**The tension worth designing for:** morning pages work *because* you don't reread them. An agent that reads them back the same morning breaks the practice—the pages stop being a dump and start being performance for an audience. This argues for an embargo: dreams sourced from morning pages surface on a deliberate lag of weeks or months, never same-day. That falls out of cron triggers and event sourcing for free, and it makes Maya the purest test of the PRD's ritual technology claim: her success metric *is* the headline metric.

## Elena — 52, independent consultant / writer

**Setup:** 20 years of professional archive: client decks, a 2008–2015 blog, three unfinished book manuscripts, 11 GB of email. Half of it is on a dead external drive. iPad + MacBook Air, Scrivener, Things, DEVONthink (lapsed).

**Day:** two client calls, writing, invoicing. Publishes a newsletter to 4,000 people twice a month. Her back catalog of thinking *is* the business asset.

**Pain:** she has said everything she's saying now, better, in 2014, and can't find it. Every newsletter starts from a blank page when it shouldn't.

**Wants:** resurfacing and reuse. On-this-day. "You wrote about this in 2016—here's the argument, more developed than the one you're making today." Tours through her own archive.

**Quits if:** it can't ingest twenty years of heterogeneous junk. Import is the whole product for her; she has no interest in building a vault from scratch at 52.

## Devon — 41, partner at a $60M seed fund

**Setup:** Superhuman, Affinity CRM, Notion for memos, Granola for call notes. ~1,100 pitch decks in a Drive folder. Airtable market maps that go stale in six weeks. Runs Claude and ChatGPT side by side, mostly for deck summarization.

**Day:** 6–8 founder calls, two partner meetings a week, and the actual job—deciding what to believe about the next five years—squeezed into flight time and Saturday. Writes a thesis memo maybe once a quarter; it's read once and dies in Notion.

**Pain:** patterns arrive as a slow drip across hundreds of conversations, and there's no place they accumulate. Devon met four companies attacking the same wedge over eight months and only noticed in the fifth meeting. The alpha in this job is *noticing early*, and the noticing currently depends on human recall of 1,100 conversations.

**Wants:** theses as lenses—the closest fit to an existing feature in the PRD. "Vertical AI agents will be sold per-outcome, not per-seat" becomes a standing question, re-answered monthly against every new call note, deck, and article. Wants to watch a thesis's confidence evolve across quarters with the evidence trail attached, and wants to be told when new evidence *contradicts* a thesis, not just supports it.

**Quits if:** it's a shared/team surface. Devon's thesis notes contain candid opinions about founders and about partners. Single-player and encrypted isn't a preference, it's a precondition. Also: the reference archive matters more than notes—the corpus is what Devon *read and heard*, not wrote.

## Sam — 31, technical cofounder, seed-stage (9 people, 14 months of runway)

**Setup:** Linear, Notion, a Slack `#strategy` channel that's really a decision graveyard, 60 recorded customer calls in Gong, and a `strategy-v7-FINAL.md` in a repo. Heavy Claude Code user—the vibe-coding audience the PRD's "Why now?" is written for.

**Day:** context-switches every 20 minutes between code, hiring, and customers. Real strategic thinking happens at 11pm or on a walk. Rewrites positioning roughly every six weeks and has no record of *why* the last version was wrong.

**Pain:** pivots are lossy. Each repositioning throws away the reasoning that produced it, so the team relitigates settled questions and re-learns the same lessons from customer calls. Sam can't answer "what changed our mind between v4 and v5"—and that's exactly the question the board asks.

**Wants:** synthesis across customer calls plus his own notes ("eleven of the last thirty calls mentioned this objection; you've been dismissing it since March"), and a decision provenance trail—the PRD's provenance requirement applied to strategy rather than notes. The hand is genuinely useful here: stash five call notes plus a competitor teardown, generate a dream.

**Quits if:** it feels like another tool the team has to adopt. This is a single-player tool for Sam's own head that happens to make the company smarter. The moment it needs buy-in from the team, it dies.

## Implications for the product

**Cold start is a bigger problem than the PRD accounts for.** Four of six personas arrive with a corpus that is not an Obsidian vault: ChatGPT threads, PDFs, 20 years of email and manuscripts, call notes and decks. Maya arrives with no digital corpus at all—hers is generated daily by the product itself, which is the one case where the cold start solves itself if capture is fast enough. "Dreams are about *you*" requires material. Import breadth is a cold-start solution, not a convenience feature—and only Obsidian import is currently in the requirements list.

**Contradiction is a missing dream type.** Devon and Sam live or die on *change over time* and *disconfirmation*, not retrieval. Lens re-runs already produce the raw material—an old answer beside a new one—but the PRD frames re-runs passively, as "watch an answer evolve." For these two it needs to be assertive: *this belief is now weaker than it was.*

**Encryption and single-player have a commercial justification, not just an ideological one.** Devon's candid notes on founders and partners, and Sam's strategy reasoning, are the cases where privacy is a precondition of adoption rather than a value statement.

**Dreams need registers, not one voice.** Marcus needs verifiable citations and will quit over a hallucinated source. Maya needs oblique provocation and will quit over a tidy summary. Same generator, opposite failure modes. Dream type should carry a register, and the review signal should be able to teach it—"less like a report, more like a prompt" is exactly the kind of semantic-level feedback the Loop already promises.

**Some dreams should be embargoed.** Not all material wants same-day reflection. Morning pages specifically require distance to keep working. A per-source delay before dreams can draw on it is cheap given the event log, and it's the difference between augmenting Maya's practice and destroying it.

**Measure the headline metric on Marcus and Maya.** "The ritual survives to week 4" is only meaningful for someone who would otherwise churn. The sovereignty-motivated user stays regardless of dream quality; Priya and Elena can't reach week 4 on a filesystem UI. Marcus is the honest signal for corpus-driven dreams, Maya for ritual-driven ones—she already has a daily practice, so the question is purely whether Subconscious makes it better or breaks it.

**Personas map to milestones:**

- Milestone 1 — Marcus
- Milestone 2 — Priya, Sam, Maya (needs voice/quick capture)
- Gated on import breadth — Elena, Devon
