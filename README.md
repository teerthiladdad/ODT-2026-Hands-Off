# Open Design and Technology  
## Final Project README

> **Project Weight:** 70%  
> **Team Size:** 2 students  
> **Project Duration:** 4 weeks  
> **Class Time Available:** 6 hours per class  
> **Total Time Available:** 48 effort-hours per team  
> **Project Type:** Playful, interactive, technology-based experience

---

# Before you begin

## Fork and rename this repository
After forking this repository, rename it using the format:

`ODT-2026-TeamName`

### Example
`ODT-2026-ClawSnatcher`

Do not keep the default repository name.

---

# How to use this README

This file is your team’s **working project document**.

You must keep updating it throughout the 4-week build period.  
By the final review, this README should clearly show:
- your idea,
- your planning,
- your design decisions,
- your technical process,
- your build progress,
- your testing,
- your failures and changes,
- your final outcome.

## Rules
- Fill every section.
- Do not delete headings.
- If something does not apply, write `Not applicable` and explain why.
- Add images, screenshots, sketches, links, and videos wherever useful.
- Update task status and weekly logs regularly.
- Use this file as evidence of process, not only as a final report.

---

# 1. Team Identity

## 1.1 Studio / Group Name
`[Enter your group name]`

## 1.2 Team Members

| Name | Primary Role | Secondary Role | Strengths Brought to the Project |
|---|---|---|---|
| `[Aarav Srivastava]` | `[Coding / App / Mechanics]` | `[Testing]` | `[Logic design, MicroPython scripting, debugging hardware-software bridges]` |
| `[Teerthi Laddad]` | `[Electronics / Fabrication / Mechanics]` | `[Role]` | `[Write here]` |

## 1.3 Project Title
`Hands Off`

## 1.4 One-Line Pitch
`[A two-player cooperative game where players must use strings to smoothly extract a bomb from a mechanical claw before it detects their movement and snaps shut.]`

## 1.5 Expanded Project Idea
In 1–2 paragraphs, explain:
- what your project is,
- what kind of playful experience it creates,
- what makes it fun, curious, engaging, strange, satisfying, competitive, or delightful,
- what technologies are involved.

**Response:**  
This project is a physical, interactive game built around tension, balance, and coordination between two players. At the center of the setup is a claw-like structure holding an object suspended by strings. Each player controls one string and must work together to lift the object smoothly within a time limit.

The challenge lies in maintaining controlled motion, any sudden or uneven movement risks failure. If the players succeed, they retrieve the object safely. If they fail or run out of time, a servo-triggered mechanism activates, causing the claw to close and trap the object.

The experience is designed to feel tense, slightly stressful, and engaging, encouraging communication and repeated attempts. It combines mechanical design, electronics, and physical interaction.
---

# 2. Philosophy Fit

## 2.1 Experience, Not Social Problem
This module does **not** require your project to solve a large social problem.

You are allowed to build:
- toys,
- games,
- interactive objects,
- playful machines,
- kinetic artifacts,
- humorous devices,
- strange but delightful experiences,
- things that are entertaining to use or watch.

## 2.2 What kind of experience are you creating?
Answer the following:
- What is the experience?
- What do you want the player or participant to feel?
- Why would someone want to try it again?

**Response:**  
`[What is the experience?
A cooperative two-player retrieval game where both players must move a prop bomb out of a mechanical claw trap using only gentle, coordinated pulling on two attached strings, without triggering the snap mechanism.
What do you want the player or participant to feel?
Nervous, focused, and connected to their partner. Success should feel like a genuine release of tension. Failure should provoke laughter and the immediate desire to try again.
Why would someone want to try it again?
Because losing feels like almost succeeding, and the physicality of the mechanism makes each round feel fresh. Players will want to beat their own coordination and improve their technique.]`

## 2.3 Design Persona
Complete the sentence below:

> We are designing this project as if we are a small creative studio making a **[toy / game / playable object / interactive experience]** for **[children / teens / adults / classmates / exhibition visitors / mixed audience]**.

**Response:**  
`[We are designing this project as if we are a small creative studio making a playable kinetic installation for classmates and exhibition visitors who want a quick, memorable, high-stakes cooperative experience.]`

---

# 3. Inspiration

## 3.1 References
List what inspired the project.

