# Erit Worldbuilding — Development Diary

This file is the clean migrated diary index for the **Erit Worldbuilding** branch.

The older full diary is preserved as working history, but it should not be treated as the clean canonical starting point until it is split and checked.

## Current Canon Starting Points

Read these files first:

1. [Erit Worldbuilding Case Study](../../Portfolio/Erit_Worldbuilding_Case_Study.md)
2. [Calendar and Eras](../01_History/Calendar_And_Eras.md)
3. [Viriatus and the Origin of Regulatus](../01_History/00_Viriatus_Regulatus_Origin.md)
4. [Regulatus](../01_History/02_Regulatus.md)
5. [House Ventari — Founding Era](../02_Founding_Era/House_Ventari.md)
6. [Ventari Family — Founding Era](../02_Founding_Era/Ventari_Family/README.md)

## Locked Development Rule

The clean Erit files must explain causality clearly.

Use:

> experience -> emotion -> reason -> behavior -> atmosphere -> history

For game-facing material, extend it into:

> experience -> emotion -> reason -> behavior -> atmosphere -> quest logic

No major worldbuilding claim should exist only because it sounds interesting.

## 2026-06-08 — Twine Layer System Finding

Today I began testing the Erit / Vys layer method directly in Twine.

The main finding is that the layers should not be treated as simple reputation bars or direct outcome switches.

The current working model is:

- Layer 1 — City / World State
- Layer 2 — Faction Pressure
- Layer 3 — NPC / Local Behavior

Layer 2 and Layer 3 influence each other's effectiveness, but they do not change each other's identity.

A faction remains itself. Scutis does not become Novacula. Novacula does not become Scutis.

What changes is how strongly their actions land inside the current social condition of Vys.

If Scutis acts while NPC behavior already favors Scutis obedience, the Scutis action gains momentum.

If Scutis acts while NPC behavior favors Novacula resistance, the Scutis action still happens, but its impact is reduced.

The same applies in reverse for Novacula.

NPC behavior also receives pressure from faction conditions. Local obedience spreads more easily when Scutis pressure is strong. Local resistance spreads more easily when Novacula pressure is strong. Opposing faction pressure does not erase NPC behavior, but it reduces how strongly that behavior can affect the city.

This creates the current loop:

```text
NPC action -> Layer 3
Faction action -> Layer 2

Layer 2 and Layer 3 modify each other's effectiveness

Layer 2 + Layer 3 -> Pressure

Pressure -> Layer 1 City State

Layer 1 City State -> future NPC behavior, faction access, location mood, and quest logic
```

The important design correction is:

```text
Actor decides layer.
Pressure decides city.
City decides future context.
```

This means a worker helping hide supplies is Layer 3 because the actor is local / NPC behavior.

A Scutis operation is Layer 2 because the actor is organized faction pressure.

A faction can unlock access to local behavior, but the resulting action still belongs to the layer of the actor carrying it out.

Example:

If Novacula trust unlocks an option to move supplies through the worker district, the action can still resolve through Layer 3 because the visible effect is local worker behavior, rumor, hunger, and district cooperation.

The current Twine implementation is built to scale by keeping quest passages separate from the city-state calculation.

Quest passages only set the current layer value:

```twine
(set: $layer2CurrentValue to 4)
```

or:

```twine
(set: $layer3CurrentValue to -2)
```

The pressure passage aggregates both values:

```twine
(set: $pressureVysControl to $pressureVysControl + $layer2CurrentValue)
(set: $pressureVysControl to $pressureVysControl + $layer3CurrentValue)

(set: $layer2CurrentValue to 0)
(set: $layer3CurrentValue to 0)

(goto: "Layer 1")
```

Layer 1 then checks whether Vys changes state.

The purpose of the Twine prototype is to test whether this produces believable social movement:

- factions push
- NPCs obey, resist, delay, or cooperate
- pressure changes the city
- the changed city alters future behavior
- consequences become systemic instead of individually scripted

This is now the clearest game-facing version of the development rule:

```text
experience -> emotion -> reason -> behavior -> atmosphere -> quest logic
```

## Locked Canon Notes

- House Ventari hides Viriatus's arrival, trains him, teaches him, shapes him, and uses him as an asset for control.
- House Ventari uses public displeasure with the old Rome-derived order to justify replacing it.
- Viriatus becomes military proof that Ventari discipline can produce what the old order could not.
- Viriatus does not create Regulatus.
- After Ecalus dies, Viriatus's living public meaning threatens the siblings' control of what comes next.
- Ermerus turns Ilunis's jealousy and wound into duty.
- Ilunis kills Viriatus privately.
- Ermerus turns public grief into Regulatus.
- ACD / Celcinus Calendar comes before Regulatus.
- AVD begins when Ermerus publicly declares Regulatus, not at the private moment Viriatus dies.
- Regulatus replaces the old order and makes obedience feel like pride, gratitude, duty, belonging, and civilization.

## Migration Note

The old diary may contain earlier wording that has since been corrected, including older phrasing around Viriatus, House Ventari, AVD, and Regulatus.

When there is conflict, use the cleaned files in this folder as the current source.

The old diary should be split into dated entries only after each section is checked for ambiguity.