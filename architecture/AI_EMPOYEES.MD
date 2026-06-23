# AI Employees

## Overview

The CopyStack AI Engine is composed of specialized AI Employees.

Each employee has one clear responsibility and collaborates with the others through structured data rather than direct rendering logic.

No employee renders video.

Every employee contributes knowledge that is later transformed into a RenderPlan and executed by the rendering engine.

---

# AI Decision Flow

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
Renderer
```

---

# Creative Director

## Mission

Owns the creative vision of the video.

## Responsibilities

- Understand the project goal.
- Define the editing style.
- Decide the emotional direction.
- Coordinate every other AI employee.

## Output

Creative strategy for the entire video.

---

# Strategy Director

## Mission

Transforms creative vision into an executable editing strategy.

## Responsibilities

- Video pacing
- Retention strategy
- Audience optimization
- Story progression

## Output

Editing strategy.

---

# Scene Planner

## Mission

Split content into logical scenes.

## Responsibilities

- Scene detection
- Scene priorities
- Scene objectives
- Story flow

## Output

Scene Plans.

---

# Music Analyzer

## Mission

Understand the soundtrack.

## Responsibilities

- Beat detection
- Drop detection
- Chorus detection
- Emotional changes
- Tempo analysis
- Music synchronization

## Output

Music Analysis.

---

# Timeline Planner

## Mission

Create the master editing timeline.

## Responsibilities

Generate TimelinePlan containing:

- TimelineClips
- Timing
- Camera plans
- Subtitle styles
- Motion plans
- Effect plans
- Transition styles

## Output

TimelinePlan.

---

# Motion Director

## Mission

Design motion graphics.

## Responsibilities

- Text animations
- Motion emphasis
- Callouts
- Motion pacing

## Output

Motion Plan.

---

# Effect Director

## Mission

Choose cinematic effects.

## Responsibilities

- Flash
- Glow
- Blur
- RGB Split
- Camera Shake
- Cinematic Effects

## Output

Effect Plan.

---

# Transition Director

## Mission

Design transitions between scenes.

## Responsibilities

- Transition timing
- Transition type
- Transition intensity
- Transition synchronization

## Output

Transition Plan.

---

# Director Memory

## Mission

Learn from previous editing decisions.

## Responsibilities

- Store successful edits
- Remember patterns
- Improve future decisions

## Output

Historical editing knowledge.

---

# Director Score

## Mission

Evaluate every AI decision.

## Responsibilities

- Confidence scoring
- Decision validation
- Quality estimation
- Final recommendation

## Output

Decision scores.

---

# Collaboration Model

Each AI Employee performs exactly one task.

Employees never duplicate responsibilities.

Communication happens only through structured models.

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

---

# Design Principles

## Single Responsibility

Every AI Employee owns one domain only.

---

## Explainability

Every decision should be explainable.

Future Explain Mode will show:

- which employee made the decision;
- why the decision was taken;
- confidence score;
- alternative decisions.

---

## Independence

Employees never know how rendering works.

Rendering is delegated entirely to the Render Engine.

---

## Long-Term Vision

Future AI Employees may include:

- Camera Director
- Color Director
- Audio Director
- Lighting Director
- Story Director
- Emotion Director
- Thumbnail Director
- Outreach Director
- Analytics Director

# Motion Decision Engine

## Purpose

Determines the most appropriate motion strategy for every scene based on story progression, speech analysis and timeline context.

---

## Responsibilities

- Evaluate motion context.
- Select the most appropriate recipe.
- Compute confidence score.
- Generate decision metadata.
- Explain every decision.

---

## Inputs

- MotionContext
- StoryState
- Timeline metadata
- Speech metadata

---

## Outputs

- MotionDecision
- MotionRecipe
- Confidence
- Reason
- Warnings

---

# Story Progress Tracker

## Purpose

Tracks narrative progression throughout the video.

---

## Responsibilities

- Measure story progression.
- Detect pacing changes.
- Estimate narrative intensity.
- Provide context for Motion Intelligence.

---

## Outputs

- StoryState
- Story Progress
- Narrative Phase

The AI Engine is designed to grow by adding new specialized employees without changing the existing architecture.