| Source Type | Title / Link | What Inspired You |
|---|---|---|
| `[Movie Scene]` | `[Indiana Jones: Raiders of the Lost Ark (Idol Scene)]` | `[The concept of replacing/stealing an object off a weight/pressure plate without triggering the environment.]` |
| `[Object]` | `[Mechanical claw machines (arcade)]` | `[The visual drama of a claw opening and closing]` |
| `[Toy]` | `[Fishing game(with fishing rod where you have to pick up the fishes)]` | `[The concept of snatching something with time as a variable]` |

## 3.2 Original Twist
What makes your project original?

**Response:**  
`[Most tension games rely on digital feedback or buzzers. Our project uses a fully physical consequence, a weighted claw that mechanically snaps shut, making the stakes feel tangible and real. The two-string cooperative input (rather than a single player) adds a coordination layer that is unusual in physical game design.]`

---

# 4. Project Intent

## 4.1 Core Interaction Loop
Describe the main loop of interaction.

Examples:
- press → launch → score → reset
- connect → control → observe → repeat
- turn → trigger → react → repeat
- move object → sensor detects → sound/light response → player reacts

**Response:**  
`[hold strings → coordinate movement → lift object → maintain stability → beat timer → win OR trigger claw → lose]`

## 4.2 Intended Player / Audience

| Question | Response |
|---|---|
| Who is this for? | `[Anyone who enjoys physical puzzle/skill games.]` |
| Age range | `[10+ (Requires fine motor skills)]` |
| Solo or multiplayer | `[2-Player Co-op ]` |
| Expected duration of one round | `[10 to 15 seconds]` |
| What should the player feel? | `[Nervous excitement, focus, shared responsibility]` |
| Is explanation required before use? | `[Minimal- one sentence of instruction is enough]` |

## 4.3 Player Journey
Describe exactly how a player will use the project.

1. **Approach:** `[The player sees a black-and-gold claw structure with a bomb-like object resting inside an open claw. Two strings dangle from it.]`
2. **Start:** `[A second player picks up the other string. The timer is started.]`
3. **First Action:** `[Both players begin gently pulling their strings upward together.]`
4. **Main Interaction:** `[Players must coordinate the lift — moving smoothly and slowly to avoid triggering the ultrasonic sensor threshold that signals abrupt motion.]`
5. **System Response:** `[The ESP32 monitors motion data from the ultrasonic sensor. If movement is too abrupt, or if the timer runs out, the servo releases the counterweight, the ring rises, and the claw snaps shut around the bomb.]`
6. **Win / Lose / End Condition:** `[ Win condition-The bomb is lifted clear of the claw before the timer expires without triggering the snap mechanism. Lose condition-Abrupt motion detected, or time runs out, servo fires, claw closes.]`
7. **Reset:** `[The counterweight is manually re-hooked, the claw is opened, the bomb is replaced, and the next round begins.]`

## 4.4 Rules of Play
If your project is a game, list the rules clearly.

- `[Rule 1: Both players must hold one string each — you may not hold both..]`
- `[Rule 2: Lift the bomb upward together without jerking or sudden movements.]`
- `[Rule 3: The bomb must be fully lifted clear before the timer ends.]`
- `[Rule 4: If the claw closes, you lose that round]`

---

# 5. Definition of Success

## 5.1 Definition of “Playable”
Your project will be considered complete only if these conditions are met.

- [ ] `[Condition 1: The claw opens and closes reliably using the ring-and-pulley mechanism]`
- [ ] `[Condition 2:The servo releases the counterweight on a trigger signal from the ESP32]`
- [ ] `[Condition 3:The ultrasonic sensor successfully detects abrupt upward motion and sends a trigger.]`
- [ ] `[Condition 4;A round can be completed from start to finish without physical intervention]`
- [ ] `[Condition 5:The mechanism can be reset and replayed at least ten times without any mechanical failure]`

## 5.2 Minimum Viable Version
What is the smallest version of this project that still delivers the core experience?

**Response:**  
`[A single claw mechanism that snaps shut when an object is removed too quickly from an ultrasonic sensor, powered by a laptop.]`

## 5.3 Stretch Features
What features are nice to have but not essential?

- `[Stretch feature 1 Dual-servo synchronized movement for heavier claws.]`
- `[Stretch feature 2 Audible countdown buzzer]`
- `[Stretch feature 3 Digital score display showing fastest successful retrieval time]`

