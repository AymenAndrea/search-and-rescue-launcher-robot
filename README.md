# Autonomous Search-and-Rescue Launcher

First-year Engineering Design Project ("Team Megabits") — University of Windsor, Team of 5

## My Role: System Design & Integration Lead
I designed the catapult system — its mechanisms, how it would function, and how 
the reload system, barrel, and launch sequence fit together — along with the 
overall layout that let the mechanical, electrical, and software components 
work as a single system. I was also responsible for documenting the project 
throughout.

Whenever something didn't work as expected or the team needed a new approach, I 
took the lead on solving it — working out what was going wrong and proposing 
the ideas that moved the design forward. The trailer-alignment issue below is 
one example: I identified the cause and worked out the fix.

## Problem
Design a fully autonomous robot that navigates an obstacle course and
accurately delivers emergency supplies to a search-and-rescue drop zone,
simulating relief delivery to a remote/inaccessible location.

## Requirements
- Autonomously navigate an obstacle course using onboard sensors/line-tracking
- Launch three payloads consecutively into a target zone 3m away
- Catapult mechanism could not exceed the width of the robotic vehicle
- No permanent modification to the base robotic vehicle
- Fully autonomous operation, no human intervention during the run

## System Architecture
A trailer-mounted catapult, towed behind an autonomously line-following robot.
The car signals the trailer's onboard control system via a wired connection
once it detects the end of the course, triggering the reload/launch sequence
(piston-driven hopper → flywheel launch → repeat x3).

## Design Decisions
- Chose a tow-behind trailer design over an onboard-mounted catapult to allow
  a larger, stronger launcher without needing to balance it on the car itself
- Fixed-incline barrel for a consistent arcing payload trajectory
- Budget-conscious component selection — reused owned materials to bring the
  actual build cost to ~$100 against a $319 full-retail estimate

## Results
Successfully completed the course and launched all three payloads in under
5 seconds of active launch time. Final full-run time: ~28–33 seconds.

## Challenges & Problem-Solving
The trailer had no independent stabilization and drifted out of alignment
with the car during sharp turns, since it simply followed the car's movement
rather than self-correcting. This required manual realignment during testing
and directly hurt payload accuracy — the team diagnosed this as a geometry
issue (tandem axle position relative to the trailer's center of mass) rather
than a control/code problem.

## Proposed Improvements
- Reposition the tandem axle closer to the center of the trailer's base to
  reduce drift during turns
- Raise the barrel's angle further off the ground for a better arcing shot

## Team
5-person team, Cornerstone Design course, University of Windsor.
