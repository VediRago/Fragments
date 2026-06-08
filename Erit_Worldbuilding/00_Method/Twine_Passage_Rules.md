# Twine Passage Rules

These rules are for the Vys layer-system prototype. Use them to keep every passage readable, consistent, and game-like while testing systems.

## Core rule

Change one thing at a time. Test after each change. Do not edit CSS, passage structure, and system logic all at once.

## Page types

### Vys hub

The Vys hub is the main player-facing city page.

It should contain:

1. Background state logic
2. City title
3. City premise
4. City mood
5. Street rumor / recent visible change
6. Movement links
7. One quiet Debug Vys link

It should not show raw system values like pressure, trust, or faction score.

Use:

```twine
<span class="hub-title">Vys</span>
<span class="hub-premise">...</span>
<span class="city-mood">...</span>
```

### Debug Vys

Debug Vys is the control room.

It may show:

- city state
- pressure
- layer influence
- current action values
- memories
- trust
- prototype tools

Debug Vys is allowed to look technical. The main Vys hub should not.

### Run Summary

Run Summary is a readable report of the current test run.

It should explain what the system produced in plain language. It is not the same as Debug Vys.

## Standard passage structure for locations

Use this structure for normal places:

```twine
<span class="place-title">Place Name</span>

<span class="place-intro">
Short atmospheric sentence about the place.
</span>

(if: $layer1CityVys is "Regulatus")[
<span class="place-mood">Regulatus-state description.</span>
]

(if: $layer1CityVys is "Contested")[
<span class="place-mood">Contested-state description.</span>
]

(if: $layer1CityVys is "Novacula")[
<span class="place-mood">Novacula-state description.</span>
]

<span class="action-prompt">What do you do?</span>

<span class="world-links">
[[Action text->Passage Name]]
[[Action text->Passage Name]]
</span>

<span class="back-link">
[[Return to Vys->Vys]]
</span>
```

## Link wording rules

Use verb-based links. Links should feel like actions, not menu labels.

Good:

```twine
[[Enter Scutis Headquarters->Scutis Headquarters]]
[[Find the Novacula Hideout->Novacula Hideout]]
[[Walk to the Worker District->Worker District]]
[[Cross into Citizen Square->Citizen Square]]
[[Read the city mood->City Status]]
```

Avoid:

```twine
[[Scutis Headquarters]]
[[Novacula Hideout]]
[[Worker District]]
[[Citizen Square]]
```

## Text style rules

Use these meanings consistently:

- `hub-title`: main city title, currently Vys
- `hub-premise`: short explanation of the city conflict
- `city-mood`: current emotional state of Vys
- `place-title`: title of a normal location
- `place-intro`: first atmospheric sentence for a location
- `place-mood`: state-based description for a location
- `action-prompt`: prompt before player choices
- `world-links`: fiction/player movement links
- `system-links`: prototype/debug links only
- `recent-change`: in-world rumor or visible consequence
- `back-link`: return navigation

## CSS class rules

Do not create a new CSS class unless an existing class cannot do the job.

Recommended classes:

```css
.place-title {
  display: block;
  font-size: 1.35em;
  font-weight: bold;
  color: #f2ead8;
  margin-bottom: 0.45em;
  letter-spacing: 0.03em;
}

.place-intro {
  display: block;
  margin-bottom: 1em;
  color: #e8e2d6;
}

.place-mood {
  display: block;
  margin-bottom: 1em;
  color: #d9cdb8;
}

.action-prompt {
  display: block;
  margin-top: 1em;
  margin-bottom: 0.35em;
  color: #f2ead8;
  font-weight: bold;
}

.back-link {
  display: block;
  margin-top: 1em;
}
```

## Debug display rules

For booleans, do not print the raw variable directly. Use yes/no.

```twine
Worker helped: (if: $helpedWorker)[yes](else:)[no]
Worker reported: (if: $reportedWorker)[yes](else:)[no]
```

## System logic rules

Current action values are temporary.

After pressure is applied, reset:

```twine
(set: $layer2CurrentValue to 0)
(set: $layer3CurrentValue to 0)
```

Influence values are memory/history and should not reset after every action.

## Tone rules

Make the player feel consequences through the world.

Prefer:

```twine
Word in the streets: $recentChange
```

Avoid:

```twine
Last visible change: $recentChange
```

Prefer atmospheric consequence over scoreboard language.

## Backup rule

Before changing layout or CSS, export a working copy of the Twine file.

Suggested name:

```text
Layer System Test - Working Backup.html
```