---

# 6. System Overview

## 6.1 Project Type
Check all that apply.

- [x] Electronics-based
- [x] Mechanical
- [x] Sensor-based
- [ ] App-connected
- [x] Motorized
- [ ] Sound-based
- [ ] Light-based
- [ ] Screen/UI-based
- [x] Fabricated structure
- [x] Game logic based
- [x] Installation / tabletop experience
- [ ] Other: `[Write here]`

## 6.2 High-Level System Description
Explain how the system works in simple terms.

Include:
- input,
- processing,
- output,
- physical structure,
- app interaction if any.

**Response:**  
`[The project is an electromechanical trap. An ultrasonic sensor sits at the base, looking straight up at an object. An ESP32 reads this sensor every 100ms. If the variation in distance spikes, the ESP32 sends a PWM signal to two SG90 servos. The servos are connected to MDF claws via rigid wire pushrods. When the servos rotate, they push the rods, snapping the claws shut. An MIT App Inventor app connects to the ESP32 via BLE to send Arm/Disarm signals.]`

## 6.3 Input / Output Map

| System Part | Type | What It Does |
|---|---|---|
| `[Ultrasonic Sensor]` | Input | `[Constantly measures the height of the object.]` |
| `[ESP32]` | Processing | `[Reads sensor, runs timer, evaluates trigger threshold, fires servo]` |
| `[Servo motors]` | Output | `[Releases counterweight latch when triggered]` |
| `[Counterweight + Pulley]` | Physical Action | `[Drops when released; pulls sleeve ring upward]` |
| `[Sliding Ring + Wire Linkage]` | Physical Action | `[Translates upward ring motion into closing claw arms]` |
| `[MDF Claw Assembly]` | Physical Action | `[Closes around the bomb prop, ending the round]` |

---

# 7. Sketches and Visual Planning

## 7.1 Concept Sketch
Add an early sketch of the full idea.

**Insert image below:**  
`[Upload image and link here]`

Example:
```md

```

## 7.2 Labeled Build Sketch
Add a sketch with labels showing:
- structure,
- electronics placement,
- user touch points,
- moving parts,
- output elements.

**Insert image below:**  
`[Upload image and link here]`

## 7.3 Approximate Dimensions

| Dimension | Value |
|---|---|
| Length | `[10- 12 cm]` |
| Width | `[10- 12 cm]` |
| Height | `[35- 40 cm]` |
| Estimated weight | `[1 kg]` |

---

# 8. Mechanical Planning

## 8.1 Mechanical Features
Check all that apply.

- [ ] Gears
- [ ] Pulleys
- [ ] Belt drives
- [x] Linkages
- [x] Hinges
- [x] Shafts
- [ ] Springs
- [ ] Bearings
- [ ] Wheels
- [x] Sliders
- [x] Levers
- [ ] Not applicable

## 8.2 Mechanical Description
Describe the mechanism and what it is meant to do.

**Response:**  
`[The claw uses an umbrella-rib-style mechanism. Six MDF arms are arranged radially and pinned at pivot points to a central vertical column (PVC pipe). Each arm is connected by a thin wire or cord to a hollow cylinder sleeve that slides along the PVC pipe. When the sleeve is pushed up, the wires pull the tips of the arms inward, closing the claw. When the sleeve drops, the arms fall open under gravity.
The sleeve is connected via cord over a pulley to a counterweight. In the ready state, the servo holds the counterweight in an elevated position, keeping the sleeve down (claw open). When the servo fires, the counterweight drops, the cord pulls the sleeve upward, and the claw closes.]`

## 8.3 Motion Planning
If something moves, explain:
- what moves,
- what causes the movement,
- how far it moves,
- how fast it moves,
- what could go wrong.

