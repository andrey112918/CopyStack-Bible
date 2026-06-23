# Project Structure

# Overview

CopyStack is organized into independent modules.

Each module has one responsibility.

The project is designed around a layered architecture where AI, rendering and infrastructure remain completely separated.

---

# High Level Structure

```
src/

    ai/

    pipeline/

    render_plan/

    renderer/

    timeline/

    employees/

    jobs/

    audio/

    subtitles/

    assets/

    utils/
```

---

# AI

```
src/ai/
```

Contains the entire AI Decision Engine.

Responsible for understanding the video and making creative decisions.

Current pipeline:

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
```

Produces:

- TimelinePlan
- Editing decisions
- Creative strategies

The AI module never renders video.

---

# Pipeline

```
src/pipeline/
```

Acts as the bridge between AI and rendering.

Current responsibilities:

- RenderPlanBuilder
- SceneToRenderPlanAdapter

Future responsibilities:

- SubtitleTranslator
- CameraTranslator
- MotionTranslator
- EffectTranslator
- TransitionTranslator
- BrollTranslator

Pipeline converts AI decisions into RenderPlan.

---

# RenderPlan

```
src/render_plan/
```

Defines the universal rendering language.

Current instruction types:

- SubtitleInstruction
- ZoomInstruction
- MotionInstruction
- BrollInstruction

Future instruction types:

- EffectInstruction
- TransitionInstruction
- CameraInstruction
- AudioInstruction
- ColorGradingInstruction

Every renderer consumes RenderPlan.

---

# Renderer

```
src/renderer/
```

Responsible for rendering only.

Main modules:

- Renderer
- FFmpegBuilder
- OverlayRenderer
- SubtitleRenderer
- ZoomRenderer
- MotionRenderer
- CutRenderer
- Exporter

The renderer never performs creative reasoning.

---

# Timeline

```
src/timeline/
```

Stores the editing timeline.

Contains:

- Timeline
- Timeline Events
- Timeline Tracks

Legacy rendering still uses Timeline while migration to TimelinePlan is in progress.

---

# Employees

```
src/employees/
```

Contains specialized AI employees responsible for individual editing domains.

Examples:

- Subtitle Director
- Motion Director

Future AI employees should be added here.

---

# Jobs

```
src/jobs/
```

Stores job execution data.

Examples:

- temporary renders
- exported videos
- reports
- intermediate assets

---

# Audio

```
src/audio/
```

Responsible for audio processing.

Examples:

- transcription
- beat detection
- silence detection
- music analysis

---

# Assets

```
src/assets/
```

Stores reusable visual resources.

Examples:

- overlays
- transitions
- effects
- motion graphics
- subtitles
- LUTs

---

# Utilities

```
src/utils/
```

Shared helper functions used throughout the project.

---

# Architecture Principles

## AI and Rendering are separated.

AI decides.

Renderer executes.

---

## RenderPlan is the universal contract.

Every editing workflow eventually produces RenderPlan.

---

## Single Responsibility.

Each module owns exactly one responsibility.

---

## Backward Compatibility.

Legacy systems remain operational until migration is complete.

---

# Current Status

Implemented:

- AI Decision Engine
- Timeline Planner
- Motion Director
- Effect Director
- Transition Director
- Director Memory
- Director Score
- Timeline AI Integration
- RenderPlanBuilder Timeline Support
- Renderer Integration

In Progress:

- Subtitle Translator
- Camera Translator
- Motion Translator refactor
- Effect Translator
- Transition Translator

Future:

- Asset Intelligence
- AI Jury
- Localhost Platform
- Intelligent Asset Library
- Explain Mode

# CopyStack Video Engine

## High-Level Architecture

```
                 Input Video
                      │
                      ▼
              Speech Analysis
                      │
                      ▼
             Content Analysis
                      │
                      ▼
               Story Engine
                      │
                      ▼
         Story Progress Tracker
                      │
                      ▼
             Director Brain
                      │
                      ▼
            Timeline Planner
                      │
                      ▼
        Motion Decision Engine
                      │
                      ▼
            Motion Recipes
                      │
                      ▼
            Motion Plugins
                      │
                      ▼
            Motion Renderer
                      │
                      ▼
              Render Plan
                      │
                      ▼
             FFmpeg Export
                      │
                      ▼
               Final Video
```

---

## Core Systems

### Analysis Layer

- Speech Analysis
- Content Analysis
- Story Engine
- Story Progress Tracker

---

### Intelligence Layer

- Director Brain
- Timeline Planner
- Motion Decision Engine
- Motion Recipe System

---

### Execution Layer

- Motion Plugins
- Motion Renderer
- FFmpeg Renderer

---

## Design Principles

- AI plans.
- Timeline organizes.
- Renderer executes.
- Plugins extend functionality.
- Recipes define behavior.
- Story drives motion.
- Every decision must remain explainable.
