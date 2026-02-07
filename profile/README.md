## Overview

Mycopunk Aim Assist is a focused runtime control module designed for precision targeting adjustment inside **Mycopunk**. The system operates as an isolated aim correction layer, modifying targeting behavior without altering weapon data or persistent files. It exposes configurable parameters such as assist strength, smoothing curves, snap thresholds, and activation conditions. By operating entirely in memory, the module allows controlled testing of aim behavior, interaction ranges, and target acquisition logic under reproducible conditions.

---

## Target Acquisition Logic Controller

* Adjustable aim assist radius
* Dynamic target selection prioritization
* Distance-based activation scaling

**In-game behavior:**
Defines how and when nearby targets are detected and considered valid for aim correction.

---

## Aim Smoothing and Curve Adjustment

* Linear and non-linear smoothing curves
* Configurable interpolation speed
* Micro-correction dampening

**Feature intent:**
Controls how aggressively aim snaps toward targets, ensuring predictable and testable motion behavior.

---

## Snap Threshold and Lock Timing System

* Snap delay configuration
* Lock-on duration limits
* Break conditions on rapid movement

**In-game behavior:**
Regulates how quickly aim correction engages and disengages based on player input and target motion.

---

## Contextual Activation Filters

* Separate rules for hip-fire and ADS
* Optional movement-based restrictions
* Field-of-view dependent scaling

**Feature intent:**
Applies aim assistance only under defined gameplay contexts, avoiding universal or uncontrolled activation.

---

## Target Type and Priority Mapping

* Enemy-only targeting
* Exclusion of neutral or inactive entities
* Priority weighting by distance or visibility

**In-game behavior:**
Ensures aim correction interacts only with intended entity categories.

---

## Hotkey and Toggle Management

* Real-time enable/disable switching
* Custom key bindings
* Independent module state tracking

**Feature intent:**
Allows immediate control over the aim assist system without pausing gameplay.

---

## Configuration Profile Handling

* Multiple named presets
* Import and export support
* Version-stable parameter storage

**In-game behavior:**
Facilitates rapid switching between different aim configurations for testing or comparison.

---

```mermaid
flowchart LR
A[Player Input] --> B[Activation Filters]
B --> C[Target Detection]
C --> D[Priority Mapping]
D --> E[Smoothing Engine]
E --> F[Snap & Lock Logic]
F --> G[Aim Output]
```

---

## FAQ

**Does aim assist alter weapon statistics?**
No, the module only adjusts targeting behavior, not weapon data.

**Can aim assist be limited to specific situations?**
Yes, activation filters control when assistance is applied.

**Is smoothing mandatory?**
Smoothing can be reduced or disabled entirely through configuration.

**Does the system support different profiles?**
Multiple configurations can be saved and loaded as needed.

**Are changes permanent?**
All modifications are runtime-only and reset when the session ends.

**Can aim assist be toggled instantly?**
Yes, hotkeys allow immediate activation or deactivation.

---

## Feature Summary

* Target acquisition control
* Aim smoothing and curve management
* Snap and lock timing regulation
* Context-aware activation filters
* Target prioritization logic
* Hotkey-based control
* Configuration profile support

---

---
