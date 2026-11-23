# Workcell Architecture

## Overview

The Gridin Linear-Axis Robotic Workcell expands a desktop multi-axis manipulator into a distributed working cell by adding external motion systems and dedicated stations.

## Motion groups

### Robotic manipulator
The arm provides the primary articulated motion for positioning the end effector.

### Linear axis
The complete robot base is carried on a linear slide. This external axis relocates the arm between separated work zones and increases the effective workspace.

### Auxiliary worktable
A separate rotary/tilting fixture is used to reorient a workpiece relative to the manipulator. This reduces the need for the arm to reach every face of a component from one fixed table orientation.

### Tool-change station
The spring-supported docking array is intended to store interchangeable machining tools or cutters in repeatable positions. CAD views and a physical prototype are included in the repository.

## Control separation

The complete project is intentionally separated into engineering layers:

1. mechanical system and CAD;
2. electronics and wiring;
3. main-controller firmware;
4. PC-level sequencing/control software.

This repository presents the first layer and the overall workcell concept. Firmware, electrical documentation and PC software may be published separately as they reach a suitable state.
