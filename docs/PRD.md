# PRD: Subconscious Prototype

Status: Draft

## Overview

(TLDR)

## Problem

AI already outperforms humans in many activities, and its capabilities are rapidly expanding. Soon, most economically-valuable knowledge work will be done entirely by AI. To survive and compete in the AI information economy, we need to augment our intellect with AI.

The AI people rely on today belong to corporations. Your memory, your context, your conversations, the accumulated model of how you think—your extended mind—belong to someone else. There goes your alpha.

We need an **AI Subconscious**: a truly personal agent that thinks with you, and can store a lifetime of memory in a vault that you own.

## Solution

Imagine a personal agent that remembers every interaction you have had together, it saves every conversation, every memory, every note that you've taken. This lifetime of AI memory is your digital shadow, your [exoself](https://kevinkelly.substack.com/p/quiet-my-exoself), your **Subconscious**. It belongs to you. Your Subconscious is stored in a decentralized, and end-to-end encrypted vault that you control.

Memory is the critical bit. Open source models have been rapidly commodifying the frontier (ETA ~3mo as of 2026), denying any one lab monopoly pricing power. You can pretty much just switch AIs whenever. The one wrinkle in this story is memory. If you accumulate memory in ChatGPT, you won't want to switch. Furthermore, whatever leverage your memory gave you belongs to them now. Therefore: who owns your memory owns your future. But what if we were to intercept every memory, every message, every bit of context, and save our own copy?  Now we have *[credible exit](https://newsletter.squishy.computer/p/credible-exit)*. So, we want a harness that stores a lifetime of AI memory in a user-owned vault, private and encrypted where feasible, or, at minimum, fully exportable.

Subconscious is Zettelkasten one meta-layer up. The classic Zettelkasten loop works because making and filing cards forces intentional engagement with your own ideas—and fails because almost nobody sustains the clerical labor. Subconscious moves you up a layer: the agent proposes the cards, you curate. Approving, merging, renaming, rejecting—that isn't a review step bolted on for safety. It *is* the thinking. The machine does the filing; you keep the judgment.

## Goals

- A personal agent that augments the user's thinking and grows with them over a lifetime.
- User-owned memory
  - Saves every memory, every message, every note, every bit of plugin data.
  - At minimum, an exportable copy of all data for credible exit.
  - Ideally private and encrypted.