**Response:**  
`[The primary movement in the system involves the sleeve, the claw arms, and the suspended object. The sleeve is positioned around a vertical PVC pipe and can slide up and down along its length. Each segment of the claw is connected to this sleeve through wires, forming an umbrella-like mechanism.

During gameplay, the object at the center is lifted by the players through controlled tension in the strings. As the players pull, the object moves upward, and its motion depends on how evenly and smoothly the forces are applied. Any imbalance causes unstable or jerky movement, increasing the difficulty of control.

Once the time limit is reached, a servo motor is activated. The servo releases a mechanism connected to a weighted pulley system. As the weight drops due to gravity, it pulls on the connected system, causing the sleeve to move upward along the PVC pipe. This upward motion of the sleeve pulls the wires attached to each claw segment, resulting in the claw arms closing inward.

The speed of this closing motion is determined by the weight and the friction between the sleeve and the pipe. If the motion is too fast, the claw may snap shut abruptly; if too slow or if friction is too high, the mechanism may not function smoothly.

Potential issues include excessive friction causing the sleeve to get stuck, uneven tension in the wires leading to asymmetrical claw movement, and uncontrolled weight drop resulting in harsh or inconsistent closing behavior. Proper alignment and surface finishing are critical to ensuring smooth and reliable motion.]`

## 8.4 Simulation / CAD / Animation Before Making
If your project includes mechanical motion, document the digital planning before fabrication.

| Tool Used | File / Link | What Was Tested |
|---|---|---|
| `[Fusion 360 / Tinkercad / other]` | `[Link or screenshot]` | `[What did you validate?]` |
| `[Tool]` | `[Link or screenshot]` | `[What did you validate?]` |

## 8.5 Changes After Digital Testing
What changed after the CAD, animation, or simulation stage?

**Response:**  
`[Write here]`

---

# 9. Electronics Planning

## 9.1 Electronics Used

| Component | Quantity | Purpose |
|---|---:|---|
| `[ESP32]` | `1` | `[Main controller- reads sensor, runs timer, fires servo]` |
| `[HC-SR04 Sensor]` | `[1]` | `[Detects bomb position and rate of motion change]` |
| `[SG90 Micro Servo]` | `[2]` | `[Holds and releases counterweight]` |
| `[Power Supply]` | `[1]` | `[provide power to all electronics]` |

## 9.2 Wiring Plan
Describe the main electrical connections.

**Response:**  
`[The ESP32 is powered via USB. The Servos are powered directly from the 5V Power Supply module. The Ground of the 5V supply is wired to the Ground of the ESP32 to ensure the PWM data signal is read correctly.
Ultrasonic: TRIG to Pin 5, ECHO to Pin 18.
Servos: Left Signal to Pin 21, Right Signal to Pin 22.]`

## 9.3 Circuit Diagram
Insert a hand-drawn or software-made circuit diagram.

**Insert image below:**  
`[Upload image and link here]`

## 9.4 Power Plan

| Question | Response |
|---|---|
| Power source | `[Power supply module]` |
| Voltage required | `[5V for servo and HC-SR04; ESP32 regulated internally to 3.3V]` |
| Current concerns | `[Servo draw at stall can spike]` |
| Safety concerns | `[Write here]` |

---

# 10. Software Planning

## 10.1 Software Tools

| Tool / Platform | Purpose |
|---|---|
| `[Thonny / MicroPython]` | `[Writing the core code]` |
| `[Illustrator]` | `[create file for laser cutting]` |

## 10.2 Software Logic
Describe what the code must do.

Include:
- startup behavior,
- input handling,
- sensor reading,
- decision logic,
- output behavior,
- communication logic,
- reset behavior.

**Response:**  
`[The code boots up and runs a calibration sequence to ignore startup sensor glitches (Ghost echoes). It then enters a while loop, checking the distance. It calculates variation = abs(current_distance - previous_distance). If variation > 2.5, it fires the servos. It also utilizes hardware interrupts to listen for BLE strings from the mobile app to override the game state.]`

## 10.3 Code Flowchart
Insert a flowchart showing your code logic.

Suggested sequence:
- start,
- initialize,
- wait for input,
- read input,
- decision,
- trigger output,
- repeat or reset,
- error handling.

**Insert image below:**  
`[Upload image and link here]`

## 10.4 Pseudocode

```text
[Write your pseudocode here]
```

---

# 11. MIT App Inventor Plan

## 11.1 Is an app part of this project?
- [ ] Yes
- [x] No

If yes, complete this section.

## 11.2 Why is the app needed?
Explain what the app adds to the experience.

Examples:
- remote control,
- score tracking,
- mode selection,
- personalization,
- triggering effects,
- displaying data.

**Response:**  
`[Write here]`

## 11.3 App Features

| Feature | Purpose |
|---|---|
| `[Bluetooth connect button]` | `[Purpose]` |
| `[Score display]` | `[Purpose]` |
| `[Control button / slider / label]` | `[Purpose]` |

