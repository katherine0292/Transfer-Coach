# 07 · Outcomes and next steps

## What the project delivered

- A 38-screen high-fidelity design for a transfer assistance feature, covering the normal flow and five disruption types: delayed train, missed train, delayed bus, missed bus and wrong stop.
- An interactive web prototype with every branch wired, six disruption triggers and a design-notes panel that ties each screen to evidence.
- A research and evaluation trail where each major design change traces to a finding.

## What changed in my thinking

1. **From features to moments.** The design started from one real moment, the 3 to 10 minutes in which a commuter decides to run, wait or reroute, instead of from a feature list.
2. **From opinion to evidence.** The designer heuristic review, seven usability sessions and two experience journals changed the screens four times. Each change in [06-evaluation.md](06-evaluation.md) names its source.
3. **From usable to felt.** An app can be easy to use and still leave people anxious. Experience evaluation found stress, such as unclear delay inclusion and trip stage, that task-based testing did not.

## Product perspective: designing the interface for a prediction

The prototype uses scripted data, but the interface is designed for a system that predicts. These are the principles I would carry into any AI-assisted product:

| Principle | How it shows up here |
|---|---|
| Calibrate trust, do not ask for it | A single "High confidence" label was not believed when it contradicted the stop display. The design shows its basis instead: live label, update time, delay included |
| Make the impact explicit | Every status states what it means for the destination, not only the next vehicle |
| Keep humans in control | "I missed it", "Fix my position" and the option to keep the original plan stay available whenever live data and the real world differ |
| Prefer the next action to the explanation | Amber "Walk a bit faster" gave people something to do. The status always comes with a move |
| Be proactive about impact, not volume | Alerts describe consequences for this trip and open the affected leg |
| Fail visibly | If live data is missing, the interface should say "Timetable" instead of implying it is live (open recommendation) |

## Open items and next steps

| Priority | Item | Rationale |
|---|---|---|
| 1 | Retest the final prototype with commuters in a real station | The most important missing context, since sessions took place away from stations |
| 2 | Editable arrive-by input on the trip screen | The only usability recommendation not yet built; people think in deadlines |
| 3 | Complete live-data labelling ("Live", "Timetable") on every status | Partly built; trust depends on it |
| 4 | Add a preview step on low-confidence warnings | Lets people compare continuing against switching without replacing the plan |
| 5 | "Position looks wrong?" on each guidance step | Currently reachable from one screen only |
| 6 | Prototype the personalisation concept | Learn each commuter's real walking pace and prepare backups before a connection fails, with controls and a clear explanation of what is learned |
| 7 | Test step-free and accessibility needs with participants who need them | None of the recorded participants did |
| 8 | Measure prediction quality against real feeds | Needed before any confidence signal is trustworthy |

## Suggested metrics for a live product

- Share of transfers completed without a missed connection
- Time from disruption to a chosen backup
- Wrong-route starts
- Rate of unprompted "I missed it" taps (a proxy for the app contradicting reality)
- Self-reported confidence at the moment of transfer