- Subconscious is a tool for thought
  - Pre-GPT apps like Obsidian were TfT 1.0. We're building TfT 2.0.
  - An agent designed to do the _opposite_ of AI deskilling. Subconscious makes you smarter.
  - Subconscious expands your OODA loop, and is especially focused on **orientation**.
  - Built-in LLM wiki.
  - Daily Rituals. Subconscious is a [ritual technology](https://newsletter.squishy.computer/p/ritual-technology). Daily review helps you craft personal feedback loops that let you learn faster, generate new thoughts, make new breakthroughs, and tackle more ambitious problems.
- Lasts a lifetime
  - Data can outlive any company.
  - Export lets it even outlive the software.

### Non-goals

- Storing data as files
- Reinventing markup. Markdown is good enough.
- P2P or "full" decentralization: Decentralization is hard. Our primary goal is credible exit through user-owned data. CAL grants both source code and access to personal data, preventing lock-in. This is sufficient for our goals. 

## Users and use-cases

- Knowledge workers: amplify your insights, creativity, strategy, and workflows
- Students: see themes emerge from the bottom-up from your study notes and collected papers
- Artists and writers: generate creative breakthroughs, see long-running threads you're following surfaced back to you.
- Founders and investors: monitor live signals, refine your theses

## Requirements

- (P1) **Chat**
  - (P1) **Messages**
  - (P1) Plain-text search across messages
  - (P2) Chat widgets
    - Table view
    - Mermaid diagrams
- (P1) **LLM wiki**
  - (P1) **Notes**
    - Notes: user-generated notes
    - Dreams: AI-generated notes
    - Agents: specially tagged note, interpreted as a template for a subagent
    - Skills: specially tagged note, loaded into agent harness as a skill
    - Config: configuration stored as note(s)
    - Subscriptions: stored as note(s)
    - Transform any note into any other kind of note. Dream to note, note to agent, dream to skill, etc.
  - (P1) **Wiki versioning**
    - (P1) Multiple editors / conflict resolution
    - (P3) real-time collaborative text editing
  - (P1) **Path-addressable**
    - Notes addressable by rev (hash address for revision), globally-unique ID, or path. Think identifier vs locator.
  - (P1) **Structured data**
    - JSON-compatible
    - Serializable as Markdown with frontmatter
  - (P1) **Markdown content**
    - Support subset of Obsidian-flavored Markdown
    - Wikilinks: use Obsidian resolution algorithm.
    - Block references: use Obsidian-style.
  - (P1) Quick capture
  - (P1) Plain-text search
- (P1) **Provenance**
  - Every dream is explainable: which spell, which sources, which model, triggered by what.
  - Git records *that* a file changed; the event log records *why*. We want to know exactly how we arrived at the current version of every note.
  - Edits arriving via vault sync are provenance-poor ("user edited this in Obsidian"). That's fine, but the system distinguishes "I know exactly why this exists" from "the human touched this directly"—they are different classes of fact.
- (P1) **Reference archive**
  - Content-addressed snapshot store for everything you read: articles, URLs, imported AI conversations.
  - Lenses recompute over the corpus, so the corpus must include what you *read*, not just what you wrote.
  - Snapshots, not links: links rot. The archive must outlive the web it points to.
  - Your archive is yours alone—not a communal pool. Subconscious individuates.
- **Agents** (spawned from agent notes)
  - **Day agent**: agents that you converse with
  - **Night agents**: agents that work while you sleep (event-driven)
- **Harness**
  - (P1) Swap LLM providers
    - Local by default: embeddings, search, classification, autotagging run on local models.
    - Frontier by exception: synthesis and conversation, where depth pays for itself.
    - This is both the privacy story and the cost story for something that runs nightly over your whole life.
  - (P1) Auto-compaction
  - (P1) Memory blocks (Letta-style)
  - (P1) Cache-efficient context injection
  - (P1) Skills
    - Use hyperlinks/wikilinks for progressive disclosure, rather than folder-based discovery.
- **Tools**
  - (P1) Edit note
  - (P1) Search notes
  - (P1) Search messages
  - (P1) Search web
- **Event system**
  - (P2): event sourced architecture
  - (P1) Path-based event subscriptions
  - (P1) Subscribe to wiki edits
  - (P1) event cascade control: `correlation_id`, `causation_id`, `depth`, token stats, etc for limiting runaway event cascades
- **Inputs**
  - Subscribe to RSS feed
  - Send email
- **Outputs**
  - Send an email
  - Post to Telegram
- **Workflows**
  - Queue with workflow attached
- **Cron jobs**
- **Import/export**
  - (P1) Export Markdown with frontmatter
  - (P1) Import/export Obsidian Vault
    - (P2): Bi-directional Sync with Obsidian Vault
- **Sync**
  - (P1): Sync memory vault copies across your devices
  - (P3): Decentralize memory vault
- (P3) **Multiplayer**
  - (P3): Post to Bluesky

## User Experience

### Principles

#### The Loop

The core mechanic:

**Spells → Dreams → Review → Signal → (better) Dreams**

- **Spells**: agent-notes with trigger conditions ("nightly", "when a note matching X changes"). A spell is an instruction stated in your terms: "find connections between...", "re-answer this question against everything new...".
- **Dreams**: notes generated by spells. Every dream carries provenance: which spell, which sources, which model, triggered by what.
- **Review**: the daily ritual. Accept, reject, merge, rename. "These two terms are the same." "This tag is wrong."
- **Signal**: review decisions are events. Future spell runs read them. Feedback is always given at the semantic level—you say what you meant, and agents translate that into reorganization. You never edit configuration.

#### Questions are lenses

A question you ask more than once is a standing query against a growing corpus. A lens is just a spell whose instruction is a question—no new primitive needed. The system's job is the *noticing*: observe the questions you keep asking (in chat, in reflections) and propose them back as spells. "You keep asking some version of this. Want it re-answered as your corpus grows?"

Re-running a lens never overwrites the old answer. It produces a new dream that cites its predecessor, so you can watch an answer evolve across months and years. (This falls out of event sourcing for free.)

#### Dreams are about you

- Dreams are about *you*: "you've changed your mind about X", "you keep circling Y".
- Dreams speak predominantly in your own words.
- Dreams cite their sources. Quote where possible. Include citations when synthesizing. Link the actual notes. Dream are easier to believe in when you can check the sources.

#### A garden, not an inbox

- No unread counts.
- No queue to clear. Dreams don't expire; unreviewed dreams are not debt.
- Review is a place you visit—[are.na](https://www.are.na) energy, a garden you poke around in—not an inbox you owe.

A **tour** is a dream type: a generated narrative walk through notes you already have, rather than a new synthesis.

### Views

- FRE
  - Journey: first-run
  - Story: as a first-time user, I want my Subconscious to learn about me so it can customize itself to me.
  - Short wizard
  - Select "interest" tokens to construct a user archetype
- Home
  - Journey: reflection
  - Story: as a user I want to see themes and insights reflected back to me from my Subconscious.
  - Goal: close feedback loop between myself and my Subconscious
  - Dreams: stack of stories generated from your Subconscious
    - Once per day?
    - Dreams types
      - AI-generated notes
      - Updates (e.g. OTD resurfaced notes)
      - Prompts to user (e.g. multiple choice, or text input)
      - Tours: a narrative walk through notes you already have
      - Lens re-runs: an old question, re-answered, citing its previous answer
    - **Set an intention**: influence what shows up next time by setting an intention
    - Swipe through dreams
      - One at a time, so you can turn your full attention to each dream
      - Signal: e.g. Tinder swipe or similar more/less signal 
      - Choices shuffle in new dreams
    - Save dream -> note
    - Add dream to your hand
  - AI chat box
- Hand (scratch)
  - A HUD you can pull up from anywhere
  - Story (quick capture): As a user, I want a scratch space where I can jot down quick thoughts or compare multiple notes.
  - Story (synthesize): When I've gathered a few notes that feel related, I want to hand them to my Subconscious and have it generate something new out of the combination.
    - Goal: explore adjacent possible, combinatorial innovation
  - Hand: Collection of notes you've temporarily stashed
  - Generate new dream from contents of your hand
  - Daily note
  - Recent notes
  - Tabs
- Chat
  - Goal: chat with your Subconscious
  - Story (query): as a user, I want to be able to ask questions of my Subconscious, and get grounded answers.
  - Story (rubber duck): as a user, I want to be able to think through a problem with my Subconscious.
  - Story (steering): as a user, I want to be able to steer my background agents.
  - Conversation grounded in notes
  - Generate TLDRs, summaries, and reports
  - Steer night agents
- Quick capture
  - Goal: capture as fast as possible, organize later
  - Story: When a thought arrives while I'm in the middle of something else, I want to get it into the vault in seconds without titling or filing it, so I can keep my attention on what I was doing and trust that it will be organized later.
  - Title optional (either generated or not required)
  - Autotag?
  - Capture URL
  - Voice memo
- Wiki
- Agent status
- Notifications
- Plugins

## Technical specs

### Tech stack

- Language: Typescript
  - Rust components?
- Runtime: Node
- Bundler: Vite or ESBuild?
- DB: SQLite or [DialogDB](https://github.com/dialog-db/dialog-db)

Prototype approach:
- Pi plugin

### Architecture

- Event sourced
  - Pro: Event log allows agents to recover from failure by looking back at log
  - Pro: easy to build multiple projections/UIs on top
  - Track causality (automatically assign `prev` ID to event based on current HEAD at write time).
    - Allows deterministic conflict resolution when merging event logs
  - **Commands** (unicast requests / "please do x") and **events** (multicast facts / "x happend")
- Named queues (backed by DB table)
  - FIFO
  - Queryable
  - At-least-once delivery
  - SQS-style timeout lease system
- LLM wiki
  - Versioned JSON
  - CouchDB-like version/conflict resolution semantics
  - Optimistic concurrency
  - Read-before-write guard for client<->server synce
    - Forces agents to read and merge conflicts
- Content-addressed store
  - Structural sharing between fat events and projections
    - E.g. `content` field is a cid in event and in wiki entry
- Agents as actors
  - Actor-like system built on top of event sourced log
    - Messages are a type of command
  - Agents have an **address**
  - Agents have a **sendMessage** tool that takes an address
      - Tool automatically tracks `correlationId`, `causationId`, `depth`
  - Agents have a **spawnAgent** tool
      - Takes a template
      - Records address, adds to their context automatically
      - `{ to: string, replyTo?: string, message, data: Record<string, unknown> }`
          - Automatically expanded to `{ id, type, from, to, replyTo, message, data, time, correlationId, causationId, depth }` with publish tool expanding metadata and threading causality.
      - Subagents only live as long as their session
          - Can be sent steering messages to kill
  - Name system: Name -> Address
    - E.g. `@subsconscious -> abc123xyz...`
    - Local human-readable names (DNS-like)
    - Globally-unique addresses (UUID or similar)
    - Agent frontmatter can be configured with well-known addresses

### Event-sourcing

`events` table as Typescript schema:

```typescript
type Event = {
  id: string; // ULID
  prev?: string; // ULID
  kind: "command" | "event";
  type: string;
  from: string; // Address
  to?: string; // Address
  replyTo?: string; // Address
  message: string; // Human-friendly message
  data: Record<string, unknown>; // Structured data
  correlationId: string; // ULID
  causationId: string; // ULID
  depth: number; // Cycle detection. Always incremented by 1.
}
```

Notes:
- Log both commands and events
- Fat events: state must be derivable from event log
- ID: ULID or UUID v7?
  - Prefer UUID v7. Native support in Postgres 18.
- Causality data automatically threaded by the system (not the agent
  - Agent `sendMessage` tool bound to thread `{ cause: event }` through

### LLM wiki

Assuming a CouchDB-shaped record (vs DialogDB)...

```typescript
type Doc = {
  _id: string; // UUID. Globally-unique reference.
  _rev: string; // CouchDB-style rev.
  _schema: string; // URI e.g. `urn:subconscious:schema:g:agent/v1`
  _path: string; // path string "foo/bar/baz". Locally unique address
  title?: string;
  content: string;
  [key: string]: unknown; // Arbitrary other properties
}
```

Notes:
- Must serialize to Markdown with frontmatter. Content is body. Everything else is frontmatter.

Open questions:
- Are paths better handled via name system (e.g. petnames)?
  - If so, `_path` could be interpreted as "preferred path"

## Success Metrics

- **The ritual survives.** The user is still voluntarily doing review in week 4.
- **Dream acceptance rate is informative.** Collapsing toward 0% means slop. Sitting at 100% means sycophancy, or rubber-stamping. A healthy middle means curation is actually happening.
- **Old questions get revisited.** Lens re-runs are read; users watch answers evolve.

## Milestones & Scope

Phasing resolves the requirements list without deleting from it.

### Milestone 1 — The daemon and the loop

One command, run in your existing vault. It just starts working.

- Daemon + bidirectional vault sync (DB is source of truth; the vault is a projection)
- Event log + provenance
- Spells run on triggers; dreams land as files
- Review happens in your own editor (Obsidian, vim, whatever)—the filesystem is the UI
- Local embeddings + plain-text search
- No chat, no name system, no inputs/outputs

Milestone 1 exists to test one hypothesis: **are the dreams good enough that you keep the ritual?**

### Milestone 2 — The ritual surface

- Review experience: tours, the hand, intentions, swipe
- Chat (day agents)
- Quick capture
- Lens noticing: propose your recurring questions back to you as spells

### Milestone 3 — The world

- Sync across devices
- Inputs/outputs: RSS, email, Telegram
- Multiplayer flirtations: Bluesky, shared gardens

## FAQ

### Why now?

We tried building this as a startup back before GPT was a thing. Unfortunately, building Subconscious way back then required solving a number of Very Hard technical challenges. How do you guarantee user-owned data? How do you build the agents? How do you decentralize it? We [burnt too much of our runway trying to solve these hard problems](https://newsletter.squishy.computer/p/subconscious-is-winding-down), and that was that. But the idea wasn't wrong, just early. A bunch of the hard problems are now solvable with off-the-shelf components:

- Agents: any LLM provider. Abstraction layers like Vercel AI SDK let us swap between providers, or even use local models.
- User-owned data: CAL license and/or a decentralizable data storage layer like DialogDB or Automerge.
- User-owned keys and rotation: use ATProto's did:plc.
- Sync: use DialogDB, Automerge, or clone CouchDB's algorithm on top of SQLite.

What remains? Mostly product design.

Furthermore, the existence of Fable-class models pushes software into post-scarcity. We no longer need to build a startup to make this happen. We can vibe-code Subconscious using our excess tokens and release the whole thing Open Source. The CAL license bakes in user data ownership, so your Subconscious is yours forever.

### Why Subconscious?

We bring a strong set of opinions about how a personal agent works, and how it will expand your OODA loop. Subconscious is _designed_. It works out of the box, and comes with a set of workflows it has been designed for.

## Appendix
<!-- Links, references, prior art: Engelbart (augmenting human intellect), Alan Kay (Dynabook), the "exoself" concept. -->