## 11.4 UI Mockup
Insert a sketch or screenshot of the app interface.

**Insert image below:**  
`[Upload image and link here]`

## 11.5 App Screen Flow

1. `[Step 1]`
2. `[Step 2]`
3. `[Step 3]`
4. `[Step 4]`

---

# 12. Bill of Materials

## 12.1 Full BOM

| Item | Quantity | In Kit? | Need to Buy? | Estimated Cost | Material / Spec | Why This Choice? |
|---|---:|---|---|---:|---|---|
| `[ESP32]` | `1` | `Yes` | `No` |
| `[MDF Board]` | `[1]` | `[Yes]` | `[No]` |
| `[Item]` | `[Qty]` | `[Yes/No]` | `[Yes/No]` | `[Cost]` | `[Spec]` | `[Reason]` |

## 12.2 Material Justification
Explain why you selected your main materials and components.

Examples:
- Why acrylic instead of cardboard?
- Why MDF instead of 3D print?
- Why servo instead of DC motor?
- Why bearing instead of a plain shaft hole?

**Response:**  
`[Write here]`

## 12.3 Items to Purchase Separately

| Item | Why Needed | Purchase Link | Latest Safe Date to Procure | Status |
|---|---|---|---|---|
| `[Item]` | `[Reason]` | `[Link]` | `[Date]` | `[Pending / Ordered / Received]` |
| `[Item]` | `[Reason]` | `[Link]` | `[Date]` | `[Pending / Ordered / Received]` |

## 12.4 Budget Summary

| Budget Item | Estimated Cost |
|---|---:|
| Electronics | `[Cost]` |
| Mechanical parts | `[Cost]` |
| Fabrication materials | `[Cost]` |
| Purchased extras | `[Cost]` |
| Contingency | `[Cost]` |
| **Total** | `[Cost]` |

## 12.5 Budget Reflection
If your cost is too high, what can be simplified, removed, substituted, or shared?

**Response:**  
`[Write here]`

---

# 13. Planning the Work

## 13.1 Team Working Agreement
Write how your team will work together.

Include:
- how tasks are divided,
- how decisions are made,
- how progress will be checked,
- what happens if a task is delayed,
- how documentation will be maintained.

**Response:**  
`[Write here]`

## 13.2 Task Breakdown

| Task ID | Task | Owner | Estimated Hours | Deadline | Dependency | Status |
|---|---|---|---:|---|---|---|
| T1 | `[Finalize concept]` | `[Name]` | `2` | `[Date]` | `None` | `To Do` |
| T2 | `[Complete BOM]` | `[Name]` | `1` | `[Date]` | `T1` | `To Do` |
| T3 | `[Test electronics]` | `[Name]` | `2` | `[Date]` | `T1` | `To Do` |
| T4 | `[Build structure]` | `[Name]` | `4` | `[Date]` | `T1` | `To Do` |
| T5 | `[Write control code]` | `[Name]` | `4` | `[Date]` | `T3` | `To Do` |
| T6 | `[Integrate system]` | `[Name]` | `4` | `[Date]` | `T4, T5` | `To Do` |
| T7 | `[Playtest]` | `[Name]` | `2` | `[Date]` | `T6` | `To Do` |
| T8 | `[Refine and document]` | `[Name]` | `3` | `[Date]` | `T7` | `To Do` |

## 13.3 Responsibility Split

| Area | Main Owner | Support Owner |
|---|---|---|
| Concept and gameplay | `[Name]` | `[Name]` |
| Electronics | `[Name]` | `[Name]` |
| Coding | `[Name]` | `[Name]` |
| App | `[Name]` | `[Name]` |
| Mechanical build | `[Name]` | `[Name]` |
| Testing | `[Name]` | `[Name]` |
| Documentation | `[Name]` | `[Name]` |

---

# 14. Weekly Milestones

## 14.1 Four-Week Plan

### Week 1 — Plan and De-risk
Expected outcomes:
- [ ] Idea finalized
- [ ] Core interaction decided
- [ ] Sketches made
- [ ] BOM completed
- [ ] Purchase needs identified
- [ ] Key uncertainty identified
- [ ] Basic feasibility tested

