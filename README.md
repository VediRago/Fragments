# Fragments

I'm Diogo Oliveira. I currently work full-time in glass manufacturing, and I am building **Fragments** outside of work as a hobby project.

This project is very early. I started **Fragments** on **20/05/2026**. The worldbuilding began on **05/06/2026**, and the NPC / quest method started on **07/06/2026**.

I am not presenting this as finished professional game development work.

I am using this repository to track what I am trying to understand and test.

Through this project, I am testing:

- whether emotional causes can make lore feel less random
- whether character wounds can grow into family patterns and world systems
- whether a repeated detail can become a clue, then a reveal, then a payoff
- whether world pressure can lead toward quests, conflicts, and consequences
- whether a layer-based method can help NPCs, districts, factions, and quests react without breaking immersion

## What This Repository Is For

This is a working record, not a finished game.

My current focus is the Erit worldbuilding branch, where I am testing whether world pressure can create factions, NPCs, quests, and consequences that feel connected instead of separate.

## Current Method

While building Erit's world, I started writing down a method for connecting worldbuilding, factions, NPCs, atmosphere, and quests through cause and consequence.

The core chain I am testing is:

> Experience → Emotion → Reason → Behavior → Atmosphere → Quest Logic

I use three layers to control where the pressure comes from and what can change afterward.

```text
                           ┌────────────────────────────┐
                           │ 1. Define World Pressure   │
                           │ Layer 1                    │
                           │ Events shaping the world   │
                           └─────────────┬──────────────┘
                                         │
                  ┌──────────────────────┴──────────────────────┐
                  │                                             │
        ┌─────────▼─────────┐                       ┌───────────▼──────────┐
        │ 2A. Read City      │                       │ 2B. Read Faction     │
        │ Layer 2            │                       │ Layer 2              │
        │ Fluid / Mutable    │                       │ Locked               │
        └─────────┬─────────┘                       └───────────┬──────────┘
                  │                                             │
        ┌─────────▼─────────┐                       ┌───────────▼──────────┐
        │ 3A. Select NPC    │                       │ 3B. Select NPC       │
        │ Patient / Nurse   │                       │ Guard                │
        │ Layer 3            │                       │ Layer 3              │
        └─────────┬─────────┘                       └───────────┬──────────┘
                  │                                             │
        ┌─────────▼─────────┐                       ┌───────────▼──────────┐
        │ 4A. Derive        │                       │ 4B. Derive           │
        │ Behavior          │                       │ Behavior             │
        │ Fluid             │                       │ Anchored             │
        └─────────┬─────────┘                       └───────────┬──────────┘
                  │                                             │
        ┌─────────▼─────────┐                       ┌───────────▼──────────┐
        │ 5A. Build         │                       │ 5B. Build            │
        │ Atmosphere        │                       │ Atmosphere           │
        │ Local / Fluid     │                       │ Faction-Anchored     │
        └─────────┬─────────┘                       └───────────┬──────────┘
                  │                                             │
                  └──────────────────────┬──────────────────────┘
                                         │
                           ┌─────────────▼──────────────┐
                           │ 6. Expose Quest Logic      │
                           │ Patient / Nurse / Guard    │
                           │ now create conflict        │
                           └─────────────┬──────────────┘
                                         │
                           ┌─────────────▼──────────────┐
                           │ 7. Player Choice           │
                           └─────────────┬──────────────┘
                                         │
                  ┌──────────────────────┴──────────────────────┐
                  │                                             │
        ┌─────────▼─────────┐                       ┌───────────▼──────────┐
        │ 8A. Update City    │                       │ 8B. Guard Reaction   │
        │ Mutable Outcome    │                       │ Faction belief stays │
        │ Loops back         │                       │ locked               │
        └─────────┬─────────┘                       └──────────────────────┘
                  │
                  └─────────────── returns to Step 2A
```

Layer 1 defines the world pressure.

Layer 2 splits that pressure into two states: cities and districts are fluid, while factions stay locked to their core beliefs.

Layer 3 selects the NPC types affected by those pressures.

For each NPC type, I run the same chain:

> Experience → Emotion → Reason → Behavior

Repeated behavior builds atmosphere. Atmosphere exposes quest logic.

A player choice can update the mutable city layer. A faction NPC, such as a guard, can react or change intensity, but one quest does not rewrite the faction belief.

For a shorter version, start with the Method Summary below. The full method document is linked from there.

## Start Here

These are the shortest entry points.

1. [Method Summary](Portfolio/Summaries/Method_Summary.md)  
   Short version of the pressure, layer, NPC, and quest method.

2. [Erit Worldbuilding Summary](Portfolio/Summaries/Erit_Worldbuilding_Summary.md)  
   How the Erit branch grew from a calendar problem into Viriatus, House Ventari, AVD, and Regulatus.

3. [Storybuilding Summary](Portfolio/Summaries/Storybuilding_Summary.md)  
   Short version of the approach to clues, realization, repeated details, and payoff.

4. [Development Process Summary](Portfolio/Summaries/Development_Process_Summary.md)  
   How I am organizing the project and tracking changes over time.

5. [Development Diary Summary](Portfolio/Summaries/Development_Diary_Summary.md)  
   Short version of the working trail from early worldbuilding to the current method tests.

Each summary links to its fuller working document.

## Project Branches

This repository currently has two working branches and one shorter portfolio route.

### Erit Worldbuilding

[Erit_Worldbuilding/README.md](Erit_Worldbuilding/README.md)

The branch I am focused on right now: Viriatus, House Ventari, Regulatus, founding families, Devaar, identity control, medical dependency, NPC behavior, quest pressure, and the world Erit inherits.

### Fragments Story

[Fragments_Story/README.md](Fragments_Story/README.md)

The main story branch: prose, characters, acts, Unity, scene bridges, emotional payoff, and reader perception.

### Portfolio

[Portfolio/README.md](Portfolio/README.md)

The shorter public-facing route with summaries, selected samples, and process notes.

## Repository Structure

- `Erit_Worldbuilding/` — worldbuilding branch for Viriatus, House Ventari, Regulatus, method notes, systems, quests, and the world Erit inherits.
- `Fragments_Story/` — main story branch with project foundation, development history, characters, acts, prose, bridges, cosmology, and reference material.
- `Portfolio/` — shorter public-facing route with summaries, selected samples, case studies, and process notes.

## Note On AI Use

I used AI as a development assistant to help organize, question, and stress-test ideas.

The creative direction, constraints, world logic, character decisions, corrections, and final choices are mine. I used the process to learn faster, not to pretend this is polished professional work.

## Note

This repository is a working record of learning and development, not a finished game portfolio.

The portfolio route is the quickest way to read it.