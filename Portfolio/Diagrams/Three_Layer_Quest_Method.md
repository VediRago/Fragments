# Three-Layer Quest Method

This diagram shows the method layout used in the quest test. The positions matter:

- The left side is the mutable city/district path.
- The right side is the locked faction path.
- Local NPCs and faction NPCs both pass through the same core method.
- Player consequence can update the city layer.
- The guard can respond, but faction belief stays locked.

```mermaid
flowchart TD
    L1[Layer 1: World Pressure / Events<br/>Medical control<br/>Identity records<br/>Surveillance]

    L1 --> C[Layer 2A: City / District<br/>Mutable]
    L1 --> F[Layer 2B: Faction<br/>Locked]

    C --> P[Layer 3: Patient<br/>Denied medicine]
    C --> N[Layer 3: Nurse<br/>Watches patients suffer]
    F --> G[Layer 3: Guard<br/>Protects faction order]

    P --> PM[Experience → Emotion → Reason → Behavior<br/>Fear → survival logic → trades papers]
    N --> NM[Experience → Emotion → Reason → Behavior<br/>Guilt → lying saves people → alters logs]
    G --> GM[Experience → Emotion → Reason → Behavior<br/>Suspicion → false records hide rebels → searches harder]

    PM --> A[Atmosphere<br/>Clinic feels watched,<br/>tense, guilty]
    NM --> A
    GM --> A

    A --> Q[Quest Logic<br/>Mismatched records reveal conflict]

    Q --> CH[Player Choice / Consequence]

    CH --> CU[Mutable City Outcome<br/>Trust, fear, access, or unrest shifts]
    CH --> GU[Guard Outcome<br/>Behavior can intensify or soften<br/>Faction belief does not change]

    CU --> C
```

## Read Order

**Layer 1 — World Pressure / Events**  
Large forces shape the setting: medical control, identity records, surveillance.

**Layer 2A — City / District**  
Mutable. Local trust, fear, access, and unrest can shift through player consequence.

**Layer 2B — Faction**  
Locked. Doctrine and core beliefs do not change because of one quest.

**Layer 3 — NPC Types**  
Patient, nurse, and guard experience the same pressure differently.

**Core Method**  
Experience → Emotion → Reason → Behavior → Atmosphere → Quest Logic

**Outcome Rule**  
The mutable city layer can change. The guard can respond, but the faction belief remains locked.