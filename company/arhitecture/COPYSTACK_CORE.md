# CopyStack Core Architecture

## Overview

CopyStack is built around one fundamental architectural principle:

> **Artificial Intelligence makes creative decisions. The renderer executes them.**

Every system inside CopyStack exists to support this philosophy.

The project is intentionally divided into two completely independent systems:

- AI Engine
- Render Engine

Both systems communicate through a single standardized contract called **RenderPlan**.

This separation guarantees scalability, maintainability and long-term flexibility.

---

# Core Philosophy

CopyStack does not render videos.

CopyStack builds intelligent editing decisions.

Rendering is only the final execution step.

This allows the AI Engine to evolve independently without requiring changes inside the renderer.

---

# System Architecture

```
                AI ENGINE

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

============================

          RenderPlan

============================

          RENDER ENGINE

FFmpegBuilder
        ↓
Renderer
        ↓
Subtitle Renderer
        ↓
Motion Renderer
        ↓
Overlay Renderer
        ↓
Zoom Renderer
        ↓
Final Video
```

---

# AI Engine

The AI Engine is responsible for understanding the video and deciding what should happen.

It never performs rendering.

Responsibilities include:

- storytelling
- pacing
- retention optimization
- scene planning
- subtitle strategy
- motion strategy
- camera decisions
- effects
- transitions
- synchronization with music

Every creative decision is made before rendering begins.

---

# RenderPlan

RenderPlan is the official communication contract between AI and rendering.

Every editing workflow eventually produces a RenderPlan.

Current instruction types:

- SubtitleInstruction
- ZoomInstruction
- MotionInstruction
- BrollInstruction

Future instruction types:

- EffectInstruction
- TransitionInstruction
- CameraInstruction
- ColorGradingInstruction
- AudioInstruction
- SpeedRampInstruction

RenderPlan guarantees that the renderer never depends on AI implementation details.

---

# Render Engine

The Render Engine executes RenderPlan.

It never performs creative reasoning.

Its responsibilities are:

- rendering subtitles
- rendering overlays
- rendering motion graphics
- rendering zooms
- exporting the final video

If RenderPlan changes, the renderer simply executes the new instructions.

---

# Timeline AI Integration

The AI pipeline now supports direct TimelinePlan rendering.

Current flow:

```
TimelinePlan
        ↓
RenderPlanBuilder
        ↓
RenderPlan
        ↓
FFmpegBuilder
        ↓
Renderer
```

This is the first complete bridge between the AI Engine and the Render Engine.

Legacy rendering remains fully supported during migration.

---

# Architectural Principles

## 1. AI decides

Creative logic belongs exclusively inside the AI Engine.

---

## 2. Renderer executes

The renderer never decides.

It only executes RenderPlan instructions.

---

## 3. Single Responsibility

Every Director owns exactly one domain.

Every Renderer owns exactly one rendering responsibility.

---

## 4. Universal Rendering Contract

RenderPlan is the only language understood by the renderer.

Future sources include:

- AI Engine
- Manual Timeline Editor
- Template Marketplace
- External API
- Localhost Editor

All of them must generate RenderPlan.

---

## 5. Backward Compatibility

New AI systems should coexist with legacy systems until migration is complete.

Breaking the rendering pipeline is never acceptable.

---

# Current Status

Implemented:

- Creative Director
- Strategy Director
- Scene Planner
- Music Analyzer
- Timeline Planner
- Motion Director
- Effect Director
- Transition Director
- Director Memory
- Director Score
- RenderPlanBuilder
- Timeline AI Integration
- timeline_ai rendering mode
- AI → Renderer bridge

Next milestones:

- Subtitle Translator
- Camera Translator
- Motion Translator refactor
- Effect Translator
- Transition Translator
- B-roll Translator
- Fully AI-driven rendering pipeline

---

# Long-Term Vision

The long-term goal of CopyStack is to become an autonomous AI video editor.

The AI Engine should eventually understand:

- storytelling
- audience retention
- music
- emotion
- pacing
- branding
- editing style

and convert those decisions into a RenderPlan that can be executed by any rendering backend.

This architecture ensures that future renderers (FFmpeg, GPU rendering, cloud rendering, or real-time rendering) can all use the same AI Engine without modification.
