# Changelog

All notable changes to CopyStack are documented in this file.

---

# Version 0.3.0

## AI Engine

### Added

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

### Rendering

Added:

- RenderPlanBuilder
- Timeline AI Integration
- timeline_ai rendering mode
- AI → Renderer bridge

Renderer now supports RenderPlan generated from TimelinePlan.

### Architecture

Introduced complete separation between:

- AI Engine
- Render Engine

RenderPlan is now the official communication contract between both systems.

### Documentation

Updated CopyStack Bible:

- CopyStack Core
- Video Engine Architecture
- AI Employees
- Project Structure
- Future AI
- Daily Reports

---

# Next Version

Upcoming work:

- Subtitle Translator
- Camera Translator
- Motion Translator refactor
- Effect Translator
- Transition Translator
- B-roll Translator

Goal:

Complete AI-controlled rendering pipeline.
