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

This is not a finished game.

Right now, I am using this repo to track how I build connected worldbuilding, character logic, NPC behavior, atmosphere, and quest structure.

What I am focused on right now is the Erit worldbuilding branch, where I am testing whether world pressure can create believable factions, NPCs, quests, and consequences instead of treating them as separate pieces.

## Current Working Method

While building Erit's world, I started writing down a method for connecting worldbuilding, factions, NPCs, atmosphere, and quests through cause and consequence.

The first worldbuilding chain used for Viriatus, House Ventari, and the family foundation was:

> Pressure → Experience → Emotion → Reason → Behavior

Later testing added **Atmosphere** as the result of repeated behavior:

> Pressure → Experience → Emotion → Reason → Behavior → Atmosphere

After that, I added **Layers** to explain why different cities, factions, districts, or NPCs can experience similar pressure but react differently.

For quests, the test expanded into:

> Starting Layer → Pressure → Experience → Emotion → Reason → Behavior → Atmosphere → Quest Logic → Player Choice → Consequence → Possible Layer Outcome

The main finding so far is that behavior and atmosphere often do not need to be forced separately. When the earlier steps are clear, behavior tends to appear naturally. When behavior repeats across a place, group, or NPC, atmosphere begins to appear. Quests can then be found inside that atmosphere instead of being placed on top of it.

```mermaid
flowchart TD
    A[Pressure] --> B[Experience]
    B --> C[Emotion]
    C --> D[Reason]
    D --> E[Behavior]
    E --> F[Atmosphere]
    F --> G[Quest Logic]
    G --> H[Player Choice]
    H --> I[Consequence]

    I --> J[Reinforce Layer]
    I --> K[Weaken Layer]
    I --> L[Shift Layer]

    J --> M[Future Behavior]
    K --> M
    L --> M
    M --> N[Future Atmosphere]
```

This simplified loop shows the current test model: pressure creates experience, experience creates emotion, emotion creates reason, and reason creates behavior. Atmosphere was added later after testing showed that repeated behavior could make the world feel coherent. Quests can create player choices and consequences. Those consequences may reinforce, weaken, or shift mutable layers as outcomes. Layer outcomes can shape future behavior, and changed behavior can affect future atmosphere.

Full document:

[Method Creation Examples](Erit_Worldbuilding/00_Method/Method_Creation_Examples.md)

## Start Here

Recommended reading order:

1. [Method Summary](Portfolio/Summaries/Method_Summary.md)  
   Short version of the pressure / layer / NPC / quest method.

2. [Erit Worldbuilding Case Study](Portfolio/Erit_Worldbuilding_Case_Study.md)  
   Portfolio-facing overview of the Erit worldbuilding branch.

3. [Current Storybuilding Approach](Portfolio/Current_Storybuilding_Approach.md)  
   Short explanation of clues, repeated details, reveals, and payoff.

4. [Development Process](Portfolio/Development_Process.md)  
   How I am organizing the project and tracking decisions.

5. [Method Creation Examples](Erit_Worldbuilding/00_Method/Method_Creation_Examples.md)  
   Full working document with examples, tests, and current conclusions.

6. [Development Diary](Erit_Worldbuilding/00_Development/Diary_Method_Validation.md)  
   Rawer notes showing how the method evolved during testing.

The first links are shorter summaries. The full method file and diary are there for anyone who wants to see the working trail behind the summaries.

## Project Branches

This repository currently contains two connected project branches and one public-facing branch.

### Erit Worldbuilding

[Erit_Worldbuilding/README.md](Erit_Worldbuilding/README.md)

What I am focused on right now: Viriatus, House Ventari, Regulatus, founding families, Devaar, identity control, medical dependency, NPC behavior, quest pressure, and the world Erit inherits.

### Fragments Story

[Fragments_Story/README.md](Fragments_Story/README.md)

The main story branch: prose, characters, acts, Unity, scene bridges, emotional payoff, and reader perception.

### Portfolio

[Portfolio/README.md](Portfolio/README.md)

A shorter public-facing branch with clean summaries, selected samples, and learning-process notes. This is useful for a quick overview, but it is not the full development trail.

## Worldbuilding Process

For the shorter case-study version, read:

[Erit Worldbuilding Case Study](Portfolio/Erit_Worldbuilding_Case_Study.md)

For the full working-process version of Erit's worldbuilding, read:

[Erit Worldbuilding — Development Diary](Erit_Worldbuilding/Development_Diary/00_Development_Diary.md)

The diary shows what questions appeared, why details mattered, what connected back to Fragments, and what had to stay constrained so the main story remained intact.

The current worldbuilding method I am testing is documented here:

[Method Creation Examples](Erit_Worldbuilding/00_Method/Method_Creation_Examples.md)

The repo-wide clarity rule is here:

[Canon Clarity Rules](Erit_Worldbuilding/00_Method/Canon_Clarity_Rules.md)

## Repository Structure

- `Erit_Worldbuilding/` — worldbuilding branch for Viriatus, House Ventari, Regulatus, method notes, systems, quests, and the world Erit inherits.
- `Fragments_Story/` — main story branch with project foundation, development history, characters, acts, prose, bridges, cosmology, and reference material.
- `Portfolio/` — shorter public-facing route with the overview, samples, case study, and process notes.

## Note On AI Use

I used AI as a development assistant to help organize, question, and stress-test ideas.

The creative direction, constraints, world logic, character decisions, corrections, and final choices are mine. I used the process to learn faster, not to pretend this is polished professional work.

## Note

This repository is a working record of learning and development, not a finished game portfolio.

The current evidence of the process is in the Erit worldbuilding files. The portfolio route is shorter and cleaner, but it does not contain the full development trail.
