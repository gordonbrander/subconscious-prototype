# Product Requirements Document — Subconscious Prototype

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
<!-- Who uses this? Primary personas and their key jobs-to-be-done. -->

## Requirements

- (P1) **Conversations**
  - (P1) **Messages**
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
  - (P1) Path-addressable
  - (P1) Structured data
    - JSON-compatible
    - Serializable as Markdown with frontmatter
- **Agents** (spawned from agent notes)
  - **Day agent**: agents that you converse with
  - **Night agents**: agents that work while you sleep (event-driven)
- **Harness**
  - (P1) Auto-compaction
  - (P1) Letta-style memory blocks
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

## Technical specs

## Success Metrics
<!-- How we'll know it's working. -->

## Milestones & Scope
<!-- Phasing: what ships first (MVP) vs. later. -->

## FAQ

### Why now?

We tried building this as a startup back before GPT was a thing. Unfortunately, building Subconscious way back then required solving a number of Very Hard technical challenges. How do you guarantee user-owned data? How do you build the agents? How do you decentralize it? We [burnt too much of our runway trying to solve these hard problems](https://newsletter.squishy.computer/p/subconscious-is-winding-down), and that was that. But the idea wasn't wrong, just early. A bunch of the hard problems are now solvable with off-the-shelf components:

- Agents: any LLM provider. Abstraction layers like Vercel AI SDK let us swap between providers, or even use local models.
- User-owned data: CAL license and/or a decentralizable data storage layer like DialogDB or Automerge.
- User-owned keys and rotation: use ATProto's did:plc.
- Sync: use DialogDB, Automerge, or clone CouchDB's algorithm on top of SQLite.

What remains? Mostly product design.

Furthermore, the existence of Fable-class models pushes software into post-scarcity. We no longer need to build a startup to make this happen. We can vibe-code Subconscious using our excess tokens and release the whole thing Open Source. The CAL license bakes in user data ownership, so your Subconscious is yours forever.

## Appendix
<!-- Links, references, prior art: Engelbart (augmenting human intellect), Alan Kay (Dynabook), the "exoself" concept. -->
