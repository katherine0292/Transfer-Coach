# 06 · Evaluation

Three complementary evaluations, each answering a different question.

| Evaluation | Prototype | Question | Evidence |
|---|---|---|---|
| Expert heuristic review | Mid fidelity (v2) | What are the likely problems, found cheaply and early? | Review against Nielsen's ten usability heuristics, re-checked on v3 |
| Scenario-based usability testing | Mid fidelity (v2) | Can people complete the core transfer tasks, and where do they struggle? | 7 commuters, 3 scenarios, think-aloud, about 5 to 10 minutes each |
| Experience evaluation | High fidelity (v3) | What does a disrupted trip feel like, and why? | 2 structured experience journals, plus 1 supporting journal from a usability session |

All sessions ran on demo data. Nothing was connected to live services.

## 1 · Expert heuristic review

Findings that shaped the first redesign:

- A missed or delayed service left the user without a clear decision.
- The "Danger" confidence label could alarm people.
- Station wording was technical and text-heavy.
- There was no "Can't find it?" escape on the station steps.

The review was repeated on the high-fidelity screens after the redesign.

## 2 · Usability testing (7 commuters, 3 scenarios)

**Participants.** Seven people who make at least two transfers on regular trips, none involved in the design. No requirements were set for age, gender or background. Sessions took place face to face between 1 and 17 October 2026.

**Session format.** Welcome and consent, think-aloud instructions, a scenario card, tasks, a planned disruption (the clock was moved forward and the participant told what a real traveller would see), and a debrief with ease and confidence ratings on a 1 to 5 scale. Where screens were not linked, the screens were advanced by hand (Wizard of Oz).

**Scenarios**

| Scenario | Situation | Features tested |
|---|---|---|
| 1 · Running late | Job interview at 10:00, on the train towards Central | Transfer alert, "Can I make it?", exit choice, step-by-step guidance |
| 2 · Concert day, bus delayed | A traffic accident delays Bus 343 by about 8 minutes at Stand C | Delay handling, missed connection, backup routes, route confirmation |
| 3 · Concert trip, train delayed | The first train is 3 minutes late and there is no spare time in an unfamiliar station | Low-confidence warning, station guidance, recovery |

**Severity scale:** Severe (user cannot continue, or the app shows wrong information), High (finishes but doubts the app; could cause a missed connection), Medium (hesitates and recovers), Low (small wording or visual issue).

### What worked

- The "Can I make it?" breakdown, for example "6 min to departure, 3 min walk, 3 min buffer", was much clearer than a "High" label alone.
- Step-by-step station directions ("Step 1 of 3") with real landmarks.
- Calm wording after a missed connection ("You still have options").
- One participant rated ease about 4 out of 5, and another found it more useful than a general maps app "because it is step by step".

### What failed

Trust dropped when the real world and the app disagreed. Confidence in arriving on time was 3 to 3.5 out of 5 in the delay scenario.

| # | Finding | Severity |
|---|---|---|
| 1 | No "delayed" state. The app showed "2 min" while the stop display showed 8 minutes late, and the only option was "The bus has already left". One participant said it "felt like I was lying to the app". | Severe |
| 2 | "Transfer complete" appeared at the stand, before boarding | High |
| 3 | Backup routes were hard to compare: arrival time was small grey text, the recommended route was slower, and delay status of other routes was unknown | High |
| 4 | Participants compared every time with their deadline in their heads | High |
| 5 | After choosing a new route there was no way to start guidance | High |
| 6 | "High" confidence could not be trusted when the bus was visibly stuck | High |
| 7 | "Indoor position is approximate" made participants nervous; nothing said what to do if the map dot was wrong | Medium |
| 8 | A calm "No need to rush" message clashed with real time pressure | Medium |
| 9 | "Level +1" and "Level route from here" felt technical and looked like links | Low |

### Recommendations and their status

13 recommendations were produced, each linked to the findings above.

| Status | Count | Examples |
|---|---|---|
| Fully built into the high-fidelity prototype | 8 | Bus delayed state; "You're at Stand C"; rebuilt route cards; navigation after a route change; live status card on every in-progress screen; plain words and pictograms |
| Partly built | 4 | Time against the user's deadline ("min to spare" shown, editable arrive-by not yet); live-data labels (on some screens only); decision on warning screens; help when position looks wrong |
| Open | 1 | An editable trip preference |

## 3 · Experience evaluation (2 journals)

**Why a second method.** Usability testing asks whether people can complete tasks. Experience evaluation asks what the trip is like: how confidence, control, stress and trust change over a disrupted journey, and why.

**Approach.** Each journal participant stepped into a written user experience story with the high-fidelity prototype and recorded the experience in a structured journal covering the technology, the user, the activity, the environment and the social context. Sessions took about 7 minutes. One story followed an 8-minute bus delay on the way to a concert; the other followed a train delay while travelling with a friend.

### Results

Both journal participants felt more in control when a delay happened: they were warned early, the amber "Walk a bit faster" card gave them an action, and "Not affected" routes gave relief. Remaining stress came from four experience problems:

| # | Experience problem | Change |
|---|---|---|
| 1 | Time was shown against the bus, but people judged the trip against the event, so they still did mental maths under pressure | Lead with arrival time and minutes before the event |
| 2 | They could not tell whether the new arrival time already included the delay | State "delay included" |
| 3 | During the bus leg it was unclear which stage they were in | Stage labels and a stop list with boarded, next and get-off stops |
| 4 | Delay information lived on a separate Alerts tab, and the selected route was not clearly confirmed, which led to one wrong-route start | Show impact inside the trip; name the selected route on the Start button |

Journal 2 added that switching between directions and trip status broke concentration, and that the fixed event time was the strongest negative factor throughout.

**Reading these results.** The journals come from two people, so they show what can affect the experience, not how often it happens.

## Traceability: finding to change to screen

| Finding | Design change | Final screens |
|---|---|---|
| No delayed state; app contradicted the stop display | Delayed state with struck-through old time, new time, "+8 min", delay included, "Updated 10:04" | 12, 31 |
| "Transfer complete" shown before boarding | "You're at Stand C"; arrival confirmed only at the end | 29, 35 |
| Hard-to-compare backup routes | Cards lead with arrival time, then wait or walk and minutes before the event | 13, 15, 32, 36 |
| Mental maths against the deadline | "Min before 10:30" on route, transfer and trip screens | 03, 10, 21 |
| No way to start after changing route | Choosing an option leads to guidance | 16, 37 |
| Station wording too technical | Pictograms, "Head downstairs", step counter | 09, 22, 25 to 28 |
| Uncertainty when the position was wrong | Landmark match and "Fix my position" | 22, 23 |
| Unclear trip stage on the bus | Stop list with boarded, next and get-off stops | 11, 34 |
| No recovery for a wrong stop | Dedicated three-screen recovery flow via T5 | 18 to 20 |

## Limitations

- **Setting.** Sessions took place at public venues, apartments or similar places, not inside a station under real time pressure.
- **Sample.** Seven usability participants and two experience journals. Findings are qualitative.
- **Participant familiarity.** The two journal participants knew the project goals and were not recruited blind.
- **Need coverage.** None of the participants whose needs were recorded needed step-free access, and several did not know Central Station well.
- **Data.** Demo data only. Accuracy of live predictions was not tested.
- **Retest.** The final prototype has not been retested with commuters.
