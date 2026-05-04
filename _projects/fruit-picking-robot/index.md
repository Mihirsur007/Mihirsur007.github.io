---
layout: post
title: Autonomous Fruit Picking Robot
description: As part of a 4-person team, I designed and built an autonomous fruit harvesting robot capable of navigating an 8' x 12' orchard, identifying target fruit by color, and harvesting them without damage. The robot features an X-drive chassis for omnidirectional movement, a single-stage belt-driven elevator, a 3D-printed claw, and a dual-camera vision system using AprilTags and color detection to achieve full end-to-end autonomy.
skills:
  - Robotics
  - Autonomous Systems
  - Computer Vision
  - VEX V5
  - 3D Printing
  - Control Systems
  - Mechanical Design
  - Python

main-image: /robot.jpg
---

## Overview

Our team designed and built a fruit picking robot capable of navigating an 8' × 12' orchard, identifying target fruit (limes, plums, or oranges), and harvesting them without damage. The robot combines a mobile drivetrain, a vertically adjustable picking mechanism, and a control system supporting both tele-op and autonomous modes.

**Team:** Mihir Surlaker, Benaiah Hills, Emerson Palaganas, Parin Dhayanidhi

---

## System Overview

The robot consists of three main subsystems:

- **X-Drive Chassis** — Four omni wheels in an X configuration enable full omnidirectional movement, making orchard navigation smooth and responsive regardless of robot orientation.
- **Single-Stage Elevator** — A belt-driven elevator powered by two VEX V5 motors allows the claw to reach fruit at multiple heights (12.5 in. to 22 in.).
- **3D-Printed Claw** — A four-bar linkage claw with a VEX AI camera mounted on top detects and grasps fruit while applying well under 1 N of force.

{% include image-gallery.html images="robot-full.jpg" height="450" %}

---

## Mechanical Design

### Drivetrain
| Parameter | Value |
|-----------|-------|
| Configuration | X-Drive (omnidirectional) |
| Motors | VEX V5 Smart Motors, 18:1 reduction |
| Wheels | VEX Omni Wheels |
| Footprint | 11.75 in × 11.75 in |

### Elevator
| Parameter | Value |
|-----------|-------|
| Type | Single-stage, belt-driven |
| Height range | 12.5 in – 22 in |
| Actuation | 2× VEX V5 Smart Motors, 18:1 reduction |
| Position sensing | Limit switch + motor odometry |

### End Effector
| Parameter | Value |
|-----------|-------|
| Design | 4-bar linkage, fully 3D-printed |
| Actuation | 1× VEX V5 Smart Motor, 18:1 reduction |
| Grip force | ~0.5 N (limit: 1 N) |

{% include image-gallery.html images="claw.jpg" height="450" %}

---

## Drivetrain

{% include image-gallery.html images="drivebase.jpg" height="450" %}

The X-drive chassis provides fast, responsive omnidirectional movement across the field. Aluminum VEX structure with custom 3D-printed gussets keeps the frame rigid while staying within weight constraints.

---

## Sensing & Control

Two VEX AI cameras handle all perception:

- **Lower camera** — mounted on the chassis, used for AprilTag detection and field-relative positioning.
- **Upper camera** — mounted on the claw, used for fruit color detection and alignment.

A VEX inertial sensor tracks tilt angle to detect ramp traversal and trigger state transitions autonomously.

### Autonomous Behaviors
1. Climb the 20° ramp using tilt feedback
2. Navigate the orchard using AprilTag localization
3. Detect and align to fruit by color
4. Grasp fruit and navigate to the correct color-coded bin
5. Release fruit and repeat

---

## Software Architecture

Field-oriented X-drive math translates joystick or autonomous commands into wheel velocities, independent of robot heading.

---

## Robot in Action

{% include image-gallery.html images="picking.jpg" height="450" %}

---

## What Worked Well

- X-drive chassis was fast, compact, and highly maneuverable
- Elevator and claw operated reliably throughout all demos
- Autonomous pickup and drop-off were consistent end-to-end
- Robot correctly identified fruit color and selected the matching bin

