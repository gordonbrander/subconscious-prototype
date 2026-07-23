# Product Requirements Document — Subconscious Prototype

Status: Draft

## Overview

(TLDR)

## Problem

AI already outperforms humans in many activities, and its capabilities are rapidly expanding. Soon, most economically-valuable knowledge work will be done entirely by AI. To survive and compete in the AI information economy, we need to augment our intellect with AI.

The AI people rely on today belong to corporations. Your memory, your context, your conversations, the accumulated model of how you think—your extended mind—belong to someone else. There goes your alpha.

We need an **AI Subconscious**: a truly personal agent that thinks with you, and can store a lifetime of memory in a vault that you own.

## Solution

Imagine a personal agent that remembers every interaction you have had together, it saves every conversation, every memory, every note that you've taken. This lifetime of context is your digital shadow, your [exoself](https://kevinkelly.substack.com/p/quiet-my-exoself), your **Subconscious**. It belongs to you. Your Subconscious is stored in a decentralized, and end-to-end encrypted vault that you control.

The critical component is memory. We want a person to own the entire record of their thinking-with-AI: private and encrypted where feasible, and — at minimum — a fully owned copy that guarantees *credible exit*.

## Goals

- P1: A personal agent that augments the user's thinking and grows with them over a lifetime.
- P1: User-owned memory
  - The full record of context, notes, and conversations belongs to the user.
- P1: Credible exit
  - At minimum, a complete owned copy of all data, ideally private and encrypted.
- P1: Your Subconscious makes you smarter.
  - We're desigining an agent for the _opposite_ of AI deskilling.
  - Subconscious expands your OODA loop, and is especially focused on **orientation**.
  - Daily Rituals. Subconscious is a [ritual technology](https://newsletter.squishy.computer/p/ritual-technology). Daily review helps you craft personal feedback loops that let you learn faster, generate new thoughts, make new breakthroughs, and tackle more ambitious problems.

### Non-goals

- Storing data as files
- Reinventing markup. Markdown is good enough.
- P2P or "full" decentralization: Decentralization is hard. Our primary goal is credible exit through user-owned data. CAL grants both source code and access to personal data, preventing lock-in. This is sufficient for our goals. 

## Users and use-cases
<!-- Who uses this? Primary personas and their key jobs-to-be-done. -->

## Requirements

- P1: LLM wiki
  - Versioned
  - JSON-compatible data model
  - Serializable as Markdown with Frontmatter.
  - Path-addressable
- P1: Import/export Obsidian Vault
  - P2: Bi-directional Sync with Obsidian Vault
- P2: Decentralize your memory vault
- P3: Multiplayer
- P3: Post to Bluesky

## User Experience
<!-- Key flows, wireframes, or screen-by-screen walkthrough. -->

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
