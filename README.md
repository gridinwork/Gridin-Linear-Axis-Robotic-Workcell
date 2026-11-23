![Gridin Linear-Axis Robotic Workcell](media/images/main-render.jpg)

<p align="center">
  <img src="media/animation/linear-rail-demo.gif" alt="Gridin Linear-Axis Robotic Workcell motion demo" width="900">
</p>

# Gridin Linear-Axis Robotic Workcell

**Advanced robotic workcell developed and modified by Oleg Gridin.**  
The project evolves the PAROL6 desktop manipulator concept into a larger robotic workcell with an additional linear travel axis, an expanded operating area, multi-position pick-and-place capability, an auxiliary rotary/tilting worktable concept, and a prototype automatic tool-changing station for CNC-style operations.

> The animation above is a CAD motion demonstration of the linear-axis workcell. The original MP4 is included in [`media/video/linear-rail-demo.mp4`](media/video/linear-rail-demo.mp4).

## Project goal

The main objective of this modernization is to move beyond the working envelope of a fixed desktop robot. The manipulator is mounted on a dedicated linear slide so the complete arm can travel between different work zones instead of remaining at one fixed base position.

This architecture allows the robot to:

- move along an additional linear axis;
- stop at different positions across an extended work area;
- approach objects that are outside the reach of the original fixed-base configuration;
- perform pick-and-place operations between separated stations;
- combine arm motion with auxiliary workpiece positioning;
- support future machining and automated tool-changing workflows.

## Core modifications

### 1. Modified multi-axis manipulator

The base arm originates from the open-source PAROL6 platform, but the system shown here represents a custom engineering adaptation by **Oleg Gridin**. The mechanical layout, drive choices, base integration and workcell architecture were reworked for the extended system.

![Axis layout](media/images/02-axis-layout.webp)

![Transparent drive layout](media/images/03-transparent-drive-layout.webp)

### 2. Additional linear travel axis

The most important extension is the rail-mounted base. The complete manipulator can translate along the workcell, substantially increasing the usable working envelope compared with a fixed desktop installation.

![Linear-axis workspace](media/images/09-linear-axis-workspace.webp)

The following frames show the same robot at different positions along the rail:

![Linear-axis position 1](media/images/10-linear-axis-position-1.webp)

![Linear-axis position 2](media/images/11-linear-axis-position-2.webp)

![Linear-axis position 3](media/images/12-linear-axis-position-3.webp)

### 3. Pick-and-place across multiple stations

The extended rail allows the manipulator to reach separated object positions and transfer parts between them. The CAD sequence demonstrates approach, gripping, transport and placement within the enlarged work area.

![Pick-and-place sequence 1](media/images/13-pick-and-place-1.webp)

![Pick-and-place sequence 2](media/images/14-pick-and-place-2.webp)

![Workspace top view](media/images/15-workspace-top-view.webp)

### 4. Auxiliary rotary / tilting worktable

A separate workpiece-positioning assembly was designed as part of the workcell concept. It adds controlled reorientation of the working surface so the manipulator can access different faces or positions of a part without relying only on arm motion.

![Rotary worktable](media/images/07-rotary-worktable.webp)

![Rotary worktable with manipulator](media/images/08-rotary-worktable-pose.webp)

### 5. Manipulator motion and drive layout

Additional CAD views illustrate the modified arm in several joint configurations and the relationship between the arm, drive components and extended base system.

![Manipulator home configuration](media/images/04-manipulator-home.webp)

![Manipulator pose](media/images/05-manipulator-pose.webp)

![Manipulator alternate pose](media/images/06-manipulator-pose-alt.webp)

## Automatic tool changer prototype

The workcell also includes a designed tool-changing station intended for interchangeable machining tools / cutters. The dock uses spring-loaded tool positions and is arranged so a spindle or end-effector can approach a selected station for tool exchange.

The images below show both the CAD implementation and a physical prototype of the docking concept.

![Automatic tool changer CAD](media/images/16-tool-changer-cad-closeup.webp)

![Automatic tool changer physical prototype](media/images/17-tool-changer-real-prototype.webp)

![Automatic tool changer overview](media/images/18-tool-changer-cad-overview.webp)

## System architecture

At the portfolio level, the complete platform is divided into several engineering subsystems:

| Subsystem | Purpose |
|---|---|
| Multi-axis robotic arm | Main manipulation and end-effector positioning |
| Linear travel axis | Moves the entire manipulator between work zones |
| Auxiliary rotary/tilting table | Reorients the workpiece for multi-side access |
| Gripper / end effector | Pick-and-place and manipulation tasks |
| Tool-change station | Stores and exchanges interchangeable machining tools |
| Main motion controller | Coordinates robot joints and auxiliary axes |
| PC software | Planned higher-level control, sequencing and visualization |

## Portfolio scope

This repository is intended to document the **mechanical and system-level modernization** of the robotic workcell. It focuses on the engineering concept, CAD development, motion demonstrations and prototype hardware shown in the media.

Controller firmware, detailed electrical schematics and future PC control software are separate workstreams and are not represented here as completed deliverables unless explicitly added in later revisions.

## Development direction

The extended architecture is intended as a foundation for:

- larger-area robotic handling;
- multi-station pick-and-place automation;
- automated part repositioning;
- interchangeable end effectors;
- automatic cutter/tool exchange;
- compact CNC-style robotic operations;
- coordinated motion between the arm, rail and auxiliary positioning mechanisms.

## Author

**Oleg Gridin**  
Mechanical integration, system modernization, extended-axis workcell concept, CAD adaptation and auxiliary mechanisms.

## Upstream attribution

This work builds on the **PAROL6 Desktop Robot Arm** open-source project by **Source Robotics / Petar Crnjak**. The original project and its software ecosystem remain subject to their upstream licenses and attribution requirements.

Official upstream repository:  
https://github.com/Source-Robotics/PAROL6-Desktop-robot-arm

See [`THIRD_PARTY_NOTICES.md`](THIRD_PARTY_NOTICES.md) for additional attribution information.

## Repository contents

```text
media/
  images/       CAD renders and prototype photos
  animation/    auto-playing GIF demonstrations for GitHub
  video/        original MP4 demonstration

docs/           portfolio-oriented engineering notes
README.md        project overview
```

## Status

This repository documents an engineering development project and includes CAD visualizations, motion simulations and prototype hardware imagery. It should not be interpreted as a certified industrial robot or production CNC machine.