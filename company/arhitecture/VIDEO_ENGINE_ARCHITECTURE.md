# Video Engine Architecture

## Overview

The CopyStack Video Engine is built around a strict separation between **AI decision making** and **video rendering**.

The AI Engine is responsible for understanding the content and deciding **what should happen**.

The Renderer is responsible only for **executing those decisions**.

This separation allows both systems to evolve independently while keeping the rendering pipeline stable and deterministic.

---

# High-Level Pipeline

```
Creative Director
        ↓
Strategy Director
        ↓
Scene Planner
        ↓
Music Analyzer
        ↓
Timeline Planner
        ↓
Motion Director
        ↓
Effect Director
        ↓
Transition Director
        ↓
Director Memory
        ↓
Director Score
        ↓
RenderPlanBuilder
        ↓
RenderPlan
        ↓
FFmpegBuilder
        ↓
Renderer
```

---

# AI Decision Layer

The AI layer contains multiple specialized directors.

Each director has a single responsibility and contributes only to its own domain.

## Creative Director

Defines the overall creative direction of the video.

Responsible for:

- creative vision
- storytelling direction
- pacing goals
- editing philosophy

---

## Strategy Director

Transforms the creative vision into an editing strategy.

Responsible for:

- editing style
- video structure
- retention strategy
- audience optimization

---

## Scene Planner

Splits the content into logical scenes.

Responsible for:

- scene boundaries
- scene purpose
- scene priorities

---

## Music Analyzer

Analyzes the soundtrack.

Responsible for:

- beat detection
- drops
- emotional moments
- pacing changes
- music synchronization

---

## Timeline Planner

Creates the first editable TimelinePlan.

Each TimelineClip contains:

- timing
- creative role
- music strategy
- subtitle style
- camera plan
- motion plan
- effect plan
- transition style

TimelinePlan is the main AI editing timeline.

---

## Motion Director

Enhances TimelinePlan with motion decisions.

Examples:

- emphasis animations
- callouts
- visual movement

---

## Effect Director

Adds cinematic effects.

Examples:

- flashes
- glow
- blur
- RGB split
- shake

---

## Transition Director

Chooses transitions between clips.

Selection depends on:

- pacing
- emotion
- music
- editing rhythm

---

## Director Memory

Stores reusable editing knowledge.

Responsible for:

- learning successful edits
- remembering editing patterns
- future optimization

---

## Director Score

Evaluates every AI decision.

Provides confidence scores before rendering.

---

# RenderPlanBuilder

RenderPlanBuilder converts AI decisions into rendering instructions.

Current supported sources:

- Subtitle Events
- Scene Plans
- TimelinePlan

Current output:

- SubtitleInstruction
- ZoomInstruction
- MotionInstruction
- BrollInstruction

RenderPlanBuilder acts as the bridge between the AI Engine and the Renderer.

---

# RenderPlan

RenderPlan is the official rendering contract.

Every renderer receives exactly the same structure regardless of how it was generated.

Current instruction types:

- Subtitles
- Zooms
- Motions
- B-roll

Future instruction types:

- Effects
- Transitions
- Camera
- Color Grading
- Audio
- Speed Ramps

---

# Rendering Layer

## FFmpegBuilder

Builds the rendering commands.

Supports multiple rendering modes:

- legacy
- hybrid_subtitles
- ai_full
- timeline_ai

---

## Overlay Renderer

Responsible for:

- PNG overlays
- WebM overlays
- MOV overlays
- positioning
- synchronization

---

## Subtitle Renderer

Responsible for:

- subtitle timing
- subtitle rendering
- subtitle animations

---

## Zoom Renderer

Responsible for:

- camera zooms
- scaling
- movement timing

---

## Renderer

Final execution layer.

The renderer never performs creative reasoning.

It only executes RenderPlan instructions.

---

# Design Principles

The Video Engine follows five core principles.

## 1. AI decides.

Only AI components make creative decisions.

---

## 2. Renderer executes.

Rendering should never contain business logic.

---

## 3. RenderPlan is the contract.

Every editing workflow must eventually produce RenderPlan.

---

## 4. Components remain independent.

Each director has one responsibility.

Each renderer has one responsibility.

---

## 5. Backward compatibility.

New AI systems must coexist with legacy rendering until migration is complete.

---

# Current Status

Implemented:

✅ Creative Director

✅ Strategy Director

✅ Scene Planner

✅ Music Analyzer

✅ Timeline Planner

✅ Motion Director

✅ Effect Director

✅ Transition Director

✅ Director Memory

✅ Director Score

✅ RenderPlanBuilder Timeline Integration

✅ timeline_ai rendering mode

✅ AI → Renderer bridge

Next milestones:

- Subtitle Translator
- Camera Translator
- Motion Translator refactor
- Effect Translator
- Transition Translator
- B-roll Translator
- Full AI-controlled rendering pipeline