### Week 2 — Build Subsystems
Expected outcomes:
- [ ] Electronics tests completed
- [ ] CAD / structure planning completed
- [ ] App UI started if needed
- [ ] Mechanical concept tested
- [ ] Main subsystems partially working

### Week 3 — Integrate
Expected outcomes:
- [ ] Physical body built
- [ ] Electronics integrated
- [ ] Code connected to hardware
- [ ] App connected if required
- [ ] First playable version exists

### Week 4 — Refine and Finish
Expected outcomes:
- [ ] Technical bugs reduced
- [ ] Playtesting completed
- [ ] Improvements made
- [ ] Documentation completed
- [ ] Final build ready

## 14.2 Weekly Update Log

| Week | Planned Goal | What Actually Happened | What Changed | Next Steps |
|---|---|---|---|---|
| Week 1 | `[Write here]` | `[Write here]` | `[Write here]` | `[Write here]` |
| Week 2 | `[Write here]` | `[Write here]` | `[Write here]` | `[Write here]` |
| Week 3 | `[Write here]` | `[Write here]` | `[Write here]` | `[Write here]` |
| Week 4 | `[Write here]` | `[Write here]` | `[Write here]` | `[Write here]` |

---

# 15. Risks and Unknowns

## 15.1 Risk Register

| Risk | Type | Likelihood | Impact | Mitigation Plan | Owner |
|---|---|---|---|---|---|
| `[Example: Bluetooth disconnects]` | `Technical` | `Medium` | `High` | `[Fallback interaction / simplify connection flow]` | `[Name]` |
| `[Example: Structure breaks during play]` | `Mechanical` | `Medium` | `High` | `[Reinforce joints / change material]` | `[Name]` |
| `[Risk]` | `[Technical / Material / Time / Gameplay]` | `[Low/Medium/High]` | `[Low/Medium/High]` | `[Plan]` | `[Name]` |
| `[Risk]` | `[Type]` | `[Low/Medium/High]` | `[Low/Medium/High]` | `[Plan]` | `[Name]` |

## 15.2 Biggest Unknown Right Now
What is the single biggest uncertainty in your project at this stage?

**Response:**  
`[Write here]`

---

# 16. Testing and Playtesting

## 16.1 Technical Testing Plan

| What Needs Testing | How You Will Test It | Success Condition |
|---|---|---|
| `[Bluetooth connection]` | `[Method]` | `[What counts as success?]` |
| `[Mechanism movement]` | `[Method]` | `[What counts as success?]` |
| `[Sensor behavior]` | `[Method]` | `[What counts as success?]` |
| `[App communication]` | `[Method]` | `[What counts as success?]` |

## 16.2 Playtesting Plan

| Question | How You Will Check |
|---|---|
| Do players understand what to do? | `[Method]` |
| Is the interaction satisfying? | `[Method]` |
| Do players want another turn? | `[Method]` |
| Is the challenge balanced? | `[Method]` |
| Is the response clear and immediate? | `[Method]` |

## 16.3 Testing and Debugging Log

| Date | Problem Found | Type | What You Tried | Result | Next Action |
|---|---|---|---|---|---|
| `[Week 3]` | `[Servos twitching but not moving]` | `[Technical]` | `[Added shared Ground wire.]` | `[Servos snap perfectly.]` | `[Move to code logic]` |
| `[Week 4]` | `[ESP32 freezing/disconnecting when claws snap]` | `[Technical]` | `[Moved servos from ESP32 5V pin to an external 5V power supply.]` | `[Works better]` | `[Final assembly]` |

## 16.4 Playtesting Notes

| Tester | What They Did | What Confused Them | What They Enjoyed | What You Will Change |
|---|---|---|---|---|
| `[Peer / friend / classmate]` | `[Observation]` | `[Observation]` | `[Observation]` | `[Action]` |
| `[Peer / friend / classmate]` | `[Observation]` | `[Observation]` | `[Observation]` | `[Action]` |

---

# 17. Build Documentation

## 17.1 Fabrication Process
Describe how the project was physically made.

Include:
- cutting,
- 3D printing,
- assembly,
- fastening,
- wiring,
- finishing,
- revisions.

**Response:**  
`[Write here]`

## 17.2 Build Photos
Add photos throughout the project.

Suggested images:
- early sketch,
- prototype,
- electronics testing,
- mechanism test,
- app screenshot,
- final build.

Example:
```md



```

## 17.3 Version History

