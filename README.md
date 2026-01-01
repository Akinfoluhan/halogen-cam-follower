# Halogen cam-follower mechanism

Cam–follower mechanism designed for automated halogen headlight bulb assembly, guiding a gripper through pickup, insertion, soldering dwell, and return with smooth motion and controlled dynamics.

## Overview

This project designed a cam–follower mechanism to automate the insertion of halogen filament components during headlight bulb assembly. The mechanism drives a gripper through a defined sequence: pick up the component, insert it into the bulb, dwell during soldering, and return to the start position.

## Design requirements

- Achieve a target follower displacement (lift) while maintaining smooth motion profiles.
- Control velocity, acceleration, and jerk to reduce shock and improve repeatability.
- Limit pressure angle to reduce side loading and ensure reliable follower contact.
- Select a feasible base circle radius that avoids undercutting and supports manufacturability.
- Validate structural integrity using stress analysis of key components.

## Project visuals

![SVAJ diagram]()

![Exploded assembly view]()

![Simple assembly view]()

![3D render]()

## Mechanism design

The system uses a cam driving a translating follower to generate the required gripper motion during halogen bulb assembly. Cam geometry and follower motion laws were chosen to satisfy displacement requirements while keeping the pressure angle within an acceptable range and maintaining a manufacturable base circle radius.

## Motion program

The follower motion was defined over a full cam rotation using segmented phases that correspond to the assembly sequence:

- rise: move the gripper from the start position toward the insertion position
- dwell: hold position during soldering/assembly operations
- return: bring the gripper back to the start position
- dwell: hold at the start position before repeating

A smooth motion law was applied to reduce shock by limiting peak acceleration and jerk. SVAJ (displacement, velocity, acceleration, jerk) curves were used to verify the motion profile and compare iterations.

## Results and validation

The final cam design achieved the required lift while meeting key kinematic and structural constraints.

Kinematic validation included:

- SVAJ verification to confirm smooth rise/dwell/return behavior and controlled dynamics
- pressure angle evaluation to reduce follower side loading and improve reliability
- base circle selection to maintain manufacturability and avoid undercutting risk

Structural validation included:

- stress analysis of critical parts (including the cam) using von Mises stress criteria
- safety factor evaluation based on the selected material properties and expected loading

## Repository contents

- docs/
  - final-poster.pdf
- cad/
  - final-project.zip
- drawings/
  - Exploded View.SLDDRW
  - Simple Assembly View.SLDDRW
- media/
  - figures/
    - svaj-diagram.png
    - exploded-assembly.png
    - simple-assembly.png
    - render.png

## Tools used

- SolidWorks (CAD modeling, drawings, and assembly)
- DynaCam (cam profile design and motion tuning)
- SVAJ analysis (kinematic verification)
- FEA / von Mises stress analysis (structural validation)

## Collaborators

- [Matthew Lardieri](https://www.linkedin.com/in/matthew-lardieri-5b3334316/)
- [Mehdi Mrini](https://www.linkedin.com/in/mehdi-mrini-28779627a/)
- [Winston Nfor Kanjo Ndi](https://www.linkedin.com/in/winston-nfor-kanjo-ndi-825270225/)
