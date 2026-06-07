# Development Diary — Layer Shifts As Test Candidate

## Context

A new possible use for layers emerged while discussing NPC behavior.

The idea is not yet proven and should be treated as a test candidate.

---

## Current Idea

Layers can act as the base system that shapes how a character, district, faction, or culture interprets experience.

A layer is not the same as a faction.

A faction is an organization.

A layer is a behavioral/worldview base.

---

## Possible Design Chain

Layer
-> experience
-> emotion
-> reason
-> behavior
-> atmosphere
-> quest logic

The layer influences how experience becomes reason and behavior.

---

## Player Influence Hypothesis

The player may be able to influence an NPC's base layer by creating meaningful experiences.

If the experience is strong enough, the NPC's interpretation of the world may shift.

That shift could change:

- dialogue
- trust
- future quest options
- faction sympathy
- willingness to cooperate
- willingness to betray old loyalties

---

## Example

An NPC begins with a Regulatus base layer.

They believe the system is flawed but necessary.

The player exposes that a ration office is deliberately hoarding food while families starve.

Possible result:

- experience: proof of state corruption
- emotion: betrayal
- reason: the state is protecting itself, not the people
- behavior: the NPC stops trusting official channels and becomes more open to Novacula ideas

The NPC has not simply changed faction.

Their interpretation layer has shifted.

---

## Why This Matters

This could make player choice affect more than reputation numbers.

Player actions could change how NPCs understand future events.

That would make later behavior feel earned rather than arbitrary.

---

## Caution

This is currently only a hypothesis.

It needs testing before becoming a core system.

Questions to test:

- Can layer shifts be represented simply?
- Do they create meaningful NPC changes?
- Do they become too complex for practical design?
- Can they work through tags or thresholds instead of full simulation?
- Does the system remain understandable to players?

---

## Current Best Implementation Idea

Use simple design tags first:

- dominant layer
- secondary layer
- breaking point

Example:

Dominant Layer: Regulatus
Secondary Layer: Lux
Breaking Point: If legal aid fails repeatedly, Novacula influence rises.

This keeps the idea testable without requiring complex simulation.