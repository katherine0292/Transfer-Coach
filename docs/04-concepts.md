# 04 · Concepts

Two concepts were explored against the same phase of the journey: the transfer. Each was framed with a design brief, a rough technology concept, the activities it supports, and why it matters for the user.

## Concept 1: Transfer Coach (decision layer)

*A mobile companion that turns live journey data into one confident next move.*

**Brief.** Help time-pressured commuters decide, in the last minutes of a transfer, whether to run, wait or reroute.
**Supports:** the transfer decision moment, the 3 to 10 minutes before boarding the next service.

**Technology concept**

- A decision layer that sits on top of existing real-time feeds (TripView and Transport for NSW), not a replacement for them
- Converts raw ETAs into one plain confidence signal: Safe, Tight or Unlikely
- Learns each commuter's real walking and interchange pace over time
- Prepares a backup route before a connection actually fails

**Why it matters**

- One glance instead of repeated app-checking. Research showed commuters re-check journey apps even on trips that go fine.
- A clear go-or-wait signal instead of raw numbers. "Cannot decide whether to run" was among the most common stress triggers.
- Confidence that a backup already exists. This answers the false "on time" status that erodes trust.

**Flow:** Monitor, Warn, Direct, Recover.

## Concept 2: Station Flow (walking guidance)

*A walking guidance layer that helps commuters move through transfers confidently, without relying on GPS or station infrastructure.*

**Brief.** Help commuters walk through unfamiliar or crowded interchanges using pre-loaded walking guidance and phone cues.
**Supports:** the physical walk from platform arrival to boarding the next service.

**Technology concept**

- Uses the phone's compass and step count to time turn-by-turn cues
- Vibration and optional earbud audio at each turn for hands-free guidance
- A crowd-sourced "shortcut library" of routes experienced commuters already use

**Why it matters**

- Reliable guidance even underground. Interviewees described walking towards an exit instead of the metro because indoor GPS gave wrong directions.
- Confidence in unfamiliar stations. Several had to ask staff after getting lost.
- A continuous, connected feeling instead of separate lookup moments.

**Flow:** Detect, Orient, Guide, Confirm.

## Decision

| Criterion | Transfer Coach | Station Flow |
|---|---|---|
| Addresses the research low point (the transfer decision) | Direct | Partial, covers the walk only |
| Addresses the trust problem (false "on time") | Direct | Indirect |
| Addresses wayfinding without GPS | Not by itself | Direct |
| Prototype feasibility | High. A data and interaction challenge, prototypable with public real-time feeds and standard front-end tooling | High. App-based, but sensor-timed cues are hard to simulate in a clickable prototype |

**Selected: Transfer Coach, with the guidance need from Station Flow folded in.** The final design keeps the decision layer as the core and adds pre-loaded, landmark-based station steps (exit choice, level changes, turns, crossings). These need no GPS and no station infrastructure. Sensor-timed haptic cues and a shortcut library were left out of the prototype and are listed as next steps.
