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
| `[Aarav Srivastava]` | `[Coding / App ]` | `[Mechanics/ Testing]` | `[MicroPython scripting, debugging hardware-software bridges]` |
| `[Teerthi Laddad]` | `[Electronics / Fabrication / Mechanics]` | `[Testing]` | `[Hands-on fabrication, mechanical assembly, system integration, electronics implementation, motion optimization, surface finishing, iterative prototyping, testing & debugging, problem-solving, precision alignment, reliability improvement]` |

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
`[the original plan for the claw system did not work so we had to create a pulley system with weights]`

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
<img width="400" height="339" alt="image" src="https://github.com/user-attachments/assets/786c31d4-368f-4c3d-a445-6c0966b6ff2b" /  

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
`[(https://drive.google.com/file/d/1pOvpKg4OYv1rVn18H-KYfztH-Smswymy/view?usp=sharing)]`

## 10.4 Pseudocode

```text
[IMPORT required hardware libraries (Pins, PWM, Time, NeoPixel, Servo, HCSR04)

SETUP hardware connections:
  - Attach Servos to Pins 32 and 33
  - Attach Ultrasonic Sensor to Pins 5 (Trig) and 18 (Echo)
  - Attach NeoPixel Strip to Pin 4
  - Attach Buzzer to Pin 14 using PWM

DEFINE game rules (Constants):
  - Time Limit = 10 Seconds
  - Win Height = 12 cm
  - Lift Threshold = 0.25 cm
  - Max Safe Movement (Variation) = 2.0 cm

DEFINE Audio-Visual Effects (Helper Functions):
  - function play_sound(pitch, duration)
  - function fx_game_start() -> Sweeping yellow lights and rising tones
  - function fx_update_progress(height) -> Lights up LEDs based on % to Win Height
  - function fx_game_over() -> Turns strip red and plays sad tones
  - function fx_victory() -> Flashes green and plays arcade win sound

START MAIN PROGRAM:
  Turn off all LEDs
  Open Claws (Set Servos to 0 degrees)

  CALIBRATION SEQUENCE:
    Read ultrasonic sensor until a stable distance under 10cm is found
    Save this stable reading as 'baseline_distance'
    Trigger fx_game_start()

  PHASE 1: WAIT FOR LIFT-OFF
    Loop continuously:
      Read current_distance
      IF current_distance > (baseline_distance + Lift Threshold):
        Print "Lift-Off Detected!"
        Break loop and start the game

  PHASE 2: THE COUNTDOWN & STEADY HAND TRAP
    Start background millisecond timer
    Set previous_distance = baseline_distance

    Loop continuously:
      Calculate time_left = 10 seconds - elapsed_time

      TRAP 1: CHECK TIME LIMIT
        IF time_left <= 0:
          Snap claws closed (90 degrees)
          Trigger fx_game_over()
          Break loop (Player Loses)

      Read current_distance
      IF reading is physically possible (ignore ultrasonic glitches):
        Calculate variation = Absolute Value of (current_distance - previous_distance)

        TRAP 2: CHECK FOR SHAKY HANDS
          IF variation > Max Safe Movement:
            Snap claws closed (90 degrees)
            Trigger fx_game_over()
            Break loop (Player Loses)
            
          ELSE (Safe lift):
            Trigger fx_update_progress(current_distance)
            
            CHECK WIN CONDITION:
              IF current_distance >= Win Height:
                Trigger fx_victory()
                Break loop (Player Wins)

            Update previous_distance = current_distance

      Wait 0.1 seconds before checking again

  POST-GAME RESET SEQUENCE:
    Wait 3 seconds to let players process the win/loss
    Open claws (0 degrees)
    Turn off all LEDs
    End program (Ready for restart)]
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
| `[Ultrasonic sensor]` | `1` | `Yes` | `No` |
| `[power supply module]` | `1` | `Yes` | `No` |
| `[servo motor]` | `2` | `Yes` | `No` |
| `[MDF Board]` | `[1]` | `[Yes]` | `[No]` |
| `[pvc pipe]` | `[1]` | `[Yes]` | `[No]` |
| `[nylon cord]` | `[2 mtr]` | `[No]` | `[Yes]` | `[10 rupees]` | `[Nylon]` | `[stronger, able to support the weights ]` |
| `[spray paint]` | `[1]` | `[No]` | `[Yes]` | `[250 rupees]` | `[acrylic]` | `[cover up the whole model and hide uneveness]` |
| `[gold acrylic]` | `[1]` | `[No]` | `[Yes]` | `[250 rupees]` | `[acrylic]` | `[add a little defining detail to the model]` |

## 12.2 Material Justification
Explain why you selected your main materials and components.

Examples:
- Why acrylic instead of cardboard?
- Why MDF instead of 3D print?
- Why servo instead of DC motor?
- Why bearing instead of a plain shaft hole?

**Response:**  
`[MDF over cardboard: MDF is rigid, laser-cuttable to precision, and holds fasteners. Cardboard would deform under repeated claw-closing forces.
PVC pipe over wooden dowel: PVC can be sanded to a very smooth finish, which is critical for the sleeve to slide freely. A wooden dowel would have grain and splinter risk.
Servo over dc motor: A servo is controllable (angle-based) and runs on lesser power compared to the dc motor.]`

## 12.3 Items to Purchase Separately

| Item | Why Needed | Purchase Link | Latest Safe Date to Procure | Status |
|---|---|---|---|---|
| `[spray paint]` | `[cover up the whole model and hide uneveness]` | `[Link]` | `[19-04-2026]` | `[Received]` |
| `[gold acrylic paint]` | `[add a little defining detail to the model]` | `[Link]` | `[19-04-2026]` | `[Received]` |
| `[nylon cord]` | `[hold the counterweights]` | `[bought in person (stationary)]` | `[17-04-2026]` | `[Received]` |

## 12.4 Budget Summary

| Budget Item | Estimated Cost |
|---|---:|
| Electronics | `[0]` |
| Mechanical parts | `[0]` |
| Fabrication materials | `[510]` |
| Purchased extras | `[10]` |
| Contingency | `[0]` |
| **Total** | `[520]` |

## 12.5 Budget Reflection
If your cost is too high, what can be simplified, removed, substituted, or shared?

**Response:**  
`[The spray paint can be replaced by a simple bolltle of acrylic paint and painted manually.]`

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
`[Tasks are divided by skill: Aarav leads code; Teerthi leads mechanical build and fabrication. Design decisions are made together. Progress is checked at the start of each class session. If a task is delayed, the other team member supports to unblock. Documentation is updated by whoever completes each task, reviewed together at end of each week.]`

## 13.2 Task Breakdown

| Task ID | Task | Owner | Estimated Hours | Deadline | Dependency | Status |
|---|---|---|---:|---|---|---|
| T1 | `[Finalize concept]` | `[Teerthi]` | `2` | `[end of week 1]` | `None` | `done` |
| T2 | `[Complete BOM]` | `[Teerthi]` | `1` | `[end of week 2]` | `T1` | `done` |
| T3 | `[Test electronics]` | `[Both]` | `2` | `[end of week 3]` | `T1` | `done` |
| T4 | `[Build structure]` | `[Teerthi]` | `6` | `[end of week 3]` | `T1` | `done` |
| T5 | `[Write control code]` | `[Aarav]` | `3` | `[mid week 4]` | `T3` | `done` |
| T6 | `[Integrate system]` | `[both]` | `4` | `[mid week 4]` | `T4, T5` | `done` |
| T7 | `[Playtest]` | `[both]` | `2` | `[Date]` | `[end of week 4]` | `To Do` |
| T8 | `[Refine and document]` | `[Teerthi]` | `3` | `[end of week 4]` | `T7` | `To Do` |

## 13.3 Responsibility Split

| Area | Main Owner | Support Owner |
|---|---|---|
| Concept and gameplay | `[Teerthi]` | `[Aarav]` |
| Electronics | `[Teerthi]` | `[Aarav]` |
| Coding | `[Aarav]` | `[Name]` |
| App | `[na]` | `[na]` |
| Mechanical build | `[Teerthi]` | `[Aarav]` |
| Testing | `[both]` | `[Name]` |
| Documentation | `[both]` | `[Name]` |

---

# 14. Weekly Milestones

## 14.1 Four-Week Plan

### Week 1 — Plan and De-risk
Expected outcomes:
- [x] Idea finalized
- [x] Core interaction decided
- [ ] Sketches made
- [x] BOM completed
- [x] Purchase needs identified
- [x] Key uncertainty identified
- [x] Basic feasibility tested

### Week 2 — Build Subsystems
Expected outcomes:
- [x] Electronics tests completed
- [x] CAD / structure planning completed
- [ ] App UI started if needed
- [x] Mechanical concept tested
- [x] Main subsystems partially working

### Week 3 — Integrate
Expected outcomes:
- [x] Physical body built
- [x] Electronics integrated
- [x] Code connected to hardware
- [ ] App connected if required
- [ ] First playable version exists

### Week 4 — Refine and Finish
Expected outcomes:
- [x] Technical bugs reduced
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
| `[HC-SR04 gives noisy readings causing false triggers]` | `Technical` | `Medium` | `High` | `[Average last 5 readings; tune threshold conservatively]` | `[Aarav]` |
| `[Counterweight force insufficient to close all arms fully]` | `Mechanical` | `Medium` | `High` | `[increase weight if needed]` | `[Teerthi]` |
| `[Sleeve doesn't slide freely enough to close claw]` | `[Mechanical]` | `[Medium]` | `[High]` | `[Plan]` | `[Teerthi]` |


## 15.2 Biggest Unknown Right Now
What is the single biggest uncertainty in your project at this stage?

**Response:**  
`[Whether the sleeve-on-PVC-pipe mechanism will slide reliably under gravity without the players needing to manually push it. The mechanism only works if friction is low enough that the counterweight alone can drive the sleeve upward.]`

---

# 16. Testing and Playtesting

## 16.1 Technical Testing Plan

| What Needs Testing | How You Will Test It | Success Condition |
|---|---|---|
| `[Sleeve slides freely on PVC]` | `[Push sleeve by hand with/without counterweight attached]` | `[Sleeve travels full range with minimal counterweight]` |
| `[Claw closes fully from sleeve travel]` | `[Attach claw arm wires; test full closure]` | `[All arms meet at centre; no arm jams]` |
| `[HC-SR04 distance reading]` | `[Serial monitor; measure known distances with ruler]` | `[Readings within ±1cm at 5–25cm range]` |
| `[Full system trigger chain]` | `[Simulate abrupt motion, confirm claw closes]` | `[Claw closes within 1 second of trigger]` |

## 16.2 Playtesting Plan

| Question | How You Will Check |
|---|---|
| Do players understand what to do? | `[Observe first 10 seconds without explanation; note if they pick up the strings spontaneously]` |
| Is the interaction satisfying? | `[Ask players immediately after: "Did the closing feel dramatic?"]` |
| Do players want another turn? | `[Note whether players ask to replay without prompting]` |
| Is the challenge balanced? | `[Track success/failure ratio over 10 rounds; target ~40–60% success rate]` |
| Is the response clear and immediate? | `[Players should be able to identify exactly what caused the claw to close]` |

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
`[Claw Arms (MDF, laser cut): Arms were designed in illustrator and laser cut from 3mm MDF. Arms were dry-fitted to the central column before wire attachment.
Sliding Ring Mechanism: A hollow PVC coupling was cut to length and test-fit on the PVC pipe. The pipe was sanded progressively until the sleeve moved freely with minimal force. Wire guides were drilled into the sleeve and each arm.
Wire Linkage: metal wires was threaded from all claw arm's base through a guide ring at the sleeve. Tension was adjusted so all arms close simultaneously.
Pulley and Counterweight: A fixed pulley was mounted at the top of the structure. Cord runs from the sleeve, over the pulley, down to the counterweight. The servo holds the counterweight via a hooked latch at its horn.
Electronics: HC-SR04 positioned above the bomb resting position, facing upwards. Servo mounted adjacent to pulley attachment point.
Finishing: Full structure spray-painted matte black. Gold acrylic applied with a fine brush to claw arm edges, bolt heads, and the bomb prop for visual contrast.]`

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
`[We successfully built "Hands Off". The final physical model uses a laser-cut hexagonal base with two large, hinged MDF claws. The artifact sits centrally over the HC-SR04. The dual-servo pushrod mechanism is incredibly snappy and violent (in a fun way), making the failure condition very satisfying.]`

## 18.2 What Works Well
- `[Point 1 The acceleration logic. It feels perfectly tuned to catch shaky hands.]`
- `[Point 2 The pushrod mechanism. It handles the heavy MDF with ease.]`
- `[Point 3 The counterweight pulley system which is sure to give a precise snap.]`

## 18.3 What Still Needs Improvement
- `[The HC-SR04 sensor sometimes catches the side of the claw if it isn't aligned perfectly.]`
- `[The mechanical build in terms of overall precision could be better if made using precise measurements and materials.]`
- `[The replicability of the project can be a little complex considering the mechanics and time constraints which could be improved upon.]`

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
`[write here]`

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
- [X] Team details are complete
- [X] Project description is complete
- [X] Inspiration sources are included
- [X] Player journey is written
- [ ] Sketches are added
- [X] BOM is complete
- [X] Purchase list is complete
- [X] Budget summary is complete
- [X] Mechanical planning is documented if applicable
- [X] App planning is documented if applicable
- [ ] Code flowchart is added
- [X] Task breakdown is complete
- [X] Weekly logs are updated
- [X] Risk register is complete
- [X] Testing log is updated
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