| Version | Date | What Changed | Why |
|---|---|---|---|
| `v1` | `[Date]` | `[Describe]` | `[Reason]` |
| `v2` | `[Date]` | `[Describe]` | `[Reason]` |
| `v3` | `[Date]` | `[Describe]` | `[Reason]` |

---

# 18. Final Outcome

## 18.1 Final Description
Describe the final version of your project.

**Response:**  
`[We successfully built "Hands Off". The final physical model uses a laser-cut hexagonal base with two large, hinged MDF claws. The artifact sits centrally over the HC-SR04. The dual-servo pushrod mechanism is incredibly snappy and violent (in a fun way), making the failure condition very satisfying. The Game Master app connects flawlessly via BLE.]`

## 18.2 What Works Well
- `[Point 1 The acceleration logic. It feels perfectly tuned to catch shaky hands.]`
- `[Point 2 The dual-servo pushrod mechanism. It handles the heavy MDF with ease.]`
- `[Point 3]`

## 18.3 What Still Needs Improvement
- `[Point 1 The HC-SR04 sensor sometimes catches the side of the claw if it isn't aligned perfectly.]`
- `[Point 2]`
- `[Point 3]`

## 18.4 What Changed From the Original Plan
How did the project change from the initial idea?

**Response:**  
`[We originally planned to use an artist's wooden mannequin hand and use fishing line tendons. We realized the wood was too heavy and the internal elastics were too stiff for our SG90 servos. We pivoted to designing our own geometric MDF claws and using a rigid pushrod linkage instead, which ultimately looked better and functioned 100x more reliably.]`

---

# 19. Reflection

## 19.1 Team Reflection
What did your team do well?  
What slowed you down?  
How well did you manage time, tasks, and responsibilities?

**Response:**  
`[Write here]`

## 19.2 Technical Reflection
What did you learn about:
- electronics,
- coding,
- mechanisms,
- fabrication,
- integration?

**Response:**  
`[The biggest lesson was understanding Power and Ground. Learning that microcontrollers can "brown out" when motors pull too much current, and discovering that an external power supply won't work unless it shares a Ground line with the data source, was a massive "aha" moment that saved our project. Also, writing code that measures delta (change over time) rather than just absolute values made the sensor feel much "smarter."]`

## 19.3 Design Reflection
What did you learn about:
- designing for play,
- delight,
- clarity,
- physical interaction,
- player understanding,
- iteration?

**Response:**  
`[Write here]`

## 19.4 If You Had One More Week
What would you improve next?

**Response:**  
`[We would add a Capacitive Touch sensor (using copper tape) to the MDF claws, so that if the player's string accidentally brushes against the sides of the claw while lifting, it triggers the trap, adding a second layer of difficulty to the extraction!]`

---

# 20. Final Submission Checklist

Before submission, confirm that:
- [ ] Team details are complete
- [ ] Project description is complete
- [ ] Inspiration sources are included
- [ ] Player journey is written
- [ ] Sketches are added
- [ ] BOM is complete
- [ ] Purchase list is complete
- [ ] Budget summary is complete
- [ ] Mechanical planning is documented if applicable
- [ ] App planning is documented if applicable
- [ ] Code flowchart is added
- [ ] Task breakdown is complete
- [ ] Weekly logs are updated
- [ ] Risk register is complete
- [ ] Testing log is updated
- [ ] Playtesting notes are included
- [ ] Build photos are included
- [ ] Final reflection is written

---

# 21. Suggested Repository Structure

```text
project-repo/
├── README.md
├── images/
│   ├── concept-sketch.jpg
│   ├── labeled-sketch.jpg
│   ├── circuit-diagram.jpg
│   ├── ui-mockup.jpg
│   ├── prototype-1.jpg
│   └── final-build.jpg
├── code/
│   ├── main.py
│   ├── test_code.py
│   └── notes.md
├── cad/
│   ├── models/
│   └── screenshots/
└── docs/
    ├── references.md
    └── extra-notes.md
```

---

# 22. Instructor Review

## 22.1 Proposal Approval
- [ ] Approved to proceed
- [ ] Approved with changes
- [ ] Rework required before proceeding

**Instructor comments:**  
`[Instructor fills this section]`

## 22.2 Midpoint Review
`[Instructor fills this section]`

## 22.3 Final Review Notes
`[Instructor fills this section]`
