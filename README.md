# LogicDesignLab_FinalProject

## Overview

This project, "Logic-Controlled Board," is a hands-on lab project designed to apply the core principles learned throughout the semester in logic design. It involves creating a dynamic switching system using combinational and sequential logic, finite state machines, and digital circuit design practices.

## Purpose

The primary purpose of this project is to reinforce theoretical concepts of Boolean algebra, FSMs, and circuit optimization through practical implementation. Students will gain experience in:
- Schematic design and simulation using Quartus.
- Hands-on breadboard and soldered circuit construction.
- Systematic debugging and design testing.

## Learning Outcomes

- **Learning and Application:** Learn new techniques and apply theoretical concepts practically.
- **Design Thinking:** Develop structured problem-solving skills.
- **Practical Skills:** Enhance proficiency in wiring, soldering, and debugging circuits.
- **Theory to Practice:** Bridge academic knowledge with real-world applications.
- **Effective Communication:** Improve documentation and presentation of circuit designs.

## Project Description

The Logic-Controlled Board includes four switches and four colored lamps (Red, Green, Blue, Yellow). Although each switch appears to control a lamp of the same color, the behavior changes dynamically based on the last switch turned off. Additional features include:
- Capless switch disabling.
- Reconfigurable lamp sequences.
- Practice/performance mode toggle via a detachable 7-segment display.
- Locking/unlocking system for performance mode.

### Lamp Sequences
- **Default:** 1 → 2 → 3 → 4
- **Sequence 1:** Last off = SW1 → 1 → 2 → 3 → 4
- **Sequence 2:** Last off = SW2 → 2 → 3 → 4 → 1
- **Sequence 3:** Last off = SW3 → 3 → 4 → 1 → 2 + Special Trick #3
- **Sequence 4:** Last off = SW4 → 4 → 3 → 2 → 1

### Special Trick #3 (Sequence 3)
- Involves cap removal, delayed reactivation, and toggling behavior.
- Requires a 4-second timer and tracking cap status.

### Lock/Unlock Mechanism
- Lock: Battery removal → SW2 ON → Battery reinserted.
- Unlock: Restart without SW2 ON.

## Solution Approach

### FSM Design
- States: Boot, Locked, Sequence Detector, Sequence 1-4, Switch NotWorking
- Inputs: SW1–SW4, Treset (4-second reset timer)
- Outputs: LEDs (L1–L4), 7-Segment Display

### Implementation Steps
1. Derive output functions using state tables.
2. Minimize logic using Karnaugh Maps.
3. Draw optimized circuit diagrams.
4. Simulate using Quartus.
5. Design and build a 555 Timer for clock generation.
6. Implement final design on a breadboard with clean soldering.
7. Package the design for final submission.

## This project has an online simulation that can be opened using a special program which is "Constructor Virtual de Circuitos".
   To download this program follow this link: https://www.mediafire.com/?p8ky34kw3r0n51u

## To run the Quartus simulations, follow these steps:
	1) Download Quartus ii version 9.1
	2) Open existing project which is the Project File in the ZIP folder
	3) Navigate to Schematic file
	4) Open Waveform File
	5) Simulate Vector Waveform File
